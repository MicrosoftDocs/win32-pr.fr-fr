---
title: Interface IDWriteFont2
description: Représente une police physique dans une collection de polices.
ms.assetid: 4E3069AE-5882-4A26-A36D-BE7D7EE1B0C3
keywords:
- Écriture directe de l’interface IDWriteFont2
- Écriture directe de l’interface IDWriteFont2, décrite
topic_type:
- apiref
api_name:
- IDWriteFont2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82a47e56915747b0e118a6f63484b9dd3dcdbd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317313"
---
# <a name="idwritefont2-interface"></a><span data-ttu-id="51628-105">Interface IDWriteFont2</span><span class="sxs-lookup"><span data-stu-id="51628-105">IDWriteFont2 interface</span></span>

<span data-ttu-id="51628-106">Représente une police physique dans une collection de polices.</span><span class="sxs-lookup"><span data-stu-id="51628-106">Represents a physical font in a font collection.</span></span>

<span data-ttu-id="51628-107">Cette interface ajoute la possibilité de vérifier si un chemin de rendu des couleurs est potentiellement nécessaire.</span><span class="sxs-lookup"><span data-stu-id="51628-107">This interface adds the ability to check if a color rendering path is potentially necessary.</span></span>

## <a name="members"></a><span data-ttu-id="51628-108">Membres</span><span class="sxs-lookup"><span data-stu-id="51628-108">Members</span></span>

<span data-ttu-id="51628-109">L’interface **IDWriteFont2** hérite de [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span><span class="sxs-lookup"><span data-stu-id="51628-109">The **IDWriteFont2** interface inherits from [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span></span> <span data-ttu-id="51628-110">**IDWriteFont2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="51628-110">**IDWriteFont2** also has these types of members:</span></span>

-   [<span data-ttu-id="51628-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="51628-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="51628-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="51628-112">Methods</span></span>

<span data-ttu-id="51628-113">L’interface **IDWriteFont2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="51628-113">The **IDWriteFont2** interface has these methods.</span></span>



| <span data-ttu-id="51628-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="51628-114">Method</span></span>                                          | <span data-ttu-id="51628-115">Description</span><span class="sxs-lookup"><span data-stu-id="51628-115">Description</span></span>                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="51628-116">**IsColorFont**</span><span class="sxs-lookup"><span data-stu-id="51628-116">**IsColorFont**</span></span>](idwritefont2-iscolorfont.md) | <span data-ttu-id="51628-117">Permet de déterminer si un chemin d’accès de rendu des couleurs est potentiellement nécessaire.</span><span class="sxs-lookup"><span data-stu-id="51628-117">Enables determining if a color rendering path is potentially necessary.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="51628-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51628-118">Requirements</span></span>



| <span data-ttu-id="51628-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51628-119">Requirement</span></span> | <span data-ttu-id="51628-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="51628-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51628-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51628-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51628-122">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="51628-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="51628-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51628-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51628-124">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="51628-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="51628-125">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51628-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="51628-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="51628-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="51628-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51628-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="51628-128"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51628-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="51628-129">DLL</span><span class="sxs-lookup"><span data-stu-id="51628-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51628-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51628-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="51628-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51628-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51628-132">**IDWriteFont1**</span><span class="sxs-lookup"><span data-stu-id="51628-132">**IDWriteFont1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
</dt> </dl>

 

