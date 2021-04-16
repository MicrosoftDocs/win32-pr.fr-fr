---
description: L’action UnpublishComponents gère la désannonce des composants listés dans la table PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Action UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104394039"
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



 

