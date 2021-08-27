---
title: Indicateurs d’affichage
description: Utilisez les indicateurs d’affichage pour contrôler les vues de table de routage.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ae9763587cf7972aab3ca9880d5ad26350c3161955c17940484cc1cbd801bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024949"
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
| \_ \_ masque de vue RTM \_ any     | 0x00000000 | Retourne les destinations de toutes les vues. Il s'agit de la valeur par défaut.  |
| \_masque de vue RTM \_ \_ UCAST   | 0x00000001 | Retourne les destinations de la vue monodiffusion.                      |
| \_masque de vue RTM \_ \_ mcast   | 0x00000002 | Retourne les destinations de la vue multidiffusion.                    |
| affichage RTM- \_ \_ Masquer \_ tout     | 0xFFFFFFFF | Retourne des informations de toutes les vues.                              |



 

 

 




