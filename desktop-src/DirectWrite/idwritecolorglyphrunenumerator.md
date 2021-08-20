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
ms.openlocfilehash: 8fa665f7000ffaada5bc14f97671fb6e52266c712ef6081b956184653d1f1c95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536139"
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
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

