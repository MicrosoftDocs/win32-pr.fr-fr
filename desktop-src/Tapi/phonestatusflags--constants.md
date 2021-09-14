---
description: Les \_ constantes d’indicateur de bit PHONESTATUSFLAGS décrivent une variété d’informations sur l’état des appareils téléphoniques.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: Constantes PHONESTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095666"
---
# <a name="phonestatusflags_-constants"></a>\_Constantes PHONESTATUSFLAGS

Les constantes d’indicateur de bit **PHONESTATUSFLAGS \_** décrivent une variété d’informations sur l’état des appareils téléphoniques.

<dl> <dt>

<span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ connecté**
</dt> <dd> <dl> <dt>



Spécifie si le téléphone est actuellement connecté à l’interface TAPI. **True** si connecté ; sinon, **false** .


</dt> </dl> </dd> <dt>

<span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS \_ suspendu**
</dt> <dd> <dl> <dt>



Spécifie si la manipulation de l’appareil téléphonique par l’interface TAPI est suspendue. **True** si l’interruption est suspendue ; sinon, **false** . L’utilisation d’un appareil téléphonique par une application peut être temporairement suspendue quand le commutateur souhaite manipuler le téléphone de manière à ne pas tolérer les interférences de l’application.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




