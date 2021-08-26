---
title: Interface IDWriteTextAnalyzer2
description: Analyse diverses propriétés de texte pour le traitement complexe des scripts.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- Écriture directe de l’interface IDWriteTextAnalyzer2
- Écriture directe de l’interface IDWriteTextAnalyzer2, décrite
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a76d4b4b7c2ef09f82834ed2e7f40ee89d2ab80bd0595db62790f38831b86fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075569"
---
# <a name="idwritetextanalyzer2-interface"></a>Interface IDWriteTextAnalyzer2

Analyse diverses propriétés de texte pour le traitement complexe des scripts.

## <a name="members"></a>Membres

L’interface **IDWriteTextAnalyzer2** hérite de [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1). **IDWriteTextAnalyzer2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDWriteTextAnalyzer2** possède ces méthodes.



| Méthode                                                                                    | Description                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**CheckTypographicFeature**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | Vérifie si une fonctionnalité typographique est disponible pour un glyphe ou un ensemble de glyphes.<br/> |
| [**GetGlyphOrientationTransform**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | Retourne la matrice de transformation 2x3 pour l’angle respectif de dessin de l’exécution du glyphe.<br/> |
| [**GetTypographicFeatures**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | Retourne la liste complète des fonctionnalités OpenType disponibles pour un script ou une police.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

