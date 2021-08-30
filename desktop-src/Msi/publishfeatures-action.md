---
description: L’action PublishFeatures écrit l’état de chaque fonctionnalité dans le registre système.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Action PublishFeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6451b3676c5927ef1659108cc3559865fff921bdf48961ce5827a10f405109f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129029"
---
# <a name="publishfeatures-action"></a>Action PublishFeatures

L’action PublishFeatures écrit l’état de chaque fonctionnalité dans le registre système. L’état de la fonctionnalité peut être absent, publié ou installé. L’action PublishFeatures écrit également le mappage du composant de fonctionnalité dans le registre système pour chaque fonctionnalité installée.

L’action PublishFeatures interroge la table [FeatureComponents](featurecomponents-table.md), la table des [fonctionnalités](feature-table.md)et la [table des composants](component-table.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action PublishFeatures doit précéder [PublishProduct](publishproduct-action.md).

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action        |
|-------|-----------------------------------|
| \[1\] | Identificateur de la fonctionnalité publiée. |



 

## <a name="remarks"></a>Remarques

L’action PublishFeatures publie la composition de toutes les fonctionnalités sélectionnées pour être publiées ou installées.

 

 



