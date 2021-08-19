---
description: Les \_ constantes d’indicateur de bit LINECALLSELECT décrivent les appels à sélectionner.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: Constantes LINECALLSELECT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaa76ea5b421b8090f9289431bfee65be61a6b47abd170569beff73a9846533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003147"
---
# <a name="linecallselect_-constants"></a>\_Constantes LINECALLSELECT

Les constantes d’indicateur de bit **LINECALLSELECT \_** décrivent les appels à sélectionner.

<dl> <dt>

<span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**\_adresse LINECALLSELECT**
</dt> <dd> <dl> <dt>



Sélectionne l’appel sur l’adresse spécifiée.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**\_appel LINECALLSELECT**
</dt> <dd> <dl> <dt>



Sélectionne les appels associés à l’appel spécifié. Par exemple, les tiers d’une conférence appellent.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT \_ CALLID**
</dt> <dd> <dl> <dt>



Sélectionne les appels associés à l’identificateur d’appel spécifié. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT \_ DEVICEID**
</dt> <dd> <dl> <dt>



Sélectionne des appels sur l’identificateur de périphérique spécifié. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,1 ou supérieure. Les applications doivent envisager l’utilisation \_ de la constante de ligne LINECALLSELECT au lieu de celle-ci.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**\_ligne LINECALLSELECT**
</dt> <dd> <dl> <dt>



Sélectionne des appels sur le périphérique de ligne spécifié.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

Cette constante est utilisée dans [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) et pour spécifier une sélection (portée) des appels qui sont demandés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




