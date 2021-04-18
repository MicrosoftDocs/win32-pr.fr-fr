---
title: Indicateurs d’affichage
description: Utilisez les indicateurs d’affichage pour contrôler les vues de table de routage.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509407"
---
# <a name="view-flags"></a>Indicateurs d’affichage

Utilisez les indicateurs d’affichage pour contrôler les vues de table de routage.



| Constante                 | Valeur      | Description                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| \_taille maximale de l' \_ adresse RTM \_ | 16         | Taille maximale d’adresse pour une famille d’adresses.                          |
| \_vues maximales RTM \_          | 32         | Nombre maximal de vues qui peuvent être actives dans la table de routage. |
| \_ID de vue RTM \_ \_ UCAST     | 0          | Spécifie une vue de monodiffusion.                                        |
| \_ID de vue RTM \_ \_ mcast     | 1          | Spécifie une vue de multidiffusion.                                      |
| \_taille du \_ masque de vue RTM \_    | 0x20       | Spécifie le nombre maximal de vues qui peuvent être configurées.    |
| \_masque de vue RTM \_ \_ aucun    | 0x00000000 | Retourne les informations indépendamment de la vue.                      |
| \_ \_ masque de vue RTM \_ any     | 0x00000000 | Retourne les destinations de toutes les vues. Il s’agit de la valeur par défaut.  |
| \_masque de vue RTM \_ \_ UCAST   | 0x00000001 | Retourne les destinations de la vue monodiffusion.                      |
| \_masque de vue RTM \_ \_ mcast   | 0x00000002 | Retourne les destinations de la vue multidiffusion.                    |
| affichage RTM- \_ \_ Masquer \_ tout     | Égale | Retourne des informations de toutes les vues.                              |



 

 

 




