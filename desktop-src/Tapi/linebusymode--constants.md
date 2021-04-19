---
description: Les \_ constantes d’indicateur de bit LINEBUSYMODE décrivent différents signaux occupés que le commutateur ou le réseau peuvent générer. Ces signaux occupés indiquent généralement qu’une ressource différente requise pour effectuer un appel est en cours d’utilisation.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: Constantes LINEBUSYMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c996ad4e6142cc8312983945ae4c716ee0b35ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535396"
---
# <a name="linebusymode_-constants"></a>\_Constantes LINEBUSYMODE

Les constantes d’indicateur de bit **LINEBUSYMODE \_** décrivent différents signaux occupés que le commutateur ou le réseau peuvent générer. Ces signaux occupés indiquent généralement qu’une ressource différente requise pour effectuer un appel est en cours d’utilisation.

<dl> <dt>

<span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**\_station LINEBUSYMODE**
</dt> <dd> <dl> <dt>



Le signal occupé indique que la station du tiers appelé est occupée. Cela est généralement signalé par un ton occupé *normal* .


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE \_ Trunk**
</dt> <dd> <dl> <dt>



Le signal occupé indique qu’un Trunk ou un circuit est occupé. Ce nombre est généralement signalé *par une tonalité à forte activité* .


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ inconnu**
</dt> <dd> <dl> <dt>



Le mode spécifique du signal occupé est actuellement inconnu, mais peut devenir connu ultérieurement.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE \_ INdispo**
</dt> <dd> <dl> <dt>



Le mode spécifique du signal occupé n’est pas disponible et ne sera pas connu.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil. Les 16 bits de poids faible sont réservés.

> [!Note]  
> Les signaux occupés peuvent être envoyés en tant que tonalités inbandes ou messages hors bande. L’interface TAPI ne fait aucune hypothèse sur le mécanisme de signalisation spécifique.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




