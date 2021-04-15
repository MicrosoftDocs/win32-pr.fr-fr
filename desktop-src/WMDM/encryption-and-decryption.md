---
title: Chiffrement et déchiffrement
description: Chiffrement et déchiffrement
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Gestionnaire de périphériques Windows Media, chiffrement
- Gestionnaire de périphériques, chiffrement
- applications de bureau, chiffrement
- fournisseurs de services, chiffrement
- Guide de programmation, chiffrement
- le chiffrement
- Gestionnaire de périphériques Windows Media, déchiffrement
- Gestionnaire de périphériques, déchiffrement
- applications de bureau, déchiffrement
- fournisseurs de services, déchiffrement
- Guide de programmation, déchiffrement
- déchiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78688c1b4ca9991d8b322c6991de96a51e7e8d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382660"
---
# <a name="encryption-and-decryption"></a>Chiffrement et déchiffrement

Windows Media Gestionnaire de périphériques nécessite le chiffrement des fichiers envoyés entre le fournisseur de services et l’application. Cette opération peut être effectuée de deux manières :

-   Si le fournisseur de services prend en charge uniquement [**IMDSPObject :: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) et [**IMDSPObject :: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), les données doivent être chiffrées et déchiffrées par l’application et le fournisseur de services à l’aide des méthodes [CSecureChannelClient](csecurechannelclient-class.md) et [CSecureChannelServer](csecurechannelserver-class.md) , respectivement.
-   Si le fournisseur de services prend en charge [**IMDSPObject2 :: ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) et [**IMDSPObject2 :: WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), votre application peut éviter l’authentification coûteuse des messages de canal sécurisé. (Le canal sécurisé est conservé afin que les fournisseurs de services hérités qui n’implémentent pas [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) continuent à fonctionner.)

L’exigence de chiffrement empêche les applications malveillantes d’obtenir des données transmises entre les composants logiciels et protège également l’intégrité des données envoyées vers ou depuis l’appareil.

Les trois méthodes suivantes requièrent le chiffrement ou le déchiffrement.



