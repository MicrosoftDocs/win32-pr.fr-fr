---
description: Les fonctions suivantes sont utilisées avec le découpage.
ms.assetid: de9e5786-63d8-47be-8522-e96d7c0f8634
title: Fonctions de découpage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7e3ec1c57713a87e5367ed28427caaab663e0bcd1abfe83c4040e04a7e6d75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115329"
---
# <a name="clipping-functions"></a>Fonctions de découpage

Les fonctions suivantes sont utilisées avec le découpage.



| Fonction                                       | Description                                                                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect)     | Crée une nouvelle zone de découpage qui se compose de la région de découpage existante moins le rectangle spécifié.                                                                                |
| [**ExtSelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-extselectcliprgn)   | Combine la région spécifiée avec la zone de découpage en cours à l’aide du mode spécifié.                                                                                                  |
| [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox)               | Récupère les dimensions du rectangle englobant le plus étroit qui peut être dessinée autour de la zone visible actuelle sur l’appareil.                                                              |
| [**GetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getcliprgn)               | Récupère un handle qui identifie la zone de découpage définie par l’application actuelle pour le contexte de périphérique spécifié.                                                                          |
| [**GetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getmetargn)               | Récupère la région actuelle pour le contexte de périphérique spécifié.                                                                                                                        |
| [**GetRandomRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getrandomrgn)           | Copie la zone de découpage du système d’un contexte de périphérique spécifié dans une région spécifique.                                                                                                     |
| [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) | Crée une nouvelle zone de découpage à partir de l’intersection de la zone de découpage actuelle et du rectangle spécifié.                                                                           |
| [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn)         | Déplace la zone de découpage d’un contexte de périphérique selon les décalages spécifiés.                                                                                                                   |
| [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible)                 | Détermine si le point spécifié se trouve dans la zone de découpage d’un contexte de périphérique (Device Context).                                                                                                 |
| [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible)             | Détermine si une partie du rectangle spécifié se trouve dans la zone de découpage d’un contexte de périphérique.                                                                               |
| [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)       | Sélectionne le chemin d’accès actuel comme zone de découpage pour un contexte de périphérique, en combinant la nouvelle région avec une région de découpage existante à l’aide du mode spécifié.                               |
| [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)         | Sélectionne une région comme zone de découpage actuelle pour le contexte de périphérique spécifié.                                                                                                         |
| [**SetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setmetargn)               | Croise la zone de découpage actuelle pour le contexte de périphérique spécifié avec la région active et enregistre la zone combinée comme nouvelle région pour le contexte de périphérique spécifié. |



 

 

 



