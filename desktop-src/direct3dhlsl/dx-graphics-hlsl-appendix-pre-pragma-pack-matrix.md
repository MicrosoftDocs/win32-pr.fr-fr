---
title: pack_matrix directive pragma
description: Directive pragma qui spécifie l’alignement de la compression pour les matrices.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix le HLSL de la directive pragma
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030235"
---
# <a name="pack_matrix-pragma-directive"></a><span data-ttu-id="98b2b-104">Directive de pragma de matrice de Pack \_</span><span class="sxs-lookup"><span data-stu-id="98b2b-104">pack\_matrix pragma Directive</span></span>

<span data-ttu-id="98b2b-105">Directive pragma qui spécifie l’alignement de la compression pour les matrices.</span><span class="sxs-lookup"><span data-stu-id="98b2b-105">Pragma directive that specifies packing alignment for matrices.</span></span>



| <span data-ttu-id="98b2b-106">\#matrice pragma Pack \_ ( *alignement* )</span><span class="sxs-lookup"><span data-stu-id="98b2b-106">\#pragma pack\_matrix( *alignment* )</span></span> |
|--------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="98b2b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98b2b-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98b2b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="98b2b-108">Item</span></span></th>
<th><span data-ttu-id="98b2b-109">Description</span><span class="sxs-lookup"><span data-stu-id="98b2b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98b2b-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>repère</em></span><span class="sxs-lookup"><span data-stu-id="98b2b-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>alignment</em></span></span><br/></td>
<td><span data-ttu-id="98b2b-111">Alignement à définir pour les matrices.</span><span class="sxs-lookup"><span data-stu-id="98b2b-111">Alignment to set for matrices.</span></span> <span data-ttu-id="98b2b-112">Ce paramètre peut prendre l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="98b2b-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="98b2b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="98b2b-113">Value</span></span></th>
<th><span data-ttu-id="98b2b-114">Description</span><span class="sxs-lookup"><span data-stu-id="98b2b-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98b2b-115">column_major</span><span class="sxs-lookup"><span data-stu-id="98b2b-115">column_major</span></span></td>
<td><span data-ttu-id="98b2b-116">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="98b2b-116">Default.</span></span> <span data-ttu-id="98b2b-117">Définit l’alignement de la compression de la matrice sur la colonne principale.</span><span class="sxs-lookup"><span data-stu-id="98b2b-117">Sets the matrix packing alignment to column major.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98b2b-118">row_major</span><span class="sxs-lookup"><span data-stu-id="98b2b-118">row_major</span></span></td>
<td><span data-ttu-id="98b2b-119">Définit l’alignement de la compression de la matrice sur la ligne principale.</span><span class="sxs-lookup"><span data-stu-id="98b2b-119">Sets the matrix packing alignment to row major.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="98b2b-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="98b2b-120">Examples</span></span>

<span data-ttu-id="98b2b-121">L’exemple suivant définit l’alignement de la compression de la matrice sur la ligne principale.</span><span class="sxs-lookup"><span data-stu-id="98b2b-121">The following example sets the matrix packing alignment to row major.</span></span>


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a><span data-ttu-id="98b2b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98b2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b2b-123">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98b2b-123">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="98b2b-124">\#Directive pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98b2b-124">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





