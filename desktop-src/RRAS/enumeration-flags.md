---
title: Indicateurs d’énumération
description: Indicateurs d’énumération
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Énumération
- Indicateurs d’énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939973"
---
# <a name="enumeration-flags"></a>Indicateurs d’énumération



| Constante               | Valeur      | Description                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| début de l' \_ énumération RTM \_       | 0x00000000 | Énumérer les itinéraires ou les destinations à partir de 0/0.                                                                                                         |
| \_énumération RTM \_ suivante        | 0x00000001 | Énumérer les itinéraires ou les destinations à partir de la longueur d’adresse/de masque spécifiée (par exemple, 10/8). L’énumération continue jusqu’à la fin de la table de routage. |
| \_plage d’énumération RTM \_       | 0x00000002 | Énumérer les itinéraires ou les destinations dans la sous-arborescence spécifiée spécifiée par la longueur de l’adresse/du masque (par exemple, 10/8).                                            |
| \_enum RTM \_ toutes les \_ dest.  | 0x00000000 | Retourne toutes les destinations.                                                                                                                                  |
| les \_ \_ propres \_ dest enum RTM  | 0x01000000 | Retourne uniquement les destinations détenues par le client.                                                                                                      |
| \_ \_ tous les \_ itinéraires de l’enum RTM | 0x00000000 | Retourne tous les itinéraires.                                                                                                                                        |
| \_ \_ itinéraires personnalisés de la version RTM \_ | 0x00010000 | Retourne uniquement les itinéraires détenus par le client.                                                                                                            |



 

 

 




