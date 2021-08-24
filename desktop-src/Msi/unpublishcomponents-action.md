---
description: L’action UnpublishComponents gère la désannonce des composants listés dans la table PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Action UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1feaca4449ffa344eeda828334f879ebc12905406446dd14623e3b9c4474c6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810259"
---
# <a name="unpublishcomponents-action"></a>Action UnpublishComponents

L’action UnpublishComponents gère la désannonce des composants listés dans la table PublishComponent. Il s’agit de composants pouvant être en panne dans d’autres produits. Cette action supprime les informations sur les composants publiés de la [table PublishComponent](publishcomponent-table.md) pour laquelle la fonctionnalité correspondante est actuellement sélectionnée pour être désinstallée.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID représentant l’ID de composant d’une fonctionnalité publiée. |
| \[2\] | Qualificateur de l’ID du composant.                               |



 

