---
title: Méthodes IDWriteFontSet GetPropertyValues (DWrite \_ 3. h)
description: Retourne des valeurs de propriété pour le jeu de polices.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- Écriture directe des méthodes GetPropertyValues
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cffc669d71bf7f78087fe3c105c182ca86b4ebf5a689bcdb6c2807dfae3c0f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816360"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a>IDWriteFontSet :: GetPropertyValues, méthodes

Retourne des valeurs de propriété pour le jeu de polices.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                   | Description                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetPropertyValues ( \_ ID de propriété de police DWRITE \_ \_ , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))                       | Retourne toutes les valeurs de propriété uniques dans le jeu, qui peuvent être utilisées à des fins telles que l’affichage d’une liste de familles ou d’un Cloud de balises. Toutes les valeurs sont retournées indépendamment de la langue, y compris tous les noms localisés. <br/>                                                                                       |
| [**GetPropertyValues ( \_ ID de propriété de police DWRITE \_ \_ , const WCHAR \* , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))        | Retourne toutes les valeurs de propriété uniques dans le jeu, qui peuvent être utilisées à des fins telles que l’affichage d’une liste de familles ou d’un Cloud de balises. Les valeurs sont retournées par ordre de priorité en fonction de la liste des langues, de telle sorte que si une police contient plusieurs noms localisés, la valeur par défaut est retournée. <br/> |
| [**GetPropertyValues (UINT32, DWRITE \_ police \_ \_ ID, bool \* , IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) | Retourne les valeurs de propriété d’un index d’élément de police spécifique.<br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DWrite \_ 3. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

�

�
