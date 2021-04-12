---
title: Initialiser l’exemple d’importation DRM
description: Initialiser l’exemple d’importation DRM
ms.assetid: 46a64305-9aac-47df-992d-6aea8ecb54bf
keywords:
- Windows Media Format SDK, importation DRM
- Windows Media Format SDK, importer
- Windows Media Format SDK, exemple de code
- Windows Media Format SDK, exemples de code
- gestion des droits numériques (DRM), importation
- DRM (gestion des droits numériques), importation
- gestion des droits numériques (DRM), initialisation de l’importation
- DRM (gestion des droits numériques), initialiser l’importation
- gestion des droits numériques (DRM), exemple de code
- DRM (gestion des droits numériques), exemple de code
- gestion des droits numériques (DRM), exemples de code
- DRM (gestion des droits numériques), exemples de code
- API étendues du client DRM, initialiser l’importation
- API étendues du client, initialiser l’importation
- API étendues du client DRM, importation
- API étendues du client, importation
- API étendues du client DRM, exemple de code
- API étendues clientes, exemple de code
- API étendues du client DRM, exemples de code
- API étendues clientes, exemples de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450eeaa128c17d0d64511dd028cda3ce1c4f28c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197318"
---
# <a name="initialize-drm-import-example"></a><span data-ttu-id="d1e68-123">Initialiser l’exemple d’importation DRM</span><span class="sxs-lookup"><span data-stu-id="d1e68-123">Initialize DRM Import Example</span></span>

<span data-ttu-id="d1e68-124">L’exemple de code suivant illustre l’initialisation d’un objet Writer DRM pour l’importation DRM :</span><span class="sxs-lookup"><span data-stu-id="d1e68-124">The following code example illustrates how to initialize a DRM writer object for DRM Import:</span></span>


```C++
HRESULT InitializeImport( IWMDRMWriter3 *pDRMWriter )
{
    // Set this value to the desired number of bytes in an encrypted 
    //  session key.
    const int MODULUS_SIZE = 32;

    HRESULT hr = S_OK;
    WMDRM_IMPORT_INIT_STRUCT ImportInit;

    BYTE *pbEncryptedSessionKey = NULL;
    DWORD cbEncryptedSessionKey = 0;

    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;
    DWORD cbSessionKey = 0;

    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;
    DWORD cbContentKey = 0;
        
    // Allocate memory for the encrypted session key.
    pbEncryptedSessionKey = new BYTE[ MODULUS_SIZE ];
    if( NULL == pbEncryptedSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    cbEncryptedSessionKey = MODULUS_SIZE;

    hr = CreateSessionKey( &pSessionKey, &cbSessionKey );
    if( FAILED( hr ) ) goto EXIT;

    if( cbSessionKey > MODULUS_SIZE )
    if( FAILED( hr ) ) goto EXIT;

    hr = CreateContentKey( &pContentKey, &cbContentKey );
    if( FAILED( hr ) ) goto EXIT;

    // TODO: Encrypt the content key with the session Key.    
    // TODO: Encrypt the session key with the machine certificate public key.   

    ImportInit.dwVersion = 0;
    ImportInit.pbEncryptedSessionKeyMessage = pbEncryptedSessionKey;
    ImportInit.cbEncryptedSessionKeyMessage = cbEncryptedSessionKey;
    ImportInit.pbEncryptedKeyMessage = (BYTE*)pContentKey;
    ImportInit.cbEncryptedKeyMessage = cbContentKey;

    hr = pDRMWriter->SetProtectStreamSamples( &ImportInit );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_ARRAY_DELETE( pContentKey );
    SAFE_ARRAY_DELETE( pSessionKey );

    return( hr );
}
```



## <a name="related-topics"></a><span data-ttu-id="d1e68-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1e68-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1e68-126">**Exemple de création d’une clé de contenu**</span><span class="sxs-lookup"><span data-stu-id="d1e68-126">**Create Content Key Example**</span></span>](create-content-key-example.md)
</dt> <dt>

[<span data-ttu-id="d1e68-127">**Exemple de création d’une clé de session**</span><span class="sxs-lookup"><span data-stu-id="d1e68-127">**Create Session Key Example**</span></span>](create-session-key-example.md)
</dt> <dt>

[<span data-ttu-id="d1e68-128">**Exemples d’importation DRM**</span><span class="sxs-lookup"><span data-stu-id="d1e68-128">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




