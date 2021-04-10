---
description: Spécifie le schéma de protection pour les exemples chiffrés.
ms.assetid: 04E9F908-C61C-43DC-8CF5-9A629FCDD82C
title: Attribut MFSampleExtension_Encryption_ProtectionScheme (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de298eb310e1258274a4ce24d49e9b53def38cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115006"
---
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a>\_Attribut ProtectionScheme de chiffrement MFSampleExtension \_

Spécifie le schéma de protection pour les exemples chiffrés.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

La valeur de cet attribut est un membre de l’énumération [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) . Dans les cas où la source du média est MP4, la valeur est définie en fonction de la valeur du **champ \_ type de schéma** dans la zone type de schéma (« SCHM ») dans l’en-tête MP4 (« Moov » ou « moof »).

Si le **champ \_ type de schéma** dans un fichier MP4, ou Stream, a la valeur’Cenc’ou’CBC1 ', l’attribut **MFSampleExtension \_ Encryption \_ ProtectionScheme** doit être défini sur le **modèle de protection \_ \_ AES \_ CTR** ou **protection \_ Scheme \_ CBC**, respectivement, et aucune valeur ne doit être définie pour MFSampleExtension Encryption CryptByteBlock et [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md). [ \_ \_](mfsampleextension-encryption-cryptbyteblock.md)

Si le **champ \_ type de schéma** dans un fichier MP4, ou Stream, a la valeur’cens’ou’CBCS', l’attribut **MFSampleExtension \_ Encryption \_ ProtectionScheme** doit être défini sur le **modèle de protection \_ \_ AES \_ CTR** ou **protection \_ Scheme \_ CBC**, respectivement, et MFSampleExtension Encryption CryptByteBlock et [MFSampleExtension \_ Encryption \_](mfsampleextension-encryption-skipbyteblock.md) SkipByteBlock doit être défini à l’aide des valeurs de la zone « tenc ». [ \_ \_](mfsampleextension-encryption-cryptbyteblock.md)

## <a name="examples"></a>Exemples

L’exemple suivant montre comment définir le **\_ \_ ProtectionScheme** de chiffrement MFSampleExtension et les attributs de chiffrement **MFSampleExtension \_ \_ CryptByteBlock** et **MFSampleExtension \_ \_** de chiffrement associés.


```C++
HRESULT AddEncryptionAttributes(_In_ IMFSample* pSample, _In_ bool fIsEncrypted)
{
      HRESULT hr = S_OK;

      if (fIsEncrypted)
    {
        //Set Encryption Protection Scheme
        hr = pSample->UINT32(MFSampleExtension_Encryption_ProtectionScheme,
            SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC);
            if (FAILED(hr))
                return hr;

        //Set the Initialization Vector (IV)
  //(spSampleEncryptionData is omitted from this example for simplicity.) 
        hr = pSample->SetBlob(MFSampleExtension_Encryption_SampleID, 
            (BYTE*)(spSampleEncryptionData->m_pInitializationVector),
            spSampleEncryptionData->m_bIVSize);
            if (FAILED(hr))
                return hr;

        //Set crypt and skip byte blocks for pattern encryption
        hr = pSample->SetUINT32(MFSampleExtension_Encryption_CryptByteBlock, 1);
            if (FAILED(hr))
                return hr;

        hr = pSample->SetUINT32(MFSampleExtension_Encryption_SkipByteBlock, 9);
            if (FAILED(hr))
                return hr;
    }
      return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
