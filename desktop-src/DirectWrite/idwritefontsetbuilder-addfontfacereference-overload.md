---
title: Méthodes IDWriteFontSetBuilder AddFontFaceReference (DWrite \_ 3. h)
description: Ajoute une référence à une police au jeu en cours de génération.
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- Écriture directe des méthodes AddFontFaceReference
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3c20ca2832bfce3696a98c22730580442f621469
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526565"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a>IDWriteFontSetBuilder :: AddFontFaceReference, méthodes

Ajoute une référence à une police au jeu en cours de génération.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddFontFaceReference (IDWriteFontFaceReference \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))                                         | Ajoute une référence à une police au jeu en cours de génération. Les métadonnées nécessaires sont automatiquement extraites de la police lors de l’appel de CreateFontSet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**AddFontFaceReference (IDWriteFontFaceReference \* , const DWRITE \_ \_ propriété \* de police, UInt32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32)) | Ajoute une référence à une police au jeu en cours de génération. L’appelant fournit suffisamment d’informations pour effectuer des recherches, évitant ainsi d’avoir à ouvrir la police potentiellement non locale. Les propriétés non fournies par l’appelant sont manquantes, et ces propriétés ne sont pas disponibles en tant que filtres dans GetMatchingFonts. GetPropertyValues pour les propriétés manquantes retourne une liste de chaînes vide. Les propriétés transmises doivent généralement être cohérentes avec le contenu réel de la police, mais elles n’ont pas besoin d’être. Vous pouvez, par exemple, créer un alias de police à l’aide d’un autre nom ou d’un identificateur unique, ou vous pouvez définir des balises personnalisées qui ne sont pas présentes dans la police réelle.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DWrite \_ 3. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

�

�
