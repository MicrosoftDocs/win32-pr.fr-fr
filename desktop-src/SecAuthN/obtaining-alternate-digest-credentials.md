---
description: Pour obtenir des informations d’identification autres que celles associées à la session active Logon, renseignez une \_ \_ structure d’identité de l’authentification Winnt avec des \_ informations pour le principal de sécurité de substitution.
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: Obtention d’autres informations d’identification de Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed7daa2a3179822929e8c2df8077ee55afaadb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123358"
---
# <a name="obtaining-alternate-digest-credentials"></a>Obtention d’autres informations d’identification de Digest

Pour obtenir des informations [*d’identification*](../secgloss/c-gly.md) autres que celles associées à la [*session*](../secgloss/s-gly.md)active Logon, renseignez une structure d’identité de l' [**\_ \_ authentification \_ winnt**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) avec des informations pour le [*principal de sécurité*](../secgloss/s-gly.md)de substitution. Transmettez la structure à la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) à l’aide du paramètre *pAuthData* .

Le tableau suivant décrit les membres de la structure de l' [**\_ \_ \_ identité d’authentification Winnt**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la sec.



| Membre             | Description                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **Utilisateur**           | Chaîne terminée par le caractère null qui contient le nom du principal de sécurité dont les informations d’identification seront utilisées pour établir un contexte de sécurité. |
| **UserLength**     | Longueur du membre **utilisateur** , en caractères. Omettez la valeur null de fin.                                                         |
| **Domaine**         | Chaîne terminée par le caractère null qui identifie le domaine contenant le compte du principal de sécurité.                                  |
| **DomainLength**   | Longueur du membre de **domaine** , en caractères. Omettez la valeur null de fin.                                                       |
| **Mot de passe**       | Chaîne terminée par le caractère null qui contient le mot de passe du principal de sécurité.                                                            |
| **PasswordLength** | Longueur du membre de **mot de passe** , en caractères. Omettez la valeur null de fin.                                                     |
| **Indicateurs**          | Indique si les membres de la chaîne sont au format ANSI ou [*Unicode*](../secgloss/u-gly.md) .  |



 

Le tableau suivant répertorie les valeurs valides pour le membre **Flags** de la structure.



| Constante                            | Description                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| SEC \_ identité d’authentification Winnt \_ \_ \_ ANSI    | Les chaînes de cette structure sont au format ANSI.                                                                    |
| SEC \_ identité d’authentification Winnt \_ \_ \_ Unicode | Les chaînes de cette structure sont au format [*Unicode*](../secgloss/u-gly.md) . |



 

La structure et les constantes sont déclarées dans le fichier d’en-tête rpcdce. h distribué avec le kit de développement logiciel (SDK) de la plateforme.

L’exemple suivant illustre un appel côté client pour obtenir des informations d’identification de résumé pour un compte d’utilisateur spécifique.


```C++
#include <windows.h>

#ifdef UNICODE
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;
#else
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_ANSI;
#endif

void main()
{
    SECURITY_STATUS SecStatus; 
    TimeStamp tsLifetime; 
    CredHandle hCred;
    SEC_WINNT_AUTH_IDENTITY ClientAuthID;
    LPTSTR UserName = TEXT("ASecurityPrinciple");
    LPTSTR DomainName = TEXT("AnAuthenticatingDomain");

    // Initialize the memory.
    ZeroMemory( &ClientAuthID, sizeof(ClientAuthID) );

    // Specify string format for the ClientAuthID structure.


    // Specify an alternate user, domain and password.
      ClientAuthID.User = (unsigned char *) UserName;
      ClientAuthID.UserLength = _tcslen(UserName);

      ClientAuthID.Domain = (unsigned char *) DomainName;
      ClientAuthID.DomainLength = _tcslen(DomainName);

    // Password is an application-defined LPTSTR variable
    // containing the user password.
      ClientAuthID.Password = Password;
      ClientAuthID.PasswordLength = _tcslen(Password);

    // Get the client side credential handle.
    SecStatus = AcquireCredentialsHandle (
      NULL,                  // Default principal.
      WDIGEST_SP_NAME,       // The Digest SSP. 
      SECPKG_CRED_OUTBOUND,  // Client will use the credentials.
      NULL,                  // Do not specify LOGON id.
      &ClientAuthID,         // User information.
      NULL,                  // Not used with Digest SSP.
      NULL,                  // Not used with Digest SSP.
      &hCred,                // Receives the credential handle.
      &tsLifetime            // Receives the credential time limit.
    );
}
```



La fonction **\_ tcslen** retourne la longueur de chaîne en caractères, à l’exclusion du caractère null de fin.

Si votre application peut utiliser les informations d’identification établies lors de l’ouverture de session, consultez [obtention des informations d’identification du condensé par défaut](obtaining-default-digest-credentials.md).

 

 
