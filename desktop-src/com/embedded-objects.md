---
title: Objets incorporés (COM)
description: Objets incorporés
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193020"
---
# <a name="embedded-objects-com"></a>Objets incorporés (COM)

Un objet incorporé est stocké physiquement dans le document composé, ainsi que toutes les informations nécessaires pour gérer l’objet. En d’autres termes, l’objet incorporé fait partie du document composé dans lequel il réside. Cette configuration présente quelques inconvénients. Tout d’abord, un document composé contenant des objets incorporés est plus grand que l’autre contenant les mêmes objets que les liens. Deuxièmement, les modifications apportées à la source d’un objet incorporé ne sont pas automatiquement répliquées dans la copie incorporée, et les modifications apportées à la copie incorporée ne sont pas reflétées dans la source, comme c’est le cas avec un lien.

Toutefois, dans certains cas, l’incorporation offre plusieurs avantages par rapport aux liens. Tout d’abord, les utilisateurs peuvent transférer des documents composés avec des objets incorporés vers d’autres ordinateurs ou d’autres emplacements sur le même ordinateur, sans rompre de lien. Deuxièmement, les utilisateurs peuvent modifier des objets incorporés sans modifier le contenu de l’original. Parfois, cette séparation est précisément ce qui est nécessaire. Troisièmement, les objets incorporés peuvent être activés sur place, ce qui signifie que l’utilisateur peut modifier ou manipuler l’objet sans avoir à travailler dans une fenêtre distincte de celle du conteneur de l’objet. Au lieu de cela, lorsque l’objet est activé, l’interface utilisateur de l’application conteneur change pour exposer les outils nécessaires à la gestion ou à la modification de l’objet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’objets liés et incorporés à partir de données existantes](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




