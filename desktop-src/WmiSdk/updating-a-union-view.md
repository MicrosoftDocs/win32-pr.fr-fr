---
description: Vous pouvez mettre à jour les valeurs des propriétés non-clés des instances de classe de vue Union. Les modifications que vous apportez à l’instance de la classe de vue seront propagées vers les instances de la classe source qui forment la classe d’affichage Union.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Mise à jour d’une vue Union
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114843"
---
# <a name="updating-a-union-view"></a>Mise à jour d’une vue Union

Vous pouvez mettre à jour les valeurs des propriétés non-clés des instances de classe de vue Union. Les modifications que vous apportez à l’instance de la classe de vue seront propagées vers les instances de la classe source qui forment la classe d’affichage Union.

Les restrictions suivantes s’appliquent aux modifications apportées aux instances de classe de vue :

-   Vous ne pouvez pas créer de nouvelles instances de classes d’affichage.
-   Seules les classes d’Union prennent en charge les mises à jour ; les vues de jointure et d’association créent des instances de vue en lecture seule.
-   La réussite d’une mise à jour varie selon qu’une instance source peut être mise à jour ou non. Si une propriété d’instance de vue est mappée à une propriété en lecture seule d’une instance source, les tentatives de modification de la propriété de vue échouent.

 

 



