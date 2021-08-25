---
description: Définit l’ID de clé de l’exemple.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: Attribut MFSampleExtension_Content_KeyID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38498665dddaed0cd38082246f61f0f86c9b1b7a1e8cec7d19d476c860fe8d6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848169"
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
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[MFSampleExtension de \_ chiffrement \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




