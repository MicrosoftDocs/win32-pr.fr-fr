---
title: Exemple de création d’une clé de session
description: Exemple de création d’une clé de session
ms.assetid: 4347502b-3900-4306-b58c-16d151200e6c
keywords:
- Windows Media Format SDK, clés de session
- Windows Media Format SDK, clés de contenu
- Windows Media Format SDK, exemple de code
- Windows Media Format SDK, exemples de code
- gestion des droits numériques (DRM), clés de session
- DRM (gestion des droits numériques), clés de session
- gestion des droits numériques (DRM), clés de contenu
- DRM (gestion des droits numériques), clés de contenu
- gestion des droits numériques (DRM), exemple de code
- DRM (gestion des droits numériques), exemple de code
- gestion des droits numériques (DRM), exemples de code
- DRM (gestion des droits numériques), exemples de code
- API étendues du client DRM, clés de session
- API étendues clientes, clés de session
- API étendues du client DRM, clés de contenu
- API étendues clientes, clés de contenu
- API étendues du client DRM, exemple de code
- API étendues clientes, exemple de code
- API étendues du client DRM, exemples de code
- API étendues clientes, exemples de code
- clés de session
- clés de contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b757f5d67df0aea1dd70ee45ad2d1b0732040be2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404703"
---
# <a name="create-session-key-example"></a>Exemple de création d’une clé de session

La clé de session est utilisée pour protéger la clé de contenu. Le code suivant montre comment créer une clé de session, mais qui ignore les détails de la génération de clés aléatoires.


```C++
HRESULT CreateSessionKey( WMDRM_IMPORT_SESSION_KEY **ppSessionKey, DWORD *pcbSessionKey )
{
    // TODO: Set this value to the desired number of bytes for the session key data. 
    const DWORD SESSION_KEY_DATA_SIZE = 20; 

    HRESULT hr = S_OK;
    WMDRM_IMPORT_SESSION_KEY *pSessionKey = NULL;

    if( NULL == ppSessionKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }
    
    // Compute the size of the session key structure plus the session key.
    DWORD cbSessionKey = sizeof( WMDRM_IMPORT_SESSION_KEY ) + SESSION_KEY_DATA_SIZE;

    // Allocate memory for the session key.
    pSessionKey = (WMDRM_IMPORT_SESSION_KEY *)new BYTE[ cbSessionKey ];
    if( NULL == pSessionKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }
    ZeroMemory( pSessionKey, cbSessionKey );

    // Set the key type and the key size.
    pSessionKey->dwKeyType = WMDRM_KEYTYPE_RC4;
    pSessionKey->cbKey = SESSION_KEY_DATA_SIZE;
    
    // Set the key to a random value. Note that the random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in shipping code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pSessionKey->rgbKey;
    for (size_t i = 0; i < SESSION_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }
    
    // If all has been successful set the parameters.
    *ppSessionKey = pSessionKey;
    pSessionKey = NULL;
    *pcbSessionKey = cbSessionKey;

EXIT:
    
    SAFE_ARRAY_DELETE( pSessionKey );
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples d’importation DRM**](drm-import-examples.md)
</dt> </dl>

 

 




