---
title: Texte vertical
description: à partir de la Windows 8, DirectWrite a un certain nombre de nouvelles api qui vous permettent d’utiliser du texte vertical dans vos applications.
ms.assetid: F40A79AE-F7BF-4CAC-9480-1489CD212DA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa5e6626ae77e610c38bfb90def7cfe068db80f7f300f58a734969fb107a46a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632543"
---
# <a name="vertical-text"></a>Texte vertical

à partir de la Windows 8, [DirectWrite](direct-write-portal.md) a un certain nombre de nouvelles api qui vous permettent d’utiliser du texte vertical dans vos applications.

## <a name="drawing-vertical-text"></a>Dessiner du texte vertical

Vous pouvez dessiner du texte vertical avec Direct2D à l’aide des méthodes [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) . Pour dessiner le texte verticalement, transmettez le [**sens de lecture DWRITE de \_ \_ \_ haut \_ en \_ bas**](/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction) à la méthode [**IDWriteTextFormat :: SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) et le sens du déroulement de l' [**DWRITE de droite à \_ \_ \_ \_ \_ gauche**](/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction) à la méthode [**IDWriteTextFormatSetFlowDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection) . Vous pouvez ensuite créer et dessiner un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) vertical.

## <a name="analyzing-character-orientation"></a>Analyser l’orientation des caractères

Chaque caractère a une orientation de caractère par défaut, ou la direction dans laquelle le caractère doit être orienté dans n’importe quelle disposition directionnelle. Par exemple, dans une disposition horizontale traditionnelle, le texte latin et le texte chinois sont orientés verticalement. D’un autre côté, dans une disposition verticale, le texte chinois reste debout et le texte latin est pivoté de 90 degrés. Cette différence d’orientation est visible dans l’exemple ici.

![image de texte en anglais et en chinois dans les dispositions horizontales et verticales.](images/vertical-text.png)

Pour déterminer l’orientation du texte dont vous disposez, vous devez implémenter les interfaces [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) et [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) . La source et le récepteur prennent le glyphe s’exécute et vous permettent de vérifier s’ils sont orientés verticalement ou non.

Après avoir implémenté votre source et votre récepteur, vous appelez la méthode [**AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) . Dans l’exemple d’image, cette fonction retourne 3 exécutions : « English », « 中国 » et « English ».

## <a name="going-from-characters-to-glyphs"></a>Passage de caractères aux glyphes

Maintenant que vous savez que l’exécution contient des glyphes verticaux, vous devez avoir accès à ces glyphes. Dans l’exemple jusqu’à présent, il y a 3 exécutions : une avec des glyphes verticaux et deux sans. Pour passer des caractères aux glyphes, vous devez appeler [**GetGlyphIndices**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices). Cette méthode retourne les index de glyphe correspondants pour les caractères de l’exemple. Étant donné que la méthode [**AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) retourne une exécution avec des glyphes verticaux, vous devez appeler [**GetVerticalGlyphVariants**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants), qui retourne les ID de glyphes orientés verticalement à la place des ID de glyphes actuels.

## <a name="drawing-text-vertically"></a>Dessiner du texte verticalement

Enfin, vous devez disposer et dessiner le texte. Étant donné que vous dessinez le texte verticalement, vous devez obtenir davantage d’informations pour que le texte latin soit dessiné correctement. Si vous dessinez tout le texte le long de la ligne de base centrale, le texte latin apparaît comme flottant au milieu de la ligne. Vous devez avoir accès à la ligne de base centrale et romaine pour aligner correctement le texte. Utilisez la méthode [**IDWriteTextAnalyzer1 :: GetBaseline**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline) pour récupérer les valeurs numériques des lignes de base que vous spécifiez. Vous pouvez soustraire la ligne de base romaine de la ligne de base centrale pour récupérer le décalage entre les deux.

Avec toutes ces informations, vous pouvez dessiner le texte à l’écran. Tout d’abord, appelez la méthode [**GetGlyphOrientationTransform**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform) avec les résultats des objets [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) et [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) .

Si vous utilisez [Direct2D](rendering-by-using-direct2d.md) , vous devez également définir la transformation universelle sur la cible de rendu Direct2D pour le rendu vertical.

Enfin, appelez [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) trois fois, une fois sur chaque bloc de texte. Dans les deux blocs de texte en anglais, vous devez appliquer le décalage que nous avons calculé entre les lignes de base romanes et centrales.

À présent, le texte de votre application est dessiné verticalement, avec l’orientation de glyphe correcte.

 

 