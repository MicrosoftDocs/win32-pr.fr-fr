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
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522526"
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
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

