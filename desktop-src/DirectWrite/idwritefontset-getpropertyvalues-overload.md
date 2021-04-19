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
ms.openlocfilehash: 3d135a63be987a4999d898c8e9c7d84251c8ece3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535995"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a><span data-ttu-id="044bd-104">IDWriteFontSet :: GetPropertyValues, méthodes</span><span class="sxs-lookup"><span data-stu-id="044bd-104">IDWriteFontSet::GetPropertyValues methods</span></span>

<span data-ttu-id="044bd-105">Retourne des valeurs de propriété pour le jeu de polices.</span><span class="sxs-lookup"><span data-stu-id="044bd-105">Returns property values for the font set.</span></span>

### <a name="overload-list"></a><span data-ttu-id="044bd-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="044bd-106">Overload list</span></span>



| <span data-ttu-id="044bd-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="044bd-107">Method</span></span>                                                                                                                                   | <span data-ttu-id="044bd-108">Description</span><span class="sxs-lookup"><span data-stu-id="044bd-108">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="044bd-109">[**GetPropertyValues ( \_ ID de propriété de police DWRITE \_ \_ , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="044bd-109">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span>                       | <span data-ttu-id="044bd-110">Retourne toutes les valeurs de propriété uniques dans le jeu, qui peuvent être utilisées à des fins telles que l’affichage d’une liste de familles ou d’un Cloud de balises.</span><span class="sxs-lookup"><span data-stu-id="044bd-110">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="044bd-111">Toutes les valeurs sont retournées indépendamment de la langue, y compris tous les noms localisés.</span><span class="sxs-lookup"><span data-stu-id="044bd-111">All values are returned regardless of language, including all localized names.</span></span> <br/>                                                                                       |
| <span data-ttu-id="044bd-112">[**GetPropertyValues ( \_ ID de propriété de police DWRITE \_ \_ , const WCHAR \* , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="044bd-112">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, const WCHAR\*, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span></span>        | <span data-ttu-id="044bd-113">Retourne toutes les valeurs de propriété uniques dans le jeu, qui peuvent être utilisées à des fins telles que l’affichage d’une liste de familles ou d’un Cloud de balises.</span><span class="sxs-lookup"><span data-stu-id="044bd-113">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="044bd-114">Les valeurs sont retournées par ordre de priorité en fonction de la liste des langues, de telle sorte que si une police contient plusieurs noms localisés, la valeur par défaut est retournée.</span><span class="sxs-lookup"><span data-stu-id="044bd-114">Values are returned in priority order according to the language list, such that if a font contains more than one localized name, the preferred one will be returned.</span></span> <br/> |
| <span data-ttu-id="044bd-115">[**GetPropertyValues (UINT32, DWRITE \_ police \_ \_ ID, bool \* , IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="044bd-115">[**GetPropertyValues(UINT32, DWRITE\_FONT\_PROPERTY\_ID, BOOL\*, IDWriteLocalizedStrings\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span> | <span data-ttu-id="044bd-116">Retourne les valeurs de propriété d’un index d’élément de police spécifique.</span><span class="sxs-lookup"><span data-stu-id="044bd-116">Returns the property values of a specific font item index.</span></span><br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="044bd-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="044bd-117">Requirements</span></span>



| <span data-ttu-id="044bd-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="044bd-118">Requirement</span></span> | <span data-ttu-id="044bd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="044bd-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="044bd-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="044bd-120">Header</span></span><br/> | <dl> <span data-ttu-id="044bd-121"><dt>DWrite \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="044bd-121"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="044bd-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="044bd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="044bd-123">**IDWriteFontSet**</span><span class="sxs-lookup"><span data-stu-id="044bd-123">**IDWriteFontSet**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

<span data-ttu-id="044bd-124">�</span><span class="sxs-lookup"><span data-stu-id="044bd-124">�</span></span>

<span data-ttu-id="044bd-125">�</span><span class="sxs-lookup"><span data-stu-id="044bd-125">�</span></span>
