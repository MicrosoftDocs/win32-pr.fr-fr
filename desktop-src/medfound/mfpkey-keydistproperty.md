---
description: Spécifie la durée maximale, en millisecondes, entre les images clés de la sortie du codec.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: MFPKEY_KEYDIST, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864153"
---
# <a name="mfpkey_keydist-property"></a>MFPKEY, \_ propriété de KEYdist

Spécifie la durée maximale, en millisecondes, entre les images clés de la sortie du codec.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCKeyframeDistance g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

La valeur par défaut dépend de la version de Windows en cours d’exécution, comme indiqué dans le tableau suivant.



| Système d’exploitation | Valeur par défaut |
|------------------|---------------|
| Windows XP       | 8000          |
| Windows Vista    | 8000          |
| Windows 7        | 2000          |



 

## <a name="remarks"></a>Notes

La logique interne du codec détermine l’emplacement réel de chaque image clé. La distance entre deux images clés quelconques peut être inférieure à la valeur de cette propriété, mais elle ne sera jamais supérieure.

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

 

 




