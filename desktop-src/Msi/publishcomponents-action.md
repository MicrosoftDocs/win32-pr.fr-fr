---
description: L’action PublishComponents gère la publication des composants à partir de la table PublishComponent.
ms.assetid: 58d945d7-7dfb-4752-ae19-7e41caca1de7
title: Action PublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c8967e737193922a9dbc3d9e03bc95131d5a63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009730"
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



 

## <a name="remarks"></a>Notes

L’action PublishComponents publie tous les composants de la table PublishComponents qui appartiennent aux fonctionnalités sélectionnées pour la publication ou l’installation.

 

 



