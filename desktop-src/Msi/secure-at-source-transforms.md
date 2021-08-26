---
description: Les transformations sécurisées à la source doivent avoir une source située à la racine de la source du package.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Transformations sécurisées à la source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f591e6f30c11ec9fa7edf2f943ef1f660a0a3b12ff87c3c1de0984328652565b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040999"
---
# <a name="secure-at-source-transforms"></a>Transformations sécurisées à la source

Les transformations sécurisées à la source doivent avoir une source située à la racine de la source du package. Lorsque le package est installé ou publié, le programme d’installation enregistre les transformations dans un cache où, sur un système de fichiers sécurisé, l’utilisateur ne dispose pas d’un accès en écriture. Si la copie locale de la transformation devient indisponible, le programme d’installation recherche une source pour restaurer le cache. La méthode est identique à la recherche d’un fichier .msi dans la liste source. Pour plus d’informations, consultez [résilience source](source-resiliency.md). La suppression d’un produit par un utilisateur supprime toutes les transformations sécurisées pour ce produit de l’ordinateur de l’utilisateur.

Pour appliquer des transformations sécurisées au niveau de la source lors de l’installation d’un package, définissez la [stratégie TransformsSecure](transformssecure-policy.md) ou la propriété [**TransformsSecure**](transformssecure.md) , ou faites de @ le premier caractère transmis dans la liste transformer. Chaque transformation doit être indiquée par un nom de fichier et doit se trouver à la racine de la source du package. Si l’une des transformations ne se trouve pas à la racine de la source du package, l’installation échoue. Pour plus d’informations, consultez [application de transformations](applying-transforms.md).

 

 



