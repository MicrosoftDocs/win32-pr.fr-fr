---
description: Pour fournir la justification du texte, une application peut utiliser l’une des deux méthodes suivantes.
ms.assetid: 1190baed-5959-4f7a-8946-ac3b3da85821
title: Traitement de scripts complexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987c58cd1d6e8979573b47bbf3e2e7ff248617b12907f81ef70761c08403a067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390423"
---
# <a name="processing-complex-scripts"></a>Traitement de scripts complexes

Pour fournir la justification du texte, une application peut utiliser l’une des deux méthodes suivantes. Pour une implémentation simple de la justification multilingue, l’application doit appeler [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify). Il génère le tableau DX Delta en tenant compte des signes kachidé, de l’espacement entre les mots, puis de l’espacement entre les caractères. Pour une justification plus sophistiquée, l’application peut générer un tableau DX Delta mis à jour à l’aide de sa propre langue et des informations extraites par [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) dans le tableau [**\_ VISATTR de scripts**](/windows/win32/api/usp10/ns-usp10-script_visattr) .

L’espace de justification ou les kachidés doivent être insérés là où ils sont identifiés par le membre **uJustification** du [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr). Lorsque vous effectuez une justification entre les caractères, l’application doit insérer l’espace supplémentaire uniquement après les glyphes marqués avec le SCRIPT \_ Justify \_ .

L’application effectue le placement et le test de positionnement à l’aide de [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) et [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox). Pour plus d’informations, consultez [gestion du placement du signe insertion et test de positionnement](managing-caret-placement-and-hit-testing.md).

Pour obtenir des largeurs de manière indépendante de la police, l’application appelle [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths). En passant les largeurs logiques à [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth), un bloc de texte peut être réaffiché dans les mêmes limites avec une perte de qualité acceptable, même lorsque la police d’origine n’est pas disponible. Il génère un tableau de largeurs de glyphes ([largeurs d’avances](uniscribe-glossary.md)) pouvant être transmis à [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout). Ce type d’enregistrement et de réapplication des informations de largeur d’avance de manière indépendante de la police peut être utile dans des situations telles que le profilage dans un format défini par l’application.

> [!Note]  
> Les fichiers de fichiers ne prennent pas en charge les index de glyphes. Pour écrire dans un métafichier amélioré, l’application doit utiliser [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) et écrire les caractères logiques directement. À l’aide de ce mécanisme, la génération et l’emplacement du glyphe ne se produisent pas tant que le texte n’a pas été lu.

 

Pour récupérer les glyphes spécifiques utilisés pour les valeurs par défaut, vides, kachidé, etc., pour la police actuelle, l’application doit appeler [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Pour déterminer quels caractères dans une série de tests sont pris en charge par la police sélectionnée, l’application appelle [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap). Les caractères qui ne sont pas disponibles ont le glyphe par défaut dans la mémoire tampon du glyphe. Notez que cette méthode échoue si une police effectue le rendu d’un caractère à l’aide d’une combinaison de glyphes au lieu d’un seul glyphe. Par exemple, 00C9 ; La lettre majuscule latine E avec accent aigu peut être rendue à l’aide d’un glyphe E majuscule et d’un glyphe aigu. Pour déterminer la prise en charge des polices pour une chaîne qui contient ces genres de points de code, l’application peut appeler [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape). Pour plus d’informations, consultez Utilisation de moteurs de mise [en forme](using-shaping-engines.md).

La fonction [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight) retourne la hauteur de la police à partir du cache de polices. [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) fournit des informations sur le traitement spécial requis pour tous les scripts, indexés par script. Par exemple, il comprend la langue principale associée au script, les données indiquant si le script est numérique et les données indiquant si le script est un script complexe.

[**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth) retourne la [largeur ABC](uniscribe-glossary.md) d’un glyphe donné, ce qui peut être utile pour dessiner des graphiques de glyphes. Toutefois, il ne doit pas être utilisé pour la mise en forme de texte de script complexe normale.

## <a name="related-topics"></a>Rubriques connexes

[Utilisation de Uniscribe](using-uniscribe.md)


 

 
