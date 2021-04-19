---
description: Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale (spécifiée par MFPKEY \_ rmax).
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: MFPKEY_BMAX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526943"
---
# <a name="mfpkey_bmax-property"></a>MFPKEY \_ propriété BMAX

Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) avec restriction à sa vitesse de transmission maximale (spécifiée par [MFPKEY \_ Rmax](mfpkey-rmaxproperty.md)).

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCBMax g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

Aucune valeur par défaut.

## <a name="remarks"></a>Notes

Vous devez définir cette valeur pour l’encodage VBR à limitation maximale. Une fois que vous avez commencé le traitement des exemples, vous ne devez pas interroger cette valeur tant que vous n’avez pas terminé d’encoder le flux. Le codec interprète une demande pour cette valeur comme un signal indiquant que la session d’encodage est terminée ; l’exemple suivant que vous traitez est traité comme le début d’une nouvelle session.

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

 

 




