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
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a><span data-ttu-id="50880-104">IDWriteFontSetBuilder :: AddFontFaceReference, méthodes</span><span class="sxs-lookup"><span data-stu-id="50880-104">IDWriteFontSetBuilder::AddFontFaceReference methods</span></span>

<span data-ttu-id="50880-105">Ajoute une référence à une police au jeu en cours de génération.</span><span class="sxs-lookup"><span data-stu-id="50880-105">Adds a reference to a font to the set being built.</span></span>

### <a name="overload-list"></a><span data-ttu-id="50880-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="50880-106">Overload list</span></span>



| <span data-ttu-id="50880-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="50880-107">Method</span></span>                                                                                                                                           | <span data-ttu-id="50880-108">Description</span><span class="sxs-lookup"><span data-stu-id="50880-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50880-109">[**AddFontFaceReference (IDWriteFontFaceReference \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span><span class="sxs-lookup"><span data-stu-id="50880-109">[**AddFontFaceReference(IDWriteFontFaceReference\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span></span>                                         | <span data-ttu-id="50880-110">Ajoute une référence à une police au jeu en cours de génération.</span><span class="sxs-lookup"><span data-stu-id="50880-110">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="50880-111">Les métadonnées nécessaires sont automatiquement extraites de la police lors de l’appel de CreateFontSet.</span><span class="sxs-lookup"><span data-stu-id="50880-111">The necessary metadata will automatically be extracted from the font upon calling CreateFontSet.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="50880-112">[**AddFontFaceReference (IDWriteFontFaceReference \* , const DWRITE \_ \_ propriété \* de police, UInt32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span><span class="sxs-lookup"><span data-stu-id="50880-112">[**AddFontFaceReference(IDWriteFontFaceReference\*, const DWRITE\_FONT\_PROPERTY\*, UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span></span> | <span data-ttu-id="50880-113">Ajoute une référence à une police au jeu en cours de génération.</span><span class="sxs-lookup"><span data-stu-id="50880-113">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="50880-114">L’appelant fournit suffisamment d’informations pour effectuer des recherches, évitant ainsi d’avoir à ouvrir la police potentiellement non locale.</span><span class="sxs-lookup"><span data-stu-id="50880-114">The caller supplies enough information to search on, avoiding the need to open the potentially non-local font.</span></span> <span data-ttu-id="50880-115">Les propriétés non fournies par l’appelant sont manquantes, et ces propriétés ne sont pas disponibles en tant que filtres dans GetMatchingFonts.</span><span class="sxs-lookup"><span data-stu-id="50880-115">Any properties not supplied by the caller will be missing, and those properties will not be available as filters in GetMatchingFonts.</span></span> <span data-ttu-id="50880-116">GetPropertyValues pour les propriétés manquantes retourne une liste de chaînes vide.</span><span class="sxs-lookup"><span data-stu-id="50880-116">GetPropertyValues for missing properties will return an empty string list.</span></span> <span data-ttu-id="50880-117">Les propriétés transmises doivent généralement être cohérentes avec le contenu réel de la police, mais elles n’ont pas besoin d’être.</span><span class="sxs-lookup"><span data-stu-id="50880-117">The properties passed should generally be consistent with the actual font contents, but they need not be.</span></span> <span data-ttu-id="50880-118">Vous pouvez, par exemple, créer un alias de police à l’aide d’un autre nom ou d’un identificateur unique, ou vous pouvez définir des balises personnalisées qui ne sont pas présentes dans la police réelle.</span><span class="sxs-lookup"><span data-stu-id="50880-118">You could, for example, alias a font using a different name or unique identifier, or you could set custom tags not present in the actual font.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="50880-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50880-119">Requirements</span></span>



| <span data-ttu-id="50880-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50880-120">Requirement</span></span> | <span data-ttu-id="50880-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="50880-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50880-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="50880-122">Header</span></span><br/> | <dl> <span data-ttu-id="50880-123"><dt>DWrite \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="50880-123"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50880-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50880-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50880-125">**IDWriteFontSetBuilder**</span><span class="sxs-lookup"><span data-stu-id="50880-125">**IDWriteFontSetBuilder**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

<span data-ttu-id="50880-126">�</span><span class="sxs-lookup"><span data-stu-id="50880-126">�</span></span>

<span data-ttu-id="50880-127">�</span><span class="sxs-lookup"><span data-stu-id="50880-127">�</span></span>
