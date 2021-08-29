---
description: Utilisation du cache des informations d’identification
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: Utilisation du cache des informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603078c0dce4c3cd335a3efed57c9d698a372bca6d77e6b76631843be6307eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034577"
---
# <a name="using-the-credential-cache"></a>Utilisation du cache des informations d’identification

Media Foundation fournit une implémentation par défaut de l’interface [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) . Une application qui implémente l’interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) peut utiliser l’objet de cache des informations d’identification par défaut pour stocker les informations d’identification de l’utilisateur.

Pour créer l’objet de cache des informations d’identification par défaut, appelez la fonction [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) .


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



Une fois le cache des informations d’identification créé, l’application peut utiliser les méthodes suivantes pour obtenir un objet d’informations d’identification, définir les informations d’identification de l’utilisateur et spécifier les options de mise en cache.

-   Pour obtenir l’objet d’informations d’identification pour une URL, appelez [**IMFNetCredentialCache :: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    Si les informations d’identification pour l’URL spécifiée n’existent pas dans le cache des informations d’identification, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) crée un nouvel objet d’informations d’identification avec des valeurs de nom d’utilisateur et de mot de passe vides.

-   Pour définir le nom d’utilisateur et le mot de passe sur l’objet d’informations d’identification, appelez [**IMFNetCredential :: SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) et [**IMFNetCredential :: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).
-   Pour définir les options de mise en cache sur l’objet Credential, appelez [**IMFNetCredentialCache :: SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    Les valeurs de paramètre *dwOptionsFlags* sont définies dans l’énumération [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) . Pour enregistrer les informations d’identification de l’utilisateur pour une URL dans un stockage persistant, définissez l' \_ indicateur d’enregistrement des informations d’identification MFNET \_ . Si l’appel [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) se termine correctement, l’appel suivant à [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) recherche les informations d’identification dans le stockage persistant. Si une correspondance est trouvée, cette méthode retourne un pointeur vers l’objet d’informations d’identification qui contient les informations.

    Par défaut, les informations d’identification de l’utilisateur envoyées sur le réseau sont chiffrées. Pour modifier cette valeur en texte clair, définissez l' \_ \_ indicateur de \_ texte clair autoriser les informations d’identification MFNET \_ .

    Pour supprimer des informations du Registre, appelez [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) pour récupérer l’objet d’informations d’identification, puis appelez [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) et définissez *dwOptionsFlags* sur MFNET \_ \_ \_ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification de la source réseau](network-source-authentication.md)
</dt> </dl>

 

 



