---
description: Les transformations sécurisées-chemin d’accès complet doivent avoir une source située dans le chemin d’accès complet spécifié dans la propriété transformations.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Sécuriser-transformations de chemin d’accès complet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f55e16f40d99deceb8b625297cf447ebf5ec7dfb14a25518554804cf35b572e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040899"
---
# <a name="secure-full-path-transforms"></a>Sécuriser-transformations de chemin d’accès complet

Les transformations sécurisées-chemin d’accès complet doivent avoir une source située dans le chemin d’accès complet spécifié dans la propriété [**TRANSformations**](transforms.md) . Lorsque le package est installé ou publié, le programme d’installation enregistre les transformations dans un cache où, sur un système de fichiers sécurisé, l’utilisateur ne dispose pas d’un accès en écriture. Si la copie locale de la transformation devient indisponible, elle peut uniquement restaurer le cache à l’aide du chemin d’accès spécifié. La suppression d’un produit par un utilisateur supprime toutes les transformations sécurisées pour ce produit de l’ordinateur de l’utilisateur.

Pour appliquer des transformations sécurisées-chemins d’accès complets lors de l’installation d’un package, définissez la [stratégie TransformsSecure](transformssecure-policy.md) ou la propriété [**TransformsSecure**](transformssecure.md) ou faites \| passer le premier caractère dans la liste transformer. Les chemins d’accès complets à la source de chaque transformation doivent être passés dans la chaîne transformations. Si des chemins d’accès relatifs se trouvent dans la liste, l’installation échoue. La source de la transformation ne doit pas être localisée avec la source du package.

 

 



