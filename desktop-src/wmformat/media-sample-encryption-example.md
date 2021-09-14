---
title: Exemple de chiffrement d’échantillon de média
description: Exemple de chiffrement d’échantillon de média
ms.assetid: f57f9ffc-47fd-47fb-b553-07b9cd6abb70
keywords:
- Windows Media Format SDK, Media Sample Encryption
- Windows Media Format SDK, exemple de code
- Windows Media Format SDK, exemples de code
- gestion des droits numériques (DRM), exemple de chiffrement de supports
- DRM (gestion des droits numériques), exemple de chiffrement de supports
- gestion des droits numériques (DRM), exemple de code
- DRM (gestion des droits numériques), exemple de code
- gestion des droits numériques (DRM), exemples de code
- DRM (gestion des droits numériques), exemples de code
- API étendues du client DRM, chiffrement d’échantillon de support
- API étendues clientes, chiffrement d’échantillon de support
- API étendues du client DRM, exemple de code
- API étendues clientes, exemple de code
- API étendues du client DRM, exemples de code
- API étendues clientes, exemples de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a669ab957aa7510cdd57daca798ec3e3ac3bf73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234594"
---
# <a name="media-sample-encryption-example"></a>Exemple de chiffrement d’échantillon de média

L’exemple complet suivant montre comment chiffrer un exemple de support à l’aide du chiffrement DRM. L’algorithme de chiffrement RC4 a été omis de l’exemple en raison de restrictions d’espace.


```C++
QWORD GetNextSalt(QWORD qwSalt)
{
   return InterlockedIncrement64( (volatile LONGLONG*)&qwSalt );
}

HRESULT EncryptSample( INSSBuffer *pSample )
{
    HRESULT hr = S_OK;
    INSSBuffer3 *pNSSBuffer3 = NULL;
    QWORD qwSalt = 0;
    BYTE *pbData = NULL;
    DWORD cbData = 0;

    hr = pSample->QueryInterface( IID_INSSBuffer3, (void**)&pNSSBuffer3 );
    if( FAILED( hr ) ) goto EXIT;

    hr = pSample->GetBufferAndLength( &pbData, &cbData );
    if( FAILED( hr ) ) goto EXIT;

    qwSalt = GetNextSalt(qwSalt);

    // TODO: Encrypt the sample by concatenating the initialization vector
    //   and using RC4 encryption.

    hr = pNSSBuffer3->SetProperty( 
        WM_SampleExtensionGUID_SampleProtectionSalt, 
        &qwSalt, sizeof( qwSalt ) );
    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pNSSBuffer3 );
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples d’importation DRM**](drm-import-examples.md)
</dt> </dl>

 

 




