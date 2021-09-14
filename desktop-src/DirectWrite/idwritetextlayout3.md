---
title: Interface IDWriteTextLayout3
description: Représente un bloc de texte une fois qu’il a été entièrement analysé et mis en forme. | Interface IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Écriture directe de l’interface IDWriteTextLayout3
- Écriture directe de l’interface IDWriteTextLayout3, décrite
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094574"
---
# <a name="idwritetextlayout3-interface"></a>Interface IDWriteTextLayout3

Représente un bloc de texte une fois qu’il a été entièrement analysé et mis en forme.

## <a name="members"></a>Membres

L’interface **IDWriteTextLayout3** hérite de [**IDWriteTextLayout2**](idwritetextlayout2.md). **IDWriteTextLayout3** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDWriteTextLayout3** possède ces méthodes.



| Méthode                                                          | Description                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)     | Récupère les propriétés de chaque ligne.<br/>                                                                                                                                                                                                                        |
| [**GetLineSpacing**](idwritetextlayout3-getlinespacing.md)     | Obtient les informations d’interligne.<br/>                                                                                                                                                                                                                            |
| [**InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) | Invalide la disposition, en forçant la disposition à la mesure avant d’appeler les mesures ou les fonctions de dessin. Cela est utile si la localité d’une police change et si la disposition doit être redessinée, ou si la taille d’un client implémentant IDWriteInlineObject est modifiée. <br/> |
| [**SetLineSpacing**](idwritetextlayout3-setlinespacing.md)     | Définissez l’interligne.<br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





