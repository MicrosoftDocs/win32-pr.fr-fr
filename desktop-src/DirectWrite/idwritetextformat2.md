---
title: Interface IDWriteTextFormat2
description: Décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte et décrit les informations relatives aux paramètres régionaux. | Interface IDWriteTextFormat2
ms.assetid: 4396d2b0-240f-ee8b-1d21-c4294fb29b51
keywords:
- Écriture directe de l’interface IDWriteTextFormat2
- Écriture directe de l’interface IDWriteTextFormat2, décrite
topic_type:
- apiref
api_name:
- IDWriteTextFormat2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06abf78095953f684ed6ec3fd241c699b2b37db4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523782"
---
# <a name="idwritetextformat2-interface"></a>Interface IDWriteTextFormat2

Décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte et décrit les informations relatives aux paramètres régionaux.

## <a name="members"></a>Membres

L’interface **IDWriteTextFormat2** hérite de [**IDWriteTextFormat1**](idwritetextformat1.md). **IDWriteTextFormat2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDWriteTextFormat2** possède ces méthodes.



| Méthode                                                      | Description                                                                      |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetLineSpacing**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextformat2-getlinespacing) | Obtient l’ajustement de l’interligne défini pour un paragraphe de texte multiligne. <br/> |
| [**SetLineSpacing**](idwritetextformat2-setlinespacing.md) | Définissez l’interligne.<br/>                                                     |



 

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

[**IDWriteTextFormat1**](idwritetextformat1.md)
</dt> </dl>

 

