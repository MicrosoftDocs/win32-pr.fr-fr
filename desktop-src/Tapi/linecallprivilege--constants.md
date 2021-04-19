---
description: Les \_ constantes d’indicateur de bit LINECALLPRIVILEGE décrivent les types de droits d’accès ou de privilèges qu’une application avec un descripteur d’appel peut avoir pour l’appel correspondant.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: Constantes LINECALLPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534890"
---
# <a name="linecallprivilege_-constants"></a>\_Constantes LINECALLPRIVILEGE

Les constantes d’indicateur de bit **LINECALLPRIVILEGE \_** décrivent les types de droits d’accès ou de privilèges qu’une application avec un descripteur d’appel peut avoir pour l’appel correspondant.

<dl> <dt>

<span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**\_moniteur LINECALLPRIVILEGE**
</dt> <dd> <dl> <dt>



L’application dispose des privilèges d’analyse pour l’appel. Ces privilèges permettent à l’application de surveiller les modifications d’État et les informations de requête et l’état de l’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ aucun**
</dt> <dd> <dl> <dt>



L’application n’a aucun privilège pour l’appel. Le descripteur de l’application est void et ne doit pas être utilisé.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**\_propriétaire LINECALLPRIVILEGE**
</dt> <dd> <dl> <dt>



L’application dispose des privilèges de propriétaire pour l’appel. Ces privilèges permettent à l’application de manipuler l’appel de manière à affecter l’état de l’appel.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Lorsqu’un descripteur d’appel est d’abord fourni à une application ou chaque fois que des privilèges d’appel de cette application sont modifiés, la [**ligne \_ CALLSTATE**](line-callstate.md) le message est envoyé à l’application. Lorsqu’une application transmet un appel et que l’application réceptrice n’a pas déjà de handle avec des privilèges de propriétaire, ce message informe l’application de ses nouveaux privilèges sur l’appel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




