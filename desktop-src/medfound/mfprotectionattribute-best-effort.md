---
description: Défini en tant qu’attribut pour un objet IMFOutputSchema.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: Attribut MFPROTECTIONATTRIBUTE_BEST_EFFORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202257"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a>\_Attribut de meilleur \_ effort MFPROTECTIONATTRIBUTE

Défini en tant qu’attribut pour un objet [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) . Si cet attribut est présent, l’échec d’une tentative d’application de la protection est ignoré. Si la valeur de l’attribut associé est **true**, le schéma de protection avec l’attribut de [ \_ \_ basculement MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) doit être appliqué.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Si la **valeur est true**, applique le schéma de protection avec l’attribut de [ \_ basculement MFPROTECTIONATTRIBUTE en \_](mfprotectionattribute-fail-over.md) cas d’échec de la définition de cette protection.

Défini en tant qu’attribut pour un objet [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications UWP Windows 8 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications UWP Windows Server 2012 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




