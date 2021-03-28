---
description: Lors de la création d’un contexte de périphérique d’affichage, le système assigne des valeurs par défaut pour les attributs (c’est-à-dire les objets de dessin, les couleurs et les modes) qui composent le contexte de périphérique.
ms.assetid: 1a9244e6-2773-435a-8569-806df3a0cd39
title: Afficher les paramètres par défaut du contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8abcf79339d4f1cc158253d46cc3eb02ec41311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863658"
---
# <a name="display-device-context-defaults"></a>Afficher les paramètres par défaut du contexte de périphérique

Lors de la création d’un contexte de périphérique d’affichage, le système assigne des valeurs par défaut pour les attributs (c’est-à-dire les objets de dessin, les couleurs et les modes) qui composent le contexte de périphérique. Le tableau suivant indique les valeurs par défaut des attributs d’un contexte de périphérique d’affichage.



| Attribut                             | Valeur par défaut                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Couleur d’arrière-plan                      | Paramètre de couleur d’arrière-plan dans le panneau de configuration (généralement, blanc).                                                                               |
| Mode arrière-plan                       | MANIÈRE                                                                                                                                        |
| Bitmap                                | Aucun                                                                                                                                          |
| Brush                                 | \_pinceau blanc                                                                                                                                  |
| Origine du pinceau                          | (0, 0)                                                                                                                                         |
| Zone de découpage                       | Fenêtre entière ou zone cliente avec la région de mise à jour découpée, selon le cas. Les fenêtres enfants et pop-up dans la zone cliente peuvent également être découpées. |
| Palette                               | PALETTE par défaut \_                                                                                                                              |
| Position actuelle du stylet                  | (0, 0)                                                                                                                                         |
| Origine de l’appareil                         | Coin supérieur gauche de la fenêtre ou de la zone cliente.                                                                                           |
| Mode dessin                          | \_COPYPEN R2                                                                                                                                   |
| Police                                  | \_police système                                                                                                                                  |
| Espacement entre les caractères                | 0                                                                                                                                             |
| Mode de mappage                          | \_texte mm                                                                                                                                      |
| Stylet                                   | \_stylet noir                                                                                                                                    |
| [**Polygone**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) -mode de remplissage | BASCUL                                                                                                                                     |
| Mode Stretch                          | BLACKONWHITE                                                                                                                                  |
| Couleur du texte                            | Paramètre de couleur du texte dans le panneau de configuration (en général, noir).                                                                                     |
| Étendue de la fenêtre d’affichage                       | (1, 1)                                                                                                                                         |
| Origine de la fenêtre d’affichage                       | (0, 0)                                                                                                                                         |
| Étendue de la fenêtre                         | (1, 1)                                                                                                                                         |
| Origine de la fenêtre                         | (0, 0)                                                                                                                                         |



 

Une application peut modifier les valeurs des attributs de contexte de périphérique d’affichage à l’aide des fonctions de sélection et d’attribut, telles que [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject), [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)et [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor). Par exemple, une application peut modifier les unités de mesure par défaut dans le système de coordonnées à l’aide de **SetMapMode** pour modifier le mode de mappage.

Les modifications apportées aux valeurs d’attribut d’un contexte de périphérique commun, parent ou Windows ne sont pas permanentes. Quand une application libère ces contextes de périphérique, les sélections actuelles, telles que le mode de mappage et la région de découpage, sont perdues à mesure que le contexte est retourné au cache. Les modifications apportées à une classe ou à un contexte de périphérique privé persistent indéfiniment. Pour restaurer leurs valeurs par défaut d’origine, une application doit définir explicitement chaque attribut.

 

 



