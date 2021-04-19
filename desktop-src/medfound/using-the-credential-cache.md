---
description: Utilisation du cache des informations d’identification
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: Utilisation du cache des informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d512d0bab8f45f50a587e3c8eda2a73c4832685f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534395"
---
# <a name="using-the-credential-cache"></a><span data-ttu-id="14db6-103">Utilisation du cache des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="14db6-103">Using the Credential Cache</span></span>

<span data-ttu-id="14db6-104">Media Foundation fournit une implémentation par défaut de l’interface [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) .</span><span class="sxs-lookup"><span data-stu-id="14db6-104">Media Foundation provides a default implementation of the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface.</span></span> <span data-ttu-id="14db6-105">Une application qui implémente l’interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) peut utiliser l’objet de cache des informations d’identification par défaut pour stocker les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14db6-105">An application that implements the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface can use the default credential cache object to store the user's credentials.</span></span>

<span data-ttu-id="14db6-106">Pour créer l’objet de cache des informations d’identification par défaut, appelez la fonction [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) .</span><span class="sxs-lookup"><span data-stu-id="14db6-106">To create the default credential cache object, call the [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) function.</span></span>


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



<span data-ttu-id="14db6-107">Une fois le cache des informations d’identification créé, l’application peut utiliser les méthodes suivantes pour obtenir un objet d’informations d’identification, définir les informations d’identification de l’utilisateur et spécifier les options de mise en cache.</span><span class="sxs-lookup"><span data-stu-id="14db6-107">After the credential cache is created, the application can use the following methods to get a credential object, set user credentials, and specify the caching options.</span></span>

-   <span data-ttu-id="14db6-108">Pour obtenir l’objet d’informations d’identification pour une URL, appelez [**IMFNetCredentialCache :: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span><span class="sxs-lookup"><span data-stu-id="14db6-108">To get the credential object for a URL, call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span>

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    <span data-ttu-id="14db6-109">Si les informations d’identification pour l’URL spécifiée n’existent pas dans le cache des informations d’identification, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) crée un nouvel objet d’informations d’identification avec des valeurs de nom d’utilisateur et de mot de passe vides.</span><span class="sxs-lookup"><span data-stu-id="14db6-109">If the credentials for the specified URL do not exist in the credential cache, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) creates a new credential object with empty user name and password values.</span></span>

-   <span data-ttu-id="14db6-110">Pour définir le nom d’utilisateur et le mot de passe sur l’objet d’informations d’identification, appelez [**IMFNetCredential :: SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) et [**IMFNetCredential :: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span><span class="sxs-lookup"><span data-stu-id="14db6-110">To set the user name and password on the credential object, call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span></span>
-   <span data-ttu-id="14db6-111">Pour définir les options de mise en cache sur l’objet Credential, appelez [**IMFNetCredentialCache :: SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span><span class="sxs-lookup"><span data-stu-id="14db6-111">To set the caching options on the credential object, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span></span>

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    <span data-ttu-id="14db6-112">Les valeurs de paramètre *dwOptionsFlags* sont définies dans l’énumération [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) .</span><span class="sxs-lookup"><span data-stu-id="14db6-112">The *dwOptionsFlags* parameter values are defined in the [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) enumeration.</span></span> <span data-ttu-id="14db6-113">Pour enregistrer les informations d’identification de l’utilisateur pour une URL dans un stockage persistant, définissez l' \_ indicateur d’enregistrement des informations d’identification MFNET \_ .</span><span class="sxs-lookup"><span data-stu-id="14db6-113">To save user credentials for a URL in a persistent storage, set the MFNET\_CREDENTIAL\_SAVE flag.</span></span> <span data-ttu-id="14db6-114">Si l’appel [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) se termine correctement, l’appel suivant à [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) recherche les informations d’identification dans le stockage persistant.</span><span class="sxs-lookup"><span data-stu-id="14db6-114">If the [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) call completes successfully, then the subsequent call to [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) searches for the credentials in the persistent storage.</span></span> <span data-ttu-id="14db6-115">Si une correspondance est trouvée, cette méthode retourne un pointeur vers l’objet d’informations d’identification qui contient les informations.</span><span class="sxs-lookup"><span data-stu-id="14db6-115">If a match is found, this method returns a pointer to the credential object that contains the information.</span></span>

    <span data-ttu-id="14db6-116">Par défaut, les informations d’identification de l’utilisateur envoyées sur le réseau sont chiffrées.</span><span class="sxs-lookup"><span data-stu-id="14db6-116">By default, user credentials sent over the network are encrypted.</span></span> <span data-ttu-id="14db6-117">Pour modifier cette valeur en texte clair, définissez l' \_ \_ indicateur de \_ texte clair autoriser les informations d’identification MFNET \_ .</span><span class="sxs-lookup"><span data-stu-id="14db6-117">To change this to clear text, set the MFNET\_CREDENTIAL\_ALLOW\_CLEAR\_TEXT flag.</span></span>

    <span data-ttu-id="14db6-118">Pour supprimer des informations du Registre, appelez [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) pour récupérer l’objet d’informations d’identification, puis appelez [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) et définissez *dwOptionsFlags* sur MFNET \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="14db6-118">To remove information from the registry, call [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) to get the credential object, and then call [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) and set *dwOptionsFlags* to MFNET\_CREDENTIAL\_DONT\_CACHE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14db6-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14db6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14db6-120">Authentification de la source réseau</span><span class="sxs-lookup"><span data-stu-id="14db6-120">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



