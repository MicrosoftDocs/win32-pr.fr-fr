---
description: Définit l’ID de clé de l’exemple.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: Attribut MFSampleExtension_Content_KeyID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524585"
---
# <a name="mfsampleextension_content_keyid-attribute"></a>\_ \_ Attribut KeyId content MFSampleExtension

Définit l’ID de clé de l’exemple.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="examples"></a>Exemples

L’exemple suivant montre comment définir l’ID de clé de l’exemple.


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[MFSampleExtension de \_ chiffrement \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




