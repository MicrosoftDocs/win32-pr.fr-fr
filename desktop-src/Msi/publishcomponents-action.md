---
description: L’action PublishComponents gère la publication des composants à partir de la table PublishComponent.
ms.assetid: 58d945d7-7dfb-4752-ae19-7e41caca1de7
title: Action PublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4840035677effff22189c357ad881c9abf2c061b169e4283037ca83df19347d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913119"
---
# <a name="publishcomponents-action"></a>Action PublishComponents

L’action PublishComponents gère la publication des composants à partir de la table [PublishComponent](publishcomponent-table.md) .

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID représentant l’ID de composant d’une fonctionnalité publiée. |
| \[2\] | Qualificateur de l’ID du composant.                                   |



 

## <a name="remarks"></a>Remarques

L’action PublishComponents publie tous les composants de la table PublishComponents qui appartiennent aux fonctionnalités sélectionnées pour la publication ou l’installation.

 

 



