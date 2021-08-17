---
title: Ce que l’installation doit faire
description: Les nouveaux attributs référencés à l’étape 3 doivent être référencés par son OID, car le nouveau nom d’attribut n’est pas présent dans le cache de schéma à ce stade.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Ce que l’installation doit faire d’AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3dcf125a171fba921a5341ad5f3de8bbe5d791d4eb4dc072f551345df3218ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182172"
---
# <a name="what-the-installation-must-do"></a>Ce que l’installation doit faire

Les applications qui étendent le schéma doivent appliquer les mises à jour comme décrit dans la procédure suivante.

**Pour appliquer des mises à jour lors de l’extension du schéma**

1.  Ajoutez les nouveaux attributs.
2.  Ajoutez les nouvelles classes.
3.  Ajoutez les nouveaux attributs aux classes.
4.  Déclenchez un rechargement du cache.

Les nouveaux attributs référencés à l’étape 3 doivent être référencés par son OID, car le nouveau nom d’attribut n’est pas présent dans le cache de schéma à ce stade.

L’étape 4 n’est pas nécessaire si les extensions ne seront pas utilisées immédiatement ; les extensions s’affichent dans le cache de schéma en 5 minutes environ, en fonction de la charge du système. Pour plus d’informations sur le cache de schéma et sur la façon de déclencher un rechargement de cache, consultez [mise à jour du cache de schéma](updating-the-schema-cache.md).

 

 




