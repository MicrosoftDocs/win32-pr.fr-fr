---
description: Les \_ constantes d’indicateur de bit LINEANSWERMODE décrivent comment un appel actif existant sur un appareil de ligne est affecté en répondant à un autre appel d’offre sur la même ligne.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: Constantes LINEANSWERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfb9d6491864f5be8788575d718e42cc5f5c7c337fd046c110bd5bd82eae110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761841"
---
# <a name="lineanswermode_-constants"></a>\_Constantes LINEANSWERMODE

Les constantes d’indicateur de bit **LINEANSWERMODE \_** décrivent comment un appel actif existant sur un appareil de ligne est affecté en répondant à un autre appel d' *offre* sur la même ligne.

<dl> <dt>

<span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE \_ Drop**
</dt> <dd> <dl> <dt>



L’appel actuellement actif est automatiquement supprimé.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE \_ conserver**
</dt> <dd> <dl> <dt>



L’appel actuellement actif sera automatiquement mis en attente.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ aucun**
</dt> <dd> <dl> <dt>



La réponse à un autre appel sur la même ligne n’a aucun effet sur l’appel actif existant sur la ligne.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

Si un appel arrive (est offert) au moment où un autre appel est déjà actif, le nouvel appel est connecté à en appelant [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer). L’effet de cette action sur l’appel actif existant dépend des fonctionnalités de l’appareil de la ligne. Le premier appel peut ne pas être affecté, il peut être automatiquement supprimé ou placé automatiquement en attente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




