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
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a><span data-ttu-id="8e0a1-103">\_Attribut ProtectionScheme de chiffrement MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="8e0a1-103">MFSampleExtension\_Encryption\_ProtectionScheme attribute</span></span>

<span data-ttu-id="8e0a1-104">Spécifie le schéma de protection pour les exemples chiffrés.</span><span class="sxs-lookup"><span data-stu-id="8e0a1-104">Specifies the protection scheme for encrypted samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="8e0a1-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="8e0a1-105">Data type</span></span>

<span data-ttu-id="8e0a1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8e0a1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8e0a1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8e0a1-107">Remarks</span></span>

<span data-ttu-id="8e0a1-108">La valeur de cet attribut est un membre de l’énumération [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) .</span><span class="sxs-lookup"><span data-stu-id="8e0a1-108">The value of this attribute is a member of the [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) enumeration.</span></span> <span data-ttu-id="8e0a1-109">Dans les cas où la source du média est MP4, la valeur est définie en fonction de la valeur du **champ \_ type de schéma** dans la zone type de schéma (« SCHM ») dans l’en-tête MP4 (« Moov » ou « moof »).</span><span class="sxs-lookup"><span data-stu-id="8e0a1-109">In cases where the media source is MP4-based, the value is set based off the value of the **scheme\_type** field within the scheme type box (‘schm’) in the MP4 header (‘moov’ or ‘moof’).</span></span>

<span data-ttu-id="8e0a1-110">Si le **champ \_ type de schéma** dans un fichier MP4, ou Stream, a la valeur’Cenc’ou’CBC1 ', l’attribut **MFSampleExtension \_ Encryption \_ ProtectionScheme** doit être défini sur le **modèle de protection \_ \_ AES \_ CTR** ou **protection \_ Scheme \_ CBC**, respectivement, et aucune valeur ne doit être définie pour MFSampleExtension Encryption CryptByteBlock et [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md). [ \_ \_](mfsampleextension-encryption-cryptbyteblock.md)</span><span class="sxs-lookup"><span data-stu-id="8e0a1-110">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cenc’ or ‘cbc1’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and no values should be set for [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).</span></span>

<span data-ttu-id="8e0a1-111">Si le **champ \_ type de schéma** dans un fichier MP4, ou Stream, a la valeur’cens’ou’CBCS', l’attribut **MFSampleExtension \_ Encryption \_ ProtectionScheme** doit être défini sur le **modèle de protection \_ \_ AES \_ CTR** ou **protection \_ Scheme \_ CBC**, respectivement, et MFSampleExtension Encryption CryptByteBlock et [MFSampleExtension \_ Encryption \_](mfsampleextension-encryption-skipbyteblock.md) SkipByteBlock doit être défini à l’aide des valeurs de la zone « tenc ». [ \_ \_](mfsampleextension-encryption-cryptbyteblock.md)</span><span class="sxs-lookup"><span data-stu-id="8e0a1-111">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cens’ or ‘cbcs’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) must be set using the values in the ‘tenc’ box.</span></span>

## <a name="examples"></a><span data-ttu-id="8e0a1-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="8e0a1-112">Examples</span></span>

<span data-ttu-id="8e0a1-113">L’exemple suivant montre comment définir le **\_ \_ ProtectionScheme** de chiffrement MFSampleExtension et les attributs de chiffrement **MFSampleExtension \_ \_ CryptByteBlock** et **MFSampleExtension \_ \_** de chiffrement associés.</span><span class="sxs-lookup"><span data-stu-id="8e0a1-113">The following example shows how to set the **MFSampleExtension\_Encryption\_ProtectionScheme** and the associated **MFSampleExtension\_Encryption\_CryptByteBlock** and **MFSampleExtension\_Encryption\_SkipByteBlock** attributes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8e0a1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e0a1-114">Requirements</span></span>



| <span data-ttu-id="8e0a1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e0a1-115">Requirement</span></span> | <span data-ttu-id="8e0a1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e0a1-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e0a1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e0a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8e0a1-118">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e0a1-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8e0a1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e0a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8e0a1-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e0a1-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="8e0a1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e0a1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e0a1-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e0a1-122"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
