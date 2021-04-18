---
description: Spécifie la vitesse de transmission moyenne, en bits par seconde, utilisée pour l’encodage à 2 passes, variable-bit-rate (VBR).
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: MFPKEY_RAVG, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519641"
---
# <a name="mfpkey_ravg-property"></a>MFPKEY \_ propriété RAVG

Spécifie la vitesse de transmission moyenne, en bits par seconde, utilisée pour l’encodage à 2 passes, variable-bit-rate (VBR).

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCAvgBitrate g

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Notes

Dans les deux cas, cette valeur correspond à la vitesse de transmission moyenne sur toute la durée du contenu.

Vous devez définir cette valeur pour les deux modes d’encodage VBR en deux passes. Une fois que vous avez commencé le traitement des exemples, vous ne devez pas interroger cette valeur tant que vous n’avez pas terminé d’encoder le flux. L’encodeur interprète une demande pour cette valeur comme un signal indiquant que la session d’encodage est terminée ; l’exemple suivant que vous traitez est traité comme le début d’une nouvelle session.

Cette propriété peut également être lue à la fin d’une session d’encodage VBR à 1 passage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




