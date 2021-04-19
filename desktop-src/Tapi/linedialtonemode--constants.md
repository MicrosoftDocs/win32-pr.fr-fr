---
description: Les \_ constantes d’indicateur de bit LINEDIALTONEMODE décrivent différents types de tonalités. Une tonalité spéciale comporte généralement une signification particulière (comme avec le message en attente).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: Constantes LINEDIALTONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539563"
---
# <a name="linedialtonemode_-constants"></a>\_Constantes LINEDIALTONEMODE

Les constantes d’indicateur de bit **LINEDIALTONEMODE \_** décrivent différents types de tonalités. Une tonalité spéciale comporte généralement une signification particulière (comme avec le message en attente).

<dl> <dt>

<span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ externe**
</dt> <dd> <dl> <dt>



Il s’agit d’une tonalité externe (réseau public).


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ interne**
</dt> <dd> <dl> <dt>



Il s’agit d’une tonalité interne, comme dans un PBX.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ normal**
</dt> <dd> <dl> <dt>



Il s’agit d’une tonalité normale, qui est généralement une tonalité continue.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ spécial**
</dt> <dd> <dl> <dt>



Il s’agit d’une tonalité spéciale indiquant qu’une certaine condition (connue par le commutateur ou le réseau) est actuellement en vigueur. Les tonalités spéciales utilisent généralement un ton interrompu. Comme avec une tonalité normale, cela indique que le commutateur est prêt à recevoir le numéro à composer.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE \_ INdispo**
</dt> <dd> <dl> <dt>



Le mode de tonalité n’est pas disponible et ne devient pas connu.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ inconnu**
</dt> <dd> <dl> <dt>



Le mode de tonalité n’est pas actuellement connu, mais peut devenir connu ultérieurement.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil. Les 16 bits de poids faible sont réservés.

Les **\_ constantes LINEDIALTONEMODE** sont utilisées dans la structure de données [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) pour un appel dans l’état de la tonalité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




