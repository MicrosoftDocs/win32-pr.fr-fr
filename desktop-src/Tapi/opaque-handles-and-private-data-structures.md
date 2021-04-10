---
description: Les handles opaques sont utilisés dans TSPI pour faire référence aux structures de données qui représentent des lignes, des téléphones et des apparences d’appel.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Descripteurs opaques et structures de données privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951351"
---
# <a name="opaque-handles-and-private-data-structures"></a>Descripteurs opaques et structures de données privées

Les handles opaques sont utilisés dans TSPI pour faire référence aux structures de données qui représentent des lignes, des téléphones et des apparences d’appel. Celles-ci apparaissent en tant que paramètres de la plupart des fonctions et des rappels. Il existe peu de fonctions qui font référence à l’appareil à l’aide d’un identificateur d’appareil au lieu d’un handle opaque. Dans ce cas, la référence se rapporte à l’appareil lui-même plutôt qu’à une structure de données. Les fonctions qui fonctionnent de cette manière sont généralement celles appelées à des moments d’initialisation précoces avant la création des structures de données et l’échange des handles opaques.

Le fournisseur de services doit décider comment interpréter ces handles. Un fournisseur de services utilise généralement le pointeur vers sa structure de données ou vers l’index dans un tableau de structures de données comme handle opaque. La seule restriction est que le fournisseur de services ne peut pas utiliser la valeur 0 comme [HDRVLINE](hdrvline.md), HDRVCALL ou [HDRVPHONE](hdrvphone.md). La valeur 0 ou **null** pour un descripteur a une signification spéciale dans certaines opérations.

 

 



