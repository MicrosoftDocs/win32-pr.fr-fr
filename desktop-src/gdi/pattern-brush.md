---
description: Un pinceau de modèle (ou personnalisé) est créé à partir d’une bitmap définie par l’application ou d’une bitmap indépendante du périphérique (DIB). Les rectangles suivants ont été peints à l’aide de différents pinceaux de modèle.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Pinceau de motif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48b7d5f3bc5c4b0fd86eda28a35bb56f02e5ba998353d36d829a71655aa66f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831519"
---
# <a name="pattern-brush"></a>Pinceau de motif

Un pinceau de modèle (ou personnalisé) est créé à partir d’une bitmap définie par l’application ou d’une bitmap indépendante du périphérique (DIB). Les rectangles suivants ont été peints à l’aide de différents pinceaux de modèle.

![Illustration montrant trois zones, chacune remplie d’un modèle différent](images/csbru-05.png)

Pour créer un pinceau de motif logique, une application doit d’abord créer une image bitmap. Après la création de l’image bitmap, l’application peut créer le pinceau de modèle logique en appelant la fonction [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) ou [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) , en fournissant un handle qui identifie la bitmap (ou DIB). Les pinceaux qui apparaissent dans l’illustration précédente ont été créés à partir d’images bitmap monochrome. Pour obtenir une description des bitmaps, des DIB et des fonctions qui les créent, consultez [bitmaps](bitmaps.md).

 

 



