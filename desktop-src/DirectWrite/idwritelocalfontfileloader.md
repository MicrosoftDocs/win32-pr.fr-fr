---
title: Interface IDWriteLocalFontFileLoader
description: Implémentation intégrée de l’interface IDWriteFontFileLoader, qui opère sur des fichiers de polices locales et expose des informations de fichier de police locale à partir de la clé de référence du fichier de police.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Écriture directe de l’interface IDWriteLocalFontFileLoader
- Écriture directe de l’interface IDWriteLocalFontFileLoader, décrite
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65f537dc2a4a96161a11d85ae0a4e1869a331e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119805"
---
# <a name="idwritelocalfontfileloader-interface"></a>Interface IDWriteLocalFontFileLoader

Implémentation intégrée de l’interface [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , qui opère sur des fichiers de polices locales et expose des informations de fichier de police locale à partir de la clé de référence du fichier de police. Les références de fichiers de polices créées à l’aide de [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) utilisent ce chargeur de fichier de police.

## <a name="members"></a>Membres

L’interface **IDWriteLocalFontFileLoader** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteLocalFontFileLoader** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDWriteLocalFontFileLoader** possède ces méthodes.



| Méthode                                                                                  | Description                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**GetFilePathFromKey**](idwritelocalfontfileloader-getfilepathfromkey.md)             | Obtient le chemin d’accès absolu au fichier de polices à partir de la clé de référence du fichier de police.<br/>          |
| [**GetFilePathLengthFromKey**](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | Obtient la longueur du chemin d’accès absolu du fichier à partir de la clé de référence du fichier de police.<br/> |
| [**GetLastWriteTimeFromKey**](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | Obtient l’heure de la dernière écriture du fichier à partir de la clé de référence du fichier de police.<br/>      |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



 

