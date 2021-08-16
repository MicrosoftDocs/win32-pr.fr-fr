---
description: Identificateur qui peut être défini sur un IMFOutputPolicy.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: MF_POLICY_ID (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1702f990dc1c88f7632bf74a40ca4671a70350450c723d4d9392af6e47dac038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740665"
---
# <a name="mf_policy_id-attribute"></a>Attribut d’ID de \_ stratégie MF \_

Identificateur qui peut être défini sur un [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy).

## <a name="data-type"></a>Type de données

**UInt32** (traité comme **bool**)

## <a name="remarks"></a>Remarques

La valeur peut être reçue à partir de l’événement de média [MEPolicySet](./mepolicyset.md) . Elle est stockée sous la forme d’une charge utile de type **VT_UI4** dans l’événement **MEPolicySet** .


## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 Mise à jour d’avril 2020   <br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>



 

 
