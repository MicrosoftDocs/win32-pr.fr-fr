---
title: Indicateurs d’énumération
description: Indicateurs d’énumération
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Énumération
- Indicateurs d’énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa99352db877cdaef3d5297d754d1e66bb246240074cfc741ba3baff94a5d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910269"
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



 

 

 




