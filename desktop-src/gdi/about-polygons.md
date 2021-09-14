---
description: Un polygone est une forme remplie avec des côtés droits.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: À propos des polygones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126914344"
---
# <a name="about-polygons"></a>À propos des polygones

Un *polygone* est une forme remplie avec des côtés droits. Les côtés d’un polygone sont dessinés à l’aide du stylet actuel. Lorsque le système remplit un polygone, il utilise le pinceau actuel et le mode de remplissage polygone actuel. Les deux modes de remplissage, alternatif (valeur par défaut) et enroulement, déterminent si les régions d’un polygone complexe sont remplies ou laissées non peintes. Une application peut sélectionner l’un ou l’autre mode en appelant la fonction [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) . Pour plus d’informations sur les modes de remplissage des polygones, consultez [régions](regions.md).

L’illustration suivante montre un polygone dessiné à l’aide de [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).

![illustration d’un polygone dans la forme d’une étoile à cinq branches](images/csfsh-04.png)

En plus de dessiner un polygone unique à l’aide de [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), une application peut dessiner plusieurs polygones à l’aide de la fonction [**polypolygone**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) .

 

 
