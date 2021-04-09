---
description: Objet de traitement de données utilisé par l’interface ID3DX10ThreadPump pour le traitement des données chargées de façon asynchrone.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Interface ID3DX10DataProcessor (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870213"
---
# <a name="id3dx10dataprocessor-interface"></a><span data-ttu-id="9ba17-103">Interface ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="9ba17-103">ID3DX10DataProcessor interface</span></span>

<span data-ttu-id="9ba17-104">Objet de traitement de données utilisé par l' [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour le traitement des données chargées de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="9ba17-104">Data processing object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for processing loaded data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="9ba17-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9ba17-105">Members</span></span>

<span data-ttu-id="9ba17-106">L’interface **ID3DX10DataProcessor** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9ba17-106">The **ID3DX10DataProcessor** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9ba17-107">**ID3DX10DataProcessor** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9ba17-107">**ID3DX10DataProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="9ba17-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9ba17-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9ba17-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9ba17-109">Methods</span></span>

<span data-ttu-id="9ba17-110">L’interface **ID3DX10DataProcessor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9ba17-110">The **ID3DX10DataProcessor** interface has these methods.</span></span>



| <span data-ttu-id="9ba17-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="9ba17-111">Method</span></span>                                                                | <span data-ttu-id="9ba17-112">Description</span><span class="sxs-lookup"><span data-stu-id="9ba17-112">Description</span></span>                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ba17-113">**CreateDeviceObject**</span><span class="sxs-lookup"><span data-stu-id="9ba17-113">**CreateDeviceObject**</span></span>](id3dx10dataprocessor-createdeviceobject.md) | <span data-ttu-id="9ba17-114">Créez un objet d’appareil.</span><span class="sxs-lookup"><span data-stu-id="9ba17-114">Create a device object.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="9ba17-115">**Suppression**</span><span class="sxs-lookup"><span data-stu-id="9ba17-115">**Destroy**</span></span>](id3dx10dataprocessor-destroy.md)                       | <span data-ttu-id="9ba17-116">Utilisé par une [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour détruire le processeur après l’achèvement d’un élément de travail.</span><span class="sxs-lookup"><span data-stu-id="9ba17-116">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the processor after a work item completes.</span></span><br/> |
| [<span data-ttu-id="9ba17-117">**Processus**</span><span class="sxs-lookup"><span data-stu-id="9ba17-117">**Process**</span></span>](id3dx10dataprocessor-process.md)                       | <span data-ttu-id="9ba17-118">Traitez des données.</span><span class="sxs-lookup"><span data-stu-id="9ba17-118">Process some data.</span></span><br/>                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="9ba17-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9ba17-119">Remarks</span></span>

<span data-ttu-id="9ba17-120">Cet objet peut être hérité et ses membres redéfinis.</span><span class="sxs-lookup"><span data-stu-id="9ba17-120">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="9ba17-121">Cela vous permettrait de personnaliser l’API pour le traitement de vos propres formats de fichier personnalisés.</span><span class="sxs-lookup"><span data-stu-id="9ba17-121">Doing so would enable you to customize the API for processing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba17-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ba17-122">Requirements</span></span>



| <span data-ttu-id="9ba17-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ba17-123">Requirement</span></span> | <span data-ttu-id="9ba17-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ba17-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba17-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ba17-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9ba17-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ba17-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ba17-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ba17-127">Library</span></span><br/> | <dl> <span data-ttu-id="9ba17-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ba17-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba17-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ba17-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba17-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="9ba17-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
