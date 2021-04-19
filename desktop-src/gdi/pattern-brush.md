---
description: Un pinceau de modèle (ou personnalisé) est créé à partir d’une bitmap définie par l’application ou d’une bitmap indépendante du périphérique (DIB). Les rectangles suivants ont été peints à l’aide de différents pinceaux de modèle.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Pinceau de motif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d39dd499d6a95b3fb61624b2aab8b421f51c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987698"
---
# <a name="pattern-brush"></a>Pinceau de motif

Un pinceau de modèle (ou personnalisé) est créé à partir d’une bitmap définie par l’application ou d’une bitmap indépendante du périphérique (DIB). Les rectangles suivants ont été peints à l’aide de différents pinceaux de modèle.

![Illustration montrant trois zones, chacune remplie d’un modèle différent](images/csbru-05.png)

Pour créer un pinceau de motif logique, une application doit d’abord créer une image bitmap. Après la création de l’image bitmap, l’application peut créer le pinceau de modèle logique en appelant la fonction [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) ou [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) , en fournissant un handle qui identifie la bitmap (ou DIB). Les pinceaux qui apparaissent dans l’illustration précédente ont été créés à partir d’images bitmap monochrome. Pour obtenir une description des bitmaps, des DIB et des fonctions qui les créent, consultez [bitmaps](bitmaps.md).

 

 



