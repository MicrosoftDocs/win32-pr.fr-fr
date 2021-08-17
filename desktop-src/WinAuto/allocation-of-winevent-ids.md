---
title: Allocation d’ID WinEvent
description: Chaque WinEvent est destiné à être utilisé uniquement à des fins spécifiques. L’utilisation d’un WinEvent à des fins involontaires peut provoquer des collisions avec d’autres applications ou le système d’exploitation, ce qui peut provoquer l’instabilité des applications ou du système d’exploitation.
ms.assetid: 956d6db4-f342-4b11-bfd9-92725284223f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e877c6adcba79870d887e0bdb0d2eb9137d9e04fda4c1cc770414d0dd01f96d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326881"
---
# <a name="allocation-of-winevent-ids"></a>Allocation d’ID WinEvent

Chaque WinEvent est destiné à être utilisé uniquement à des fins spécifiques. L’utilisation d’un WinEvent à des fins involontaires peut provoquer des collisions avec d’autres applications ou le système d’exploitation, ce qui peut provoquer l’instabilité des applications ou du système d’exploitation.

Microsoft a défini plusieurs catégories différentes de WinEvents et, pour chaque catégorie, a défini une ou plusieurs plages de valeurs à utiliser en tant qu’ID WinEvent. la plage réservée Community (0xA000 — 0xAFFF) est disponible pour les applications qui doivent définir de nouvelles WinEvents. L’utilisation de valeurs de cette plage permet de réduire le risque de collisions ; Toutefois, les développeurs qui créent de nouveaux WinEvents doivent toujours collaborer pour éviter les collisions entre leurs applications.

Le tableau suivant présente les catégories WinEvent et les plages de valeurs définies pour chaque catégorie.



| Category                                                | Plage         | En cours d’utilisation | Commentaires                                                                                        |
|---------------------------------------------------------|---------------|------------------|-------------------------------------------------------------------------------------------------|
| Événements de Active Accessibility Microsoft (système réservé) | 0x0001-0x00FF | 0x0001-0x0020    | \_ID d' \_ \* événement du système d’événements                                                                     |
| Événements de Active Accessibility Microsoft (système réservé) | 0x4001-0x40FF | 0x4001-0x4007    | \_ID d' \_ \* événement de la console d’événements                                                                    |
| Événements UI Automation (système réservé)                  | 0x4E00-0x4EFF | 0x4E20-0x4E33    | ID d’événement UI Automation                                                                         |
| Événements UI Automation (système réservé)                  | 0x7500-0x75FF | 0x7530-0x759B    | ID d’événement de modification de propriété UI Automation                                                        |
| Événements de Active Accessibility Microsoft (système réservé) | 0x8000-0x80FF | 0x8000-0x8015    | \_ID d' \_ \* événement de l’objet d’événement                                                                     |
| OEM réservé                                            | 0x0101-0x01FF | 0x0101-0x0122    | ID d’événement IAccessible2                                                                          |
| Community Réservé                                      | 0xA000-0xAFFF | Aucun             | Réservé aux nouveaux événements définis par les spécifications de l’interopérabilité de l’accessibilité (AIA) |
| ATOM                                                    | 0xC000-0xFFFF | 0xC000-0xFFFF    | Réservé pour les événements personnalisés alloués au moment de l’exécution                                                 |



 

Les rubriques suivantes décrivent les plages WinEvent plus en détail.

## <a name="microsoft-active-accessibility-and-ui-automation-events"></a>Événements Microsoft Active Accessibility et UI Automation

Cinq plages d’ID WinEvent sont réservées à une utilisation par Microsoft Active Accessibility et Microsoft UI Automation. La première plage (0x0001 — 0x00FF) est réservée aux événements de niveau système, généralement utilisés pour décrire les situations qui affectent toutes les applications du système. la deuxième plage (0x4001 — 0x40FF) est réservée aux événements Windows spécifiques à la console. La troisième (0x4E00 — 0x4EFF) et la quatrième plage (0x7500, 0x75FF) sont destinées à la réflexion des événements UI Automation. Enfin, la cinquième plage (0x8000 — 0x80FF) concerne les événements de niveau objet qui se rapportent à des situations spécifiques aux objets au sein d’une même application.

Tous les événements Microsoft Active Accessibility et UI Automation sont définis dans les fichiers d’en-tête WinUser. h et UIAutomationClient. h.

## <a name="oem-reserved-events"></a>Événements réservés OEM

La plage réservée OEM est ouverte à toute personne qui a besoin d’utiliser WinEvents comme mécanisme de communication. Les développeurs doivent définir et publier des définitions d’événements avec leurs paramètres (ou également avec les types d’objets associés) pour le traitement des événements, afin que des collisions accidentelles d’ID d’événement puissent être évitées. La spécification IAccessible2 utilise une partie de la plage réservée OEM.

## <a name="community-reserved-events"></a>Community Événements réservés

la Community plage réservée est pour les WinEvents spécifiés par l’interopérabilité de l’accessibilité (AIA) pour une utilisation dans le secteur. Les développeurs sont vivement encouragés à définir et publier une spécification officielle avant d’utiliser les valeurs de cette plage.

## <a name="atom-events"></a>Événements ATOM

La plage ATOM est réservée aux ID d’événement qui sont alloués au moment de l’exécution via l’API d’extensibilité UI Automation. N’utilisez pas les valeurs de la plage ATOM à d’autres fins. L’utilisation de la fonction [**GlobalAddAtom**](/windows/desktop/api/winbase/nf-winbase-globaladdatoma) avec un GUID de chaîne est la méthode recommandée pour allouer des WinEvents à partir de la plage Atom.

## <a name="using-values-from-a-reserved-range"></a>Utilisation des valeurs d’une plage réservée

Selon la spécification WinEvent, les valeurs de la plage réservée du système, ou toute autre plage non définie, ne peuvent pas être utilisées sans révision du kit de développement logiciel (SDK). pour les nouveaux WinEvents, les applications doivent utiliser des valeurs provenant des plages réservées de l’OEM ou Community réservées. Avant d’utiliser un nouveau WinEvent, il est vivement conseillé aux développeurs de partager leurs spécifications de façon ouverte et en toute transparence, et de travailler avec l’Alliance Interoperability Interoperability pour définir des spécifications de WinEvent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Accessibility Interoperability Alliance](https://www.atia.org/)
</dt> </dl>

 

 