---
description: Identificateur qui peut être défini sur un IMFOutputPolicy.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: MF_POLICY_ID (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787195b20980164d7534bccc267781cdbb7510e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042746"
---
# <a name="mf_policy_id-attribute"></a>Attribut d’ID de \_ stratégie MF \_

Identificateur qui peut être défini sur un [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy).

## <a name="data-type"></a>Type de données

**UInt32** (traité comme **bool**)

## <a name="remarks"></a>Notes

La valeur peut être reçue à partir de l’événement de média [MEPolicySet](./mepolicyset.md) . Elle est stockée sous la forme d’une charge utile de type **VT_UI4** dans l’événement **MEPolicySet** .


## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Mise à jour 2020 de Windows 10 avril   <br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>



 

 