| Méthode                                                                          | Description                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMDMOperation::TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | Oeuvre Chiffrement ou déchiffrement, selon que l’application envoie ou reçoit des données. |
| [**IMDSPObject :: lecture**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | (Fournisseur de services) Chiffre.                                                                             |
| [**IMDSPObject :: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | (Fournisseur de services) Déchiffrement.                                                                             |



 

Le chiffrement et le déchiffrement sont tous deux effectués par des appels de méthode uniques. Le chiffrement est effectué par [**CSecureChannelClient :: EncryptParam**](/previous-versions/bb231587(v=vs.85)) pour les applications ou par [**CSecureChannelServer :: EncryptParam**](/previous-versions/ms868509(v=msdn.10)) pour les fournisseurs de services. Le déchiffrement s’effectue par [**CSecureChannelClient ::D ecryptparam**](/previous-versions/bb231586(v=vs.85)) pour les applications ou [**CSecureChannelServer ::D ecryptparam**](/previous-versions/bb231598(v=vs.85)) pour les fournisseurs de services. Les paramètres sont identiques entre les méthodes client et serveur.

Les étapes suivantes montrent comment chiffrer et déchiffrer les données. (Ces étapes sont importantes uniquement si votre application communique avec un fournisseur de services hérité qui n’implémente pas [IWMDMOperation3 :: TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)

**Chiffrement**

1.  Créez la clé MAC pour les données chiffrées, comme décrit dans [authentification de message](message-authentication.md).
2.  Appelez **EncryptParam** avec les données à chiffrer pour effectuer un chiffrement sur place.

L’exemple de code suivant illustre l’implémentation d’un fournisseur de services de [**IMDSPObject :: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read). Cette méthode crée la clé MAC à l’aide des données à chiffrer et de la taille des données, puis les envoie à l’application.


```C++
HRESULT CMyStorage::Read(
    BYTE  *pData,
    DWORD *pdwSize,
    BYTE   abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwToRead;         // Bytes to read.
    DWORD    dwRead   = NULL;  // Bytes read.
    BYTE    *pTmpData = NULL;  // Temporary buffer to hold data before 
                               // it is copied to pData.

    // Use a global CSecureChannelServer member to verify that 
    // the client is authenticated.
    if (!(g_pAppSCServer->fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    

    // Verify that the handle to the file to read is valid.
    if(m_hFile == INVALID_HANDLE_VALUE)
    {
        return E_FAIL;
    }

    // Create a buffer to hold the data read.    
    dwToRead = *pdwSize;
    pTmpData = new BYTE [dwToRead] ;
    if(!pTmpData)
        return E_OUTOFMEMORY;

    // Read data into the temporary buffer.
    if(ReadFile(m_hFile,(LPVOID)pTmpData,dwToRead,&dwRead,NULL)) 
    { 
        *pdwSize = dwRead; 

        if( dwRead )
        {
            // Create a MAC from all the parameters.
            // CORg is a macro that goes to Error label on failure.
            // MAC consists of data and size of data.
            HMAC hMAC;
            
            CORg(g_pAppSCServer->MACInit(&hMAC));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD)));
            CORg(g_pAppSCServer->MACFinal(hMAC, abMac));
            
            // Encrypt the data.
            CORg(g_pAppSCServer->EncryptParam(pTmpData, dwRead));
            
            // Copy data from the temporary buffer into the out parameter.
            memcpy(pData, pTmpData, dwRead);
        }
    
        hr = S_OK; 
    }
    else
    { 
        *pdwSize = 0; 

        hr = E_FAIL; 
    }

Error:

    if(pTmpData) 
    {
        delete [] pTmpData;
    }

    return hr;
} 
```



**Déchiffrement**

1.  Appelez **DecryptParam** avec les données à chiffrer pour effectuer un déchiffrement sur place.
2.  Vérifiez la clé MAC pour les données déchiffrées, comme décrit dans [authentification de message](message-authentication.md).

L’exemple de code suivant illustre l’implémentation d’un fournisseur de services de [**IMDSPObject :: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write). Cette méthode crée la clé MAC à l’aide des données à chiffrer et de la taille des données, puis les envoie à l’application.


```C++
HRESULT CMyStorage::Write(BYTE *pData, DWORD *pdwSize,
                                 BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwWritten = 0;
    BYTE    *pTmpData  = NULL;          // Temporary buffer to hold the 
                                        // data during decryption.
    BYTE     pTempMac[WMDM_MAC_LENGTH]; // Temporary MAC that will be 
                                        // copied into the abMac
                                        // out parameter.

    if( m_hFile == INVALID_HANDLE_VALUE )
    {
        return E_FAIL;
    }

    // Allocate the temporary buffer and copy the encrypted data into it.
    pTmpData = new BYTE [*pdwSize];
    if(!pTmpData)
        return E_OUTOFMEMORY;
    memcpy(pTmpData, pData, *pdwSize);

    // Decrypt the data.
    CHRg(g_pAppSCServer->DecryptParam(pTmpData, *pdwSize));

    // Check the MAC passed to the method. The MAC is built from
    // the data and data size parameters.
    // CORg is a macro that goes to the Error label on failure.
    HMAC hMAC;
    CORg(g_pAppSCServer->MACInit(&hMAC));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), *pdwSize));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(*pdwSize)));
    CORg(g_pAppSCServer->MACFinal(hMAC, pTempMac));

    // If the MAC values don't match, return an error.
    if (memcmp(abMac, pTempMac, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto Error;
    }

    // The MAC values matched, so write the decrypted data to a local file.
    if( WriteFile(m_hFile,pTmpData,*pdwSize,&dwWritten,NULL) ) 
    {
        hr = S_OK;
    }
    else 
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    *pdwSize = dwWritten;

Error:

    if( pTmpData )
    {
        delete [] pTmpData;
    }

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation de canaux authentifiés sécurisés**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 