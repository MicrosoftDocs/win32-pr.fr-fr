---
description: Profil en mode restreint et établissement de la configuration
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Profil en mode restreint et établissement de la configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bb4d4bea3f42eaf897e781ccf859d094a0d0321815e7457aa6c79f96cb5ded
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747049"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a>Profil en mode restreint et établissement de la configuration

En raison de la variété des types de données qui peuvent être décodées par DirectX VA, ainsi que des configurations de décodage multiples prises en charge dans DirectX VA pour chacun de ces types de données (par exemple, à l’aide de mémoires tampons de flux binaire par rapport au décodage des différences résiduelles d’hôte par rapport aux IDCT basés sur des accélérateurs),  Nous pensons qu’il serait quelque peu plus simple de spécifier un GUID unique pour chaque type de données et configuration de décodage uniques. Cela créerait un grand nombre de GUID (par exemple, s’il existait 16 profils de DirectX VA et 16 configurations possibles pour chacun d’entre eux), il faudrait 256 GUID définis, ce qui nécessite 4 kilo-octets de mémoire tout simplement pour les conserver. Ce problème est la partie la plus difficile pour déterminer comment mapper DirectX VA dans **IAMVideoAccelerator**, avec le reste de la définition opérationnelle qui est généralement assez simple. Par conséquent, nous spécifions un GUID unique pour chaque type de données (pour chaque profil en mode restreint) et vous autorisez l’Association d’un GUID supplémentaire à chaque type de chiffrement. La configuration du décodage est ensuite établie entre le décodeur et l’accélérateur par une négociation subordonnée de niveau inférieur à l’aide d’opérations de détection et de verrouillage pour établir des configurations pour chaque type de fonction DirectX VA.

 

 



