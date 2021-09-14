---
title: Annexe A prise en charge des éléments de référence d’interface utilisateur
description: cette annexe contient des informations sur les éléments d’interface utilisateur fournis par Microsoft Active Accessibility dans Windows 95, Windows 98, microsoft Windows NT, Windows 2000, Windows XP et Windows serveur 2000.
ms.assetid: 5d0a81d8-5d36-4c33-bb8c-abcb8b00166e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f75cd4251ed7d75d9aa6a2d83387a51a8b157e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010715"
---
# <a name="appendix-a-supported-user-interface-elements-reference"></a>Annexe A : informations de référence sur les éléments d’interface utilisateur pris en charge

cette annexe contient des informations sur les éléments d’interface utilisateur fournis par Microsoft Active Accessibility dans Windows 95, Windows 98, microsoft Windows NT, Windows 2000, Windows XP et Windows serveur 2000. Cette prise en charge permet aux utilitaires clients d’obtenir des informations sur les éléments d’interface utilisateur fournis par le système dans les applications qui n’implémentent pas Microsoft Active Accessibility.

Oleacc.dll prend en charge les contrôles définis dans les éléments d’interface utilisateur User32.dll, Comctl32.dll et Windows. plus précisément, il prend en charge les types d’éléments d’interface utilisateur suivants (listés par Windows nom de la classe).



| nom de la classe Windows                   | Type d’élément d’interface utilisateur                                         | Windows Mises à jour de Vista                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ListBox                              | Zones de liste                                              | None                                                                                                                                                                                                                 |
| Bouton                               | Boutons de commande, cases d’option, boutons de case à cocher, zones de groupe | Les boutons partagés peuvent avoir zéro ou plusieurs enfants.                                                                                                                                                                        |
| statique                               | Étiquettes                                                  | None                                                                                                                                                                                                                 |
| Modifier                                 | Zones de texte                                              | None                                                                                                                                                                                                                 |
| ComboBox                             | Zones de liste déroulante, listes déroulantes                            | None                                                                                                                                                                                                                 |
| ScrollBar                            | Barres de défilement                                             | [**Événement \_ L’objet \_ CONTENTSCROLLED**](event-constants.md) est un nouvel événement pour le contrôle qui a des fonctionnalités de défilement, mais qui n’inclut pas de barre de défilement standard dans le cadre du contrôle. |
| \#32768                              | Menus utilisateur                                              | None                                                                                                                                                                                                                 |
| \#32770                              | Boîtes de dialogue utilisateur                                       | None                                                                                                                                                                                                                 |
| \#32771                              | Alt-Tab (fenêtre)                                          | Disponible uniquement en mode classique.                                                                                                                                                                                      |
| msctls \_ statusbar32                  | Barres d'état                                             | None                                                                                                                                                                                                                 |
| msctls \_ progress32                   | Barres de progression                                           | Les nouvelles options de couleur des barres de progression ne sont pas exposées par les propriétés Microsoft Active Accessibility ou Microsoft UI Automation.                                                                                         |
| msctls \_ hotkey32                     | Contrôles de touche d’accès rapide                                        | None                                                                                                                                                                                                                 |
| msctls \_ trackbar32                   | Trackbars, curseurs                                      | None                                                                                                                                                                                                                 |
| msctls \_ updown32                     | Contrôles Up-Down ou spin                                | None                                                                                                                                                                                                                 |
| SysAnimate32                         | Contrôle Animation                                       | None                                                                                                                                                                                                                 |
| SysTabControl32                      | Contrôle Tab                                             | None                                                                                                                                                                                                                 |
| SysHeader32                          | En-têtes de mode liste                                       | None                                                                                                                                                                                                                 |
| SysListView32                        | Contrôles d’affichage de liste                                      | None                                                                                                                                                                                                                 |
| SysTreeView32                        | Contrôles Tree View                                      | None                                                                                                                                                                                                                 |
| SysDateTimePick32 (versions 5 et 6) | Date et/ou sélecteur d’heure                                 | la Version 6 de ce contrôle dans Windows Vista a une implémentation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) native.                                                                                                           |
| SysIPAddress32                       | Contrôles d’adresse IP                                     | None                                                                                                                                                                                                                 |
| info-bulles \_ Class32                    | Info-bulles                                                | None                                                                                                                                                                                                                 |
| ToolbarWindow32                      | Barres d'outils                                                | None                                                                                                                                                                                                                 |
| RICHEDIT, RichEdit20A, RichEdit20W   | Champs de texte                                             | None                                                                                                                                                                                                                 |
| SysMonthCal32 (versions 5 et 6)     | Calendrier du mois                                          | la Version 6 de ce contrôle dans Windows Vista a une implémentation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) native.                                                                                                           |



 

Bien que la prise en charge des éléments d’interface fournis par le système soit fournie par Microsoft Active Accessibility sur Microsoft Windows NT 4,0 avec Service Pack 4, cette prise en charge est limitée.

Cette annexe répertorie les propriétés et les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que Microsoft Active Accessibility prend en charge pour chaque élément de l’interface utilisateur. Le cas échéant, la documentation répertorie également les [winEvents](winevents-infrastructure.md) que l’élément d’interface utilisateur déclenche et contient des informations supplémentaires sur les propriétés et les méthodes prises en charge. Elle contient également des informations sur les rôles d’objet et leurs propriétés et méthodes **IAccessible** prises en charge.

Ces détails peuvent aider les développeurs clients à éviter d’effectuer des appels inutiles à des propriétés et des méthodes non prises en charge. Ces informations permettent également aux développeurs de serveurs de savoir quelles propriétés et quelles méthodes leurs contrôles personnalisés doivent prendre en charge et quels WinEvents leurs contrôles doivent déclencher.

Utilisez les informations de cette annexe comme guide. Nous vous suggérons vivement d’utiliser les outils de Active Accessibility Microsoft pour vérifier le comportement attendu pour les éléments d’interface utilisateur ou les rôles d’objet.

Pour plus d'informations, voir les rubriques suivantes :

-   [Comment Active Accessibility expose les éléments d’interface utilisateur](how-active-accessibility-exposes-user-interface-elements.md)
-   [Référence des éléments de l’interface utilisateur](user-interface-element-reference.md)

 

 




