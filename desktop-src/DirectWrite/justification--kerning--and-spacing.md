---
title: Justification, crénage et espacement
description: À compter de Windows 8, DirectWrite fournit un certain nombre de fonctionnalités qui vous permettent de contrôler les fonctionnalités typographiques de base, de mise en page et d’espacement, telles que l’espacement des caractères, le crénage des paires et la justification.
ms.assetid: A5397132-0806-4842-8B82-E17925FBBBA9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cc915922d0dbadb45bf47f223df83a25414daf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729829"
---
# <a name="justification-kerning-and-spacing"></a>Justification, crénage et espacement

À compter de Windows 8, [DirectWrite](direct-write-portal.md) fournit un certain nombre de fonctionnalités qui vous permettent de contrôler les fonctionnalités typographiques de base, de mise en page et d’espacement, telles que l’espacement des caractères, le crénage des paires et la justification.

## <a name="character-spacing"></a>Espacement des caractères

L’espacement des caractères, également appelé « suivi », est l’espacement entre les caractères d’une exécution de texte.

Voici un exemple de suivi. La première ligne ne s’applique à aucun suivi du texte. La deuxième ligne augmente l’espacement des caractères, tandis que la troisième ligne diminue l’espacement des caractères.

![trois exemples du même texte sans suivi, plus d’espacement et moins d’espacement.](images/spacing.png)

À compter de Windows 8, [DirectWrite](direct-write-portal.md) ajoute ces méthodes ici pour contrôler l’espacement des caractères dans votre texte.

Si vous utilisez la disposition [DirectWrite](direct-write-portal.md) , vous pouvez utiliser les méthodes [**IDWriteTextLayout1 :: GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) et [**IDWriteTextLayout1 :: SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) à cet effet.

Utilisez la méthode [**GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) pour déterminer l’espacement actuel des caractères et retourne le caractère actuel, l’espacement avant et après le caractère, la largeur d’avance minimale et une structure de [**\_ \_ plage de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) qui contient des informations sur la position de départ et la longueur du texte restant.

Utilisez [**SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) sur une interface [**DWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) pour appliquer votre propre espace de caractères au texte de la disposition. La méthode **SetCharacterSpacing** prend la quantité d’espace que vous souhaitez avant et après le caractère, l’avance minimale autorisée et une [**\_ \_ plage de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) qui définit la plage d’application de l’espacement.

Si vous utilisez une disposition personnalisée, [DirectWrite](direct-write-portal.md) prend en charge la définition de l’espacement des caractères avec [**IDWriteTextAnalyzer1 :: ApplyCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-applycharacterspacing). Utilisez cette méthode si vous avez besoin d’une disposition de texte personnalisée afin d’avoir un contrôle avancé sur votre disposition. Cette méthode vous permet de fournir des **ApplyCharacterSpacing** avec les espaces de début et de fin, la largeur d’avance minimale, la longueur de la carte de cluster, le nombre de glyphes, le mappage entre les plages de caractères et les glyphes, et la largeur d’avance de chaque glyphe si vous utilisez une disposition personnalisée. La méthode retourne les avances de glyphe modifiées et une énumération de [**\_ \_ décalage de glyphe DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) avec les nouveaux décalages par rapport à l’origine de chaque glyphe.

## <a name="kerning"></a>Le crénage

Le crénage est l’ajustement de l’espacement contextuel entre les paires ou les triplets de lettres. L’espacement spécifique entre les jeux de caractères peut améliorer la lisibilité et améliorer l’apparence du texte. La différence importante entre le crénage et l’espacement des caractères réside dans le fait que l’espacement des lettres est indépendant du texte des espaces, tandis que le crénage est utilisé dans certaines situations entre certaines paires de caractères, comme défini dans la police.

L’image elle est un exemple de crénage. Le mot AVATAR sur la ligne supérieure est crénage afin de rendre le mot plus naturel. Comme vous pouvez le voir dans les zones rouges autour des caractères, un espace supplémentaire est appliqué entre les quatre premières lettres, tandis que le R à l’extrémité a plus d’espace avant. Le texte d’origine sans crénage est sur la deuxième ligne. Dans cet exemple, le crénage rend le mot plus lisible et plus naturel.

![exemple de mot identique avec et sans crénage appliqué.](images/kerning.png)

Le caractère avance entre les paires de caractères que le crénage de police est stocké dans la table de crénage et [DirectWrite](direct-write-portal.md) analyse cette table et vous renvoie les informations via les API de crénage.

