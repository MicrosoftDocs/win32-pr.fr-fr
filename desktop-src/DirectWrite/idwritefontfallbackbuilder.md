---
title: Interface IDWriteFontFallbackBuilder
description: Vous permet de créer des mappages de substitution de police Unicode et de créer une police qui revient à l’objet de ces mappages.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Écriture directe de l’interface IDWriteFontFallbackBuilder
- Écriture directe de l’interface IDWriteFontFallbackBuilder, décrite
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f42bc9882c238bb1167c76e941c4f183eef05e12d5d8dc70305b0c01e048797
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051389"
---
# <a name="idwritefontfallbackbuilder-interface"></a>Interface IDWriteFontFallbackBuilder

Vous permet de créer des mappages de substitution de police Unicode et de créer une police qui revient à l’objet de ces mappages.

## <a name="members"></a>Membres

L’interface **IDWriteFontFallbackBuilder** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteFontFallbackBuilder** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDWriteFontFallbackBuilder** possède ces méthodes.



| Méthode                                                                      | Description                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AddMapping**](idwritefontfallbackbuilder-addmapping.md)                 | Ajoute un mappage unique à la liste. Appelez cette fois pour chaque mappage supplémentaire.<br/> |
| [**AddMappings**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | Ajoutez tous les mappages à partir d’un objet de police de secours existant.<br/>                       |
| [**CreateFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | Crée l’objet de secours finalisé à partir des mappages ajoutés.<br/>                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

