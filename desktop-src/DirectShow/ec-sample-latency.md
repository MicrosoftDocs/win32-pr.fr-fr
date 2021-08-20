---
description: Spécifie la distance de planification d’un composant pour les exemples de traitement.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612c553916dc19685224bb512f6627363dba439883553d82c59f153324f5eda7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686149"
---
# <a name="ec_sample_latency"></a>latence de l' \_ exemple EC \_

Spécifie la distance de planification d’un composant pour les exemples de traitement.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const Reference \_ Time** \* ) à l’arrière-plan du composant, en unités de 100 nanosecondes. Si cette valeur est positive, le composant est en arrière-plan. Si cette valeur est négative, le composant est en avance sur Schedule.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="remarks"></a>Notes

Un présentateur personnalisé pour le filtre EVR ( [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) ) peut envoyer ce message à EVR, pour informer le EVR si le présenteur est en retard ou en avance sur la planification.

La façon la plus simple de calculer *lParam1* est la suivante : *QPC maintenant*   *QPC Target*, où *QPC* est désormais l’heure de l’horloge, et *QPC Target* est l’heure de la présentation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Comment écrire un présentateur EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

