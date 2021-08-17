---
description: Une palette de couleurs est un tableau qui contient des valeurs de couleur identifiant les couleurs qui peuvent actuellement être affichées ou dessinées sur le périphérique de sortie.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: palettes de couleurs (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81079ac94b40de98bc1c53098a8b9d1654f90d0d855397ac38d11311e9741e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761956"
---
# <a name="color-palettes-windows-gdi"></a>palettes de couleurs (Windows GDI)

Une palette de couleurs est un tableau qui contient des valeurs de couleur identifiant les couleurs qui peuvent actuellement être affichées ou dessinées sur le périphérique de sortie. Les palettes de couleurs sont utilisées par les appareils capables de générer de nombreuses couleurs, mais qui ne peuvent afficher ou dessiner qu’un sous-ensemble de ces couleurs à un moment donné. Pour ces appareils, le système gère une *palette système* pour suivre et gérer les couleurs actuelles de l’appareil. Les applications n’ont pas d’accès direct à la palette du système. Au lieu de cela, le système associe une palette par défaut à chaque contexte de périphérique. Les applications peuvent utiliser les couleurs de la palette par défaut ou définir leurs propres couleurs en créant des *palettes logiques* et en les associant à des contextes de périphérique individuels.

Une application peut déterminer si un appareil prend en charge les palettes de couleurs en recherchant le \_ bit de palette RC dans la valeur RasterCaps retournée par la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) .

 

 



