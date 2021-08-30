---
description: Vous pouvez mettre à jour les valeurs des propriétés non-clés des instances de classe de vue Union. Les modifications que vous apportez à l’instance de la classe de vue seront propagées vers les instances de la classe source qui forment la classe d’affichage Union.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Mise à jour d’une vue Union
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7061181971a6f97a0bbde0992b64a8bdb3be8c7441fb4e90cb8fdcd0d675a221
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030329"
---
# <a name="updating-a-union-view"></a>Mise à jour d’une vue Union

Vous pouvez mettre à jour les valeurs des propriétés non-clés des instances de classe de vue Union. Les modifications que vous apportez à l’instance de la classe de vue seront propagées vers les instances de la classe source qui forment la classe d’affichage Union.

Les restrictions suivantes s’appliquent aux modifications apportées aux instances de classe de vue :

-   Vous ne pouvez pas créer de nouvelles instances de classes d’affichage.
-   Seules les classes d’Union prennent en charge les mises à jour ; les vues de jointure et d’association créent des instances de vue en lecture seule.
-   La réussite d’une mise à jour varie selon qu’une instance source peut être mise à jour ou non. Si une propriété d’instance de vue est mappée à une propriété en lecture seule d’une instance source, les tentatives de modification de la propriété de vue échouent.

 

 



