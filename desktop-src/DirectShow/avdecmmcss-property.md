---
description: Spécifie la classe du service Planificateur de classes multimédias (MMCSS) pour le thread de décodage.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Propriété AVDecMmcss (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9084db3cce8d555afa44097271a6b08f58cfea2f2edcb7acb5845730afc86b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159943"
---
# <a name="avdecmmcss-property"></a>Propriété AVDecMmcss

Spécifie la classe du service Planificateur de classes multimédias (MMCSS) pour le thread de décodage.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecMmcssClass**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est le nom de la classe MMCSS.

## <a name="remarks"></a>Remarques

MMCSS permet aux applications de s’assurer que le traitement qui respecte le temps a un accès prioritaire aux ressources du processeur. Il fonctionne en élevant les threads inscrits sur des priorités de thread supérieures tout en diminuant régulièrement leurs priorités afin de transmettre du temps à d’autres processus.

La valeur recommandée pour les décodeurs audio est « audio » et la valeur recommandée pour les décodeurs vidéo est « lecture ».

Si le service MMCSS n’est pas disponible ou si la classe MMCSS spécifiée n’existe pas, la définition de la propriété n’a aucun effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>UUID. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




