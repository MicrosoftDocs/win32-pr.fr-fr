---
title: Interface ID3DX11DataProcessor (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Objet de traitement de données utilisé par l’interface ID3DX11ThreadPump pour le chargement des données de façon asynchrone.'
ms.assetid: ab893879-416f-4b17-9035-a7f03a62b753
keywords:
- Interface ID3DX11DataProcessor Direct3D 11
- Interface ID3DX11DataProcessor Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e421a6e840665220311e5a27c0692cd7f347e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104971859"
---
# <a name="id3dx11dataprocessor-interface"></a><span data-ttu-id="a87d6-106">Interface ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="a87d6-106">ID3DX11DataProcessor interface</span></span>

> [!Note]  
> <span data-ttu-id="a87d6-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a87d6-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="a87d6-108">Objet de traitement de données utilisé par l' [**interface ID3DX11ThreadPump**](id3dx11threadpump.md) pour le chargement des données de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a87d6-108">Data processing object used by [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="a87d6-109">Membres</span><span class="sxs-lookup"><span data-stu-id="a87d6-109">Members</span></span>

<span data-ttu-id="a87d6-110">L’interface **ID3DX11DataProcessor** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a87d6-110">The **ID3DX11DataProcessor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a87d6-111">**ID3DX11DataProcessor** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a87d6-111">**ID3DX11DataProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="a87d6-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a87d6-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a87d6-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a87d6-113">Methods</span></span>

<span data-ttu-id="a87d6-114">L’interface **ID3DX11DataProcessor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a87d6-114">The **ID3DX11DataProcessor** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="a87d6-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="a87d6-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a87d6-116">Description</span><span class="sxs-lookup"><span data-stu-id="a87d6-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a87d6-117"><a href="id3dx11dataprocessor-createdeviceobject.md"><strong>CreateDeviceObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="a87d6-117"><a href="id3dx11dataprocessor-createdeviceobject.md"><strong>CreateDeviceObject</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="a87d6-118">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a87d6-118">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="a87d6-119">Crée un objet appareil.</span><span class="sxs-lookup"><span data-stu-id="a87d6-119">Creates a device object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="a87d6-120"><a href="id3dx11dataprocessor-destroy.md"><strong>Suppression</strong></a></span><span class="sxs-lookup"><span data-stu-id="a87d6-120"><a href="id3dx11dataprocessor-destroy.md"><strong>Destroy</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="a87d6-121">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a87d6-121">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="a87d6-122">Détruit le processeur après la fin d’un élément de travail.</span><span class="sxs-lookup"><span data-stu-id="a87d6-122">Destroys the processor after a work item completes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="a87d6-123"><a href="id3dx11dataprocessor-process.md"><strong>Processus</strong></a></span><span class="sxs-lookup"><span data-stu-id="a87d6-123"><a href="id3dx11dataprocessor-process.md"><strong>Process</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="a87d6-124">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a87d6-124">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="a87d6-125">Traite les données.</span><span class="sxs-lookup"><span data-stu-id="a87d6-125">Processes data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a87d6-126">Notes</span><span class="sxs-lookup"><span data-stu-id="a87d6-126">Remarks</span></span>

<span data-ttu-id="a87d6-127">Cet objet peut être hérité et ses membres redéfinis pour le traitement des formats de fichier personnalisés.</span><span class="sxs-lookup"><span data-stu-id="a87d6-127">This object can be inherited and its members redefined for processing custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="a87d6-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a87d6-128">Requirements</span></span>



| <span data-ttu-id="a87d6-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a87d6-129">Requirement</span></span> | <span data-ttu-id="a87d6-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a87d6-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a87d6-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a87d6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a87d6-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a87d6-132">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a87d6-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a87d6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a87d6-134">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a87d6-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a87d6-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="a87d6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a87d6-136"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a87d6-136"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="a87d6-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a87d6-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="a87d6-138"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a87d6-138"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a87d6-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a87d6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a87d6-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="a87d6-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

