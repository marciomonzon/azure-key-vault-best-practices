# Azure Key Vault Best Practices

<ul>
  <li>
    **Managed identities for Azure resources:** When you deploy an app on a virtual machine in Azure, you can assign an identity to your virtual machine that has access to 
     Key Vault. You can also assign identities to other Azure resources. The benefit of this approach is that the app or service isn't managing the rotation of the first 
     secret. Azure automatically rotates the service principal client secret associated with the identity. We recommend this approach as a best practice
  </li>
  <li>
    **Use separate key vaults:** Recommended using a vault per application per environment (Development, Pre-Production and Production). This pattern helps you not share 
     secrets across environments and also reduces the threat if there is a breach.
  </li>
  <li>
    **Control access to your vault:** Key Vault data is sensitive and business critical, 
    you need to secure access to your key vaults by allowing only authorized applications and 
   users.
  </li>
  <li>
    **Backup:** Create regular back ups of your vault on update/delete/create of objects within a Vault.
  </li>
  <li>
    **Logging:** Be sure to turn on logging and alerts.
  </li>
  <li>
    **Recovery options:** Turn on soft-delete and purge protection if you want to guard against force deletion of the secret.
  </li>
</ul>
