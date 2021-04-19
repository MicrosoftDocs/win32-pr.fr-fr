---
description: Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) contraints à sa vitesse de transmission moyenne (spécifiée par MFPKEY \_ RAVG).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: MFPKEY_BAVG, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518228"
---
# <a name="mfpkey_bavg-property"></a>MFPKEY \_ propriété BAVG

Spécifie la fenêtre de mémoire tampon, en millisecondes, d’un flux de vitesse de transmission variable (VBR) contraints à sa vitesse de transmission moyenne (spécifiée par [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)).

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCBAvg g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

Aucune valeur par défaut, mais le codec calcule une valeur appropriée en fonction des autres paramètres VBR restreints.

## <a name="remarks"></a>Notes

Cette valeur est calculée par le codec après l’étape d’encodage finale. Vous ne devez pas interroger cette valeur tant que l’encodage n’est pas terminé. Le codec interprète une demande pour cette valeur comme un signal indiquant que la session d’encodage est terminée ; l’exemple suivant que vous traitez est traité comme le début d’une nouvelle session.

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

 

 




