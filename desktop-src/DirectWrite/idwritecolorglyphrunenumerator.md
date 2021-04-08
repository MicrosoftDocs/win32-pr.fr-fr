---
title: Interface IDWriteColorGlyphRunEnumerator
description: Cette interface permet à l’application d’énumérer les exécutions de glyphes de couleurs.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Écriture directe de l’interface IDWriteColorGlyphRunEnumerator
- Écriture directe de l’interface IDWriteColorGlyphRunEnumerator, décrite
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742237"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a>Interface IDWriteColorGlyphRunEnumerator

Cette interface permet à l’application d’énumérer les exécutions de glyphes de couleurs. L’énumérateur énumère les couches dans une commande Back to front pour les couches appropriées.

## <a name="members"></a>Membres

L’interface **IDWriteColorGlyphRunEnumerator** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteColorGlyphRunEnumerator** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDWriteColorGlyphRunEnumerator** possède ces méthodes.



| Méthode                                                                | Description                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [**GetCurrentRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | Retourne l’exécution de glyphes actuelle de l’énumérateur.<br/> |
| [**MoveNext**](idwritecolorglyphrunenumerator-movenext.md)           | Passe au glyphe suivant exécuté dans l’énumérateur.<br/>    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