Si vous souhaitez savoir si une police prend en charge le crénage de paires, vous pouvez utiliser la méthode [**IDWriteFontFace1 :: HasKerningPairs**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs) . Cette méthode retourne une valeur booléenne de 1 si la police prend en charge les paires de crénage.

Le [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) dispose également d’une méthode qui vous permet d’accéder aux réglages de la paire de crénage pour les index de glyphes. [**GetKerningPairAdjustments**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments) vous permet d’entrer un tableau d’index de glyphes et [DirectWrite](direct-write-portal.md) retourne un tableau d’ajustements de glyphes avancés. Si une police ne prend pas en charge la table de crénage, la méthode retourne des zéros pour les réglages avancés du glyphe.

Si vous utilisez la disposition [DirectWrite](direct-write-portal.md) , il existe deux méthodes sur l’interface [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) qui vous permettent de définir le crénage des paires et d’en savoir plus sur le crénage de paires dans la disposition. La méthode [**SetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setpairkerning) prend une représentation booléenne indiquant si vous souhaitez activer le crénage des paires et une plage de [**\_ texte DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) qui définit la plage de texte à laquelle l’appliquer. Si vous souhaitez savoir si le crénage est activé ou non sur une plage de texte, vous pouvez utiliser la méthode [**GetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getpairkerning) , qui prend la position actuelle et retourne une valeur booléenne qui correspond à l’activation ou non du crénage des paires, ainsi qu’à la plage de texte à laquelle s’applique le paramètre de crénage.

## <a name="justification"></a>Justification

La justification est le processus qui consiste à aligner le texte afin qu’il remplisse tout l’espace dans une colonne en accroissant les avances entre les caractères ou les clusters de glyphes, ou en ajoutant des caractères de justification pour obtenir le même effet. En général, cela s’effectue en déterminant où l’espace doit être ajouté à une ligne de texte, et en insérant des caractères d’espacement dans les opportunités de rupture. Ces éléments d’espacement peuvent également différer, dans les scripts latins, le texte est justifié par l’amélioration des largeurs d’avance entre les éléments, tandis que dans l’arabe, le texte est justifié par un kachidé. Voici un exemple de script arabe et latin à la fois justifié et non justifié.

![un exemple de script arabe et latin est justifié et non justifié.](images/justification.png)

À compter de Windows 8, [DirectWrite](direct-write-portal.md) dispose d’un certain nombre de méthodes qui vous permettent de justifier du texte dans vos applications.

Il existe une valeur supplémentaire dans l’énumération de l' [**\_ \_ alignement du texte DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment) . Vous pouvez utiliser la méthode [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) et transmettre la constante **\_ \_ \_ justifiée d’alignement de texte DWRITE** et [DirectWrite](direct-write-portal.md) justifie le texte et insère le caractère de justification approprié pour le script.

Si vous utilisez une disposition personnalisée, plusieurs méthodes sont disponibles pour vous permettre de tirer parti de la justification. [DirectWrite](direct-write-portal.md) a trois méthodes sur l’interface [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) que vous pouvez utiliser pour ajouter la justification à une disposition personnalisée.

La première méthode est [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities), qui prend dans le texte que vous souhaitez justifier et retourne une structure [**d' \_ \_ opportunité de justification DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) qui met en ligne où des caractères de justification peuvent être ajoutés pour justifier le texte.

La deuxième fonction est [**JustifyGlyphAdvances**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances), qui justifie un tableau d’avances de glyphes afin qu’elles correspondent à la largeur de ligne. Cette méthode prend la structure [**d' \_ \_ opportunité de justification DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) que [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities) génère, le glyphe avance et les décalages de glyphe. Il génère ensuite les avances de glyphes justifiées et une énumération de [**\_ \_ décalage de glyphe DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) qui contient les décalages de glyphes justifiés.

La troisième fonction est [**GetJustifiedGlyphs**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustifiedglyphs), qui remplit les nouveaux glyphes pour les scripts complexes où la justification a augmenté les avances pour les glyphes. **GetJustifiedGlyphs** doit uniquement être appelé si le script comporte un caractère de justification spécifique tel qu’il est retourné par [**GetScriptProperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties). Cette méthode prend des informations sur la police, la longueur du texte, la taille de la police em des glyphes, le script du texte, le nombre de glyphes, le mappage de cluster, les avances/décalages de glyphes d’origine, les avancements de glyphes justifiés/les décalages et les propriétés de glyphe. La méthode retourne le nombre réel de glyphes, le mappage mis à jour, les index de glyphes mis à jour avec des glyphes de justification insérés, les décalages de glyphe mis à jour et les avances de glyphes mis à jour.

 

 