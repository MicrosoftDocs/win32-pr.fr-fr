---
description: Cette section décrit les structures de module de reconnaissance.
ms.assetid: 4c17391f-7af4-42ab-b77f-e3c39cadc0b6
title: Structures de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addaccf3e69f35b99379710d681fe8ac45559ea1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411460"
---
# <a name="recognizer-structures"></a>Structures de reconnaissance

Cette section décrit les structures de module de reconnaissance.

## <a name="in-this-section"></a>Dans cette section



| Structure                                                    | Description                                                                                                                                                   |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**plage de caractères \_**](/windows/win32/api/rectypes/ns-rectypes-character_range)                  | Spécifie une plage de points Unicode (caractères).<br/>                                                                                                  |
| [**\_métriques de treillis**](/windows/win32/api/rectypes/ns-rectypes-lattice_metrics)                  | Décrit la ligne de base et la hauteur de la ligne médiane.<br/>                                                                                                     |
| [**SEGMENT de ligne \_**](/windows/win32/api/rectypes/ns-rectypes-line_segment)                        | Décrit les points de début et de fin d’un segment de reconnaissance de ligne, tels que la ligne de base ou la ligne médiane.<br/>                                                 |
| [**Description du paquet \_**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)            | Décrit le contenu du paquet pour un contexte de tablette particulier.<br/>                                                                               |
| [**PACKET, \_ propriété**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)                  | Décrit une propriété de paquet qui est signalée par le pilote de tablette.<br/>                                                                                 |
| [**\_métriques de propriété**](/windows/desktop/api/tpcshrd/ns-tpcshrd-property_metrics)                | Définit la plage et la résolution d’une propriété de paquet.<br/>                                                                                             |
| [**é \_ ATTRS**](/windows/win32/api/rectypes/ns-rectypes-reco_attrs)                            | Récupère les attributs d’un module de reconnaissance ou spécifie les attributs à utiliser lors de la recherche d’un module de reconnaissance installé.<br/>                         |
| [**\_Guide é**](/windows/win32/api/rectypes/ns-rectypes-reco_guide)                            | Définit les limites de l’encre pour le module de reconnaissance.<br/>                                                                                               |
| [**\_treillis é**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)                        | Sert de point d’entrée dans un treillis.<br/>                                                                                                          |
| [**\_colonne de treillis é \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)         | Représente une colonne dans le treillis.<br/>                                                                                                                |
| [**\_élément de treillis é \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)       | Correspond à un mot ou un caractère d’Extrême-Orient, en général ; Toutefois, un élément peut également correspondre à un mouvement, une forme ou un autre code.<br/> |
| [**\_Propriétés du treillis é \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties) | Contient un tableau de pointeurs vers les structures de propriété.<br/>                                                                                              |
| [**\_propriété de treillis é \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)     | Contient une propriété utilisée dans le treillis.<br/>                                                                                                           |
| [**\_plage é**](/windows/win32/api/rectypes/ns-rectypes-reco_range)                            | Identifie une plage de caractères dans la chaîne de résultat.<br/>                                                                                             |
| [**plage de traits \_**](/windows/win32/api/tpcshrd/ns-tpcshrd-stroke_range)                        | Spécifie une plage de traits dans l’objet [**InkDisp**](inkdisp-class.md) .<br/>                                                                       |



 

 

 




