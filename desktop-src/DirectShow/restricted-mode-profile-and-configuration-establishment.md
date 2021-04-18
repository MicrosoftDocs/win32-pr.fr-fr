---
description: Profil en mode restreint et établissement de la configuration
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Profil en mode restreint et établissement de la configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a424505b3934131527f249176f9fe0984b320a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392532"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a>Profil en mode restreint et établissement de la configuration

En raison de la variété des types de données qui peuvent être décodées par DirectX VA et des configurations de décodage multiples prises en charge dans DirectX VA pour chacun de ces types de données (par exemple, à l’aide des tampons de flux binaire par rapport au décodage des différences résiduelles de l’hôte par rapport aux IDCT basés sur des accélérateurs avec et sans chiffrement de chaque type de mémoire tampon, etc.), nous pensons qu’il serait un peu plus simple de spécifier un GUID unique pour chaque type de données et configuration de décodage uniques. Cela créerait un grand nombre de GUID (par exemple, s’il existait 16 profils de DirectX VA et 16 configurations possibles pour chacun d’entre eux), il faudrait 256 GUID définis, ce qui nécessite 4 kilo-octets de mémoire tout simplement pour les conserver. Ce problème est la partie la plus difficile pour déterminer comment mapper DirectX VA dans **IAMVideoAccelerator**, avec le reste de la définition opérationnelle qui est généralement assez simple. Par conséquent, nous spécifions un GUID unique pour chaque type de données (pour chaque profil en mode restreint) et vous autorisez l’Association d’un GUID supplémentaire à chaque type de chiffrement. La configuration du décodage est ensuite établie entre le décodeur et l’accélérateur par une négociation subordonnée de niveau inférieur à l’aide d’opérations de détection et de verrouillage pour établir des configurations pour chaque type de fonction DirectX VA.

 

 



