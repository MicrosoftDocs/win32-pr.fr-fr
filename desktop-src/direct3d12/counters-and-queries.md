---
title: Compteurs, requêtes et prédicats
description: La sortie de flux et les compteurs UAV fonctionnent dans Direct3D 12 dans une méthode similaire à Direct3D 11, bien que la mémoire pour les compteurs doive être allouée par l’application, le pilote ne le fait pas.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404350"
---
# <a name="counters-queries-and-predication"></a>Compteurs, requêtes et prédicats

Cette rubrique traite des compteurs de flux de sortie, des compteurs UAV, des requêtes et des prédicats.

La sortie de flux et les compteurs UAV fonctionnent dans Direct3D 12 dans une méthode similaire à Direct3D 11, bien que la mémoire pour les compteurs doive être allouée par l’application, le pilote ne le fait pas. Les requêtes dans Direct3D 12 sont plus différentes de celles de Direct3D 11, avec l’ajout de clôtures et d’autres processus qui éliminent le besoin de certains types de requêtes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                           | Description                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Compteurs de sortie de flux](stream-output-counters.md)<br/> | La sortie de flux est la capacité du GPU à écrire des vertex dans une mémoire tampon. Les compteurs de sortie de flux surveillent la progression.<br/>                                                               |
| [Compteurs UAV](uav-counters.md)<br/>                     | Les compteurs UAV peuvent être utilisés pour associer un compteur atomique 32 bits à un mode d’accès non ordonné (UAV).<br/>                                                                                |
| [Requêtes](queries.md)<br/>                               | Dans Direct3D 12, les requêtes sont regroupées en tableaux de requêtes appelé segment de requête. Un segment de mémoire de requête a un type qui définit les types de requêtes valides qui peuvent être utilisés avec ce tas.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mesure des performances](performance-measurement.md)
</dt> </dl>

 

 





