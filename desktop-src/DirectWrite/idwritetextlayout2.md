---
title: Interface IDWriteTextLayout2
description: Représente un bloc de texte une fois qu’il a été entièrement analysé et mis en forme. | Interface IDWriteTextLayout2
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- Écriture directe de l’interface IDWriteTextLayout2
- Écriture directe de l’interface IDWriteTextLayout2, décrite
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bb6037a598096109a9255abbb01ef289c5ef99
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322289"
---
# <a name="idwritetextlayout2-interface"></a>Interface IDWriteTextLayout2

Représente un bloc de texte une fois qu’il a été entièrement analysé et mis en forme.

## <a name="members"></a>Membres

L’interface **IDWriteTextLayout2** hérite de [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1). **IDWriteTextLayout2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDWriteTextLayout2** possède ces méthodes.



| Méthode                                                                                | Description                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | Obtient l’objet de police de secours actuel. <br/>                                           |
| [**GetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | Déterminez si le dernier mot sur la dernière ligne est renvoyé à la ligne.<br/>                    |
| [**GetMetrics**](idwritetextlayout2-getmetrics.md)                                   | Récupère les métriques globales de la chaîne mise en forme. <br/>                             |
| [**GetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | Obtient la manière dont les glyphes s’alignent sur les bords de la marge. <br/>                               |
| [**GetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | Obtenir l’orientation par défaut des glyphes lorsque vous utilisez un sens de lecture vertical.<br/> |
| [**SetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | Appliquez une police de secours personnalisée à la disposition.<br/>                                        |
| [**SetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | Définit si le dernier mot sur la dernière ligne est renvoyé à la ligne. <br/>                   |
| [**SetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | Définissez la façon dont les glyphes s’alignent sur les bords de la marge.<br/>                                |
| [**SetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | Définissez l’orientation par défaut des glyphes lorsque vous utilisez un sens de lecture vertical.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

