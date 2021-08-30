---
title: Interface IDWriteTextFormat1
description: Décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte et décrit les informations relatives aux paramètres régionaux. | Interface IDWriteTextFormat1
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- Écriture directe de l’interface IDWriteTextFormat1
- Écriture directe de l’interface IDWriteTextFormat1, décrite
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25fa32ea9faff586cbaf3c40a8ffe3d12c7e983fac7b3a0526c65b71757ea91f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075559"
---
# <a name="idwritetextformat1-interface"></a>Interface IDWriteTextFormat1

Décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte et décrit les informations relatives aux paramètres régionaux. Cette interface a les mêmes méthodes que [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) et ajoute la possibilité d’appliquer une orientation explicite.

## <a name="members"></a>Membres

L’interface **IDWriteTextFormat1** hérite de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat). **IDWriteTextFormat1** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDWriteTextFormat1** possède ces méthodes.



| Méthode                                                                                | Description                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | Obtient le de secours actuel. Si aucun n’a été défini depuis la création de la disposition, il sera nullptr.<br/>               |
| [**GetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | Obtient le mode d’habillage de la dernière ligne.<br/>                                                                     |
| [**GetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | Obtient l’alignement de la marge optique pour le format texte.<br/>                                                       |
| [**GetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | Obtenir l’orientation par défaut des glyphes lorsque vous utilisez un sens de lecture vertical.<br/>                             |
| [**SetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | Applique la police de secours personnalisée à la disposition. Si aucune valeur n’est définie, elle utilise la liste de secours système par défaut. <br/> |
| [**SetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | Définit le mode d’habillage de la dernière ligne.<br/>                                                                     |
| [**SetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | Définit l’alignement de la marge optique pour le format texte.<br/>                                                       |
| [**SetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | Définit l’orientation d’un format de texte.<br/>                                                                       |



 

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

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

