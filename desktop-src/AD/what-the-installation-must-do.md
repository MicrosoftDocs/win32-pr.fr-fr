---
title: Ce que l’installation doit faire
description: Les nouveaux attributs référencés à l’étape 3 doivent être référencés par son OID, car le nouveau nom d’attribut n’est pas présent dans le cache de schéma à ce stade.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Ce que l’installation doit faire d’AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939619"
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

 

 




