---
title: ISoftKbd Initialize, méthode (Softkbdc. h)
description: La méthode Initialize ISoftKbd initialise tous les champs nécessaires pour un clavier logiciel et génère des dispositions de clavier souples standard.
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Initialiser la méthode Text Services Framework
- Initialiser la méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, Initialize, méthode
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740205"
---
# <a name="isoftkbdinitialize-method"></a><span data-ttu-id="2bc1e-106">ISoftKbd :: Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="2bc1e-106">ISoftKbd::Initialize method</span></span>

<span data-ttu-id="2bc1e-107">La méthode **ISoftKbd :: Initialize** initialise tous les champs nécessaires pour un clavier conditionnel et génère des dispositions de clavier souples standard.</span><span class="sxs-lookup"><span data-stu-id="2bc1e-107">The **ISoftKbd::Initialize** method initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bc1e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bc1e-108">Syntax</span></span>


```C++
HRESULT Initialize();
```



## <a name="parameters"></a><span data-ttu-id="2bc1e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bc1e-109">Parameters</span></span>

<span data-ttu-id="2bc1e-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2bc1e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bc1e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2bc1e-111">Return value</span></span>

<span data-ttu-id="2bc1e-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2bc1e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2bc1e-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bc1e-113">Value</span></span>                                                                                | <span data-ttu-id="2bc1e-114">Description</span><span class="sxs-lookup"><span data-stu-id="2bc1e-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2bc1e-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2bc1e-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2bc1e-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="2bc1e-116">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2bc1e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bc1e-117">Requirements</span></span>



| <span data-ttu-id="2bc1e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bc1e-118">Requirement</span></span> | <span data-ttu-id="2bc1e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bc1e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc1e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bc1e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc1e-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bc1e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2bc1e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bc1e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc1e-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bc1e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2bc1e-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2bc1e-124">Redistributable</span></span><br/>          | <span data-ttu-id="2bc1e-125">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="2bc1e-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="2bc1e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2bc1e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bc1e-127"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bc1e-127"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="2bc1e-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="2bc1e-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2bc1e-129"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2bc1e-129"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="2bc1e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2bc1e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bc1e-131"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bc1e-131"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bc1e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bc1e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc1e-133">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="2bc1e-133">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





