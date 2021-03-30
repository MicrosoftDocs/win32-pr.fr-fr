---
title: D3DX11CreateThreadPump, fonction (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Consultez la section Notes. Créer une pompe de thread.'
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- Fonction D3DX11CreateThreadPump Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5551cd22a4c134570c2059cc6aeaa9538311b19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974602"
---
# <a name="d3dx11createthreadpump-function"></a><span data-ttu-id="3859a-106">D3DX11CreateThreadPump fonction)</span><span class="sxs-lookup"><span data-stu-id="3859a-106">D3DX11CreateThreadPump function</span></span>

> [!Note]  
> <span data-ttu-id="3859a-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="3859a-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="3859a-108">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="3859a-108">See Remarks.</span></span>

 

<span data-ttu-id="3859a-109">Créer une pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="3859a-109">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="3859a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3859a-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="3859a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3859a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3859a-112">*cIoThreads* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3859a-112">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3859a-113">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3859a-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3859a-114">Nombre de threads d’e/s à créer.</span><span class="sxs-lookup"><span data-stu-id="3859a-114">The number of I/O threads to create.</span></span> <span data-ttu-id="3859a-115">Si la valeur 0 est spécifiée, Direct3D tente de calculer le nombre optimal de threads en fonction de la configuration matérielle.</span><span class="sxs-lookup"><span data-stu-id="3859a-115">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="3859a-116">*cProcThreads* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3859a-116">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3859a-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3859a-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3859a-118">Nombre de threads de processus à créer.</span><span class="sxs-lookup"><span data-stu-id="3859a-118">The number of process threads to create.</span></span> <span data-ttu-id="3859a-119">Si la valeur 0 est spécifiée, Direct3D tente de calculer le nombre optimal de threads en fonction de la configuration matérielle.</span><span class="sxs-lookup"><span data-stu-id="3859a-119">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="3859a-120">*ppThreadPump* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3859a-120">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3859a-121">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3859a-121">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span></span>

<span data-ttu-id="3859a-122">Pompe de thread créée.</span><span class="sxs-lookup"><span data-stu-id="3859a-122">The created thread pump.</span></span> <span data-ttu-id="3859a-123">Voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="3859a-123">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3859a-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3859a-124">Return value</span></span>

<span data-ttu-id="3859a-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3859a-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3859a-126">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3859a-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3859a-127">Notes</span><span class="sxs-lookup"><span data-stu-id="3859a-127">Remarks</span></span>

<span data-ttu-id="3859a-128">Une pompe de thread est un objet très gourmand en ressources.</span><span class="sxs-lookup"><span data-stu-id="3859a-128">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="3859a-129">Une seule pompe de threads doit être créée par application.</span><span class="sxs-lookup"><span data-stu-id="3859a-129">Only one thread pump should be created per application.</span></span>

<span data-ttu-id="3859a-130">Il n’y a aucune implémentation du chargeur asynchrone en dehors de D3DX 10 et D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="3859a-130">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="3859a-131">Pour les applications du Windows Store, les exemples DirectX (par exemple, l' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluent le module **BasicLoader** qui utilise le modèle de programmation asynchrone Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="3859a-131">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="3859a-132">Pour les applications de bureau Win32, vous pouvez utiliser le [Runtime d’accès concurrentiel](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) pour implémenter un modèle semblable au Windows Runtime modèle de programmation asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3859a-132">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="3859a-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3859a-133">Requirements</span></span>



| <span data-ttu-id="3859a-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3859a-134">Requirement</span></span> | <span data-ttu-id="3859a-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="3859a-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3859a-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="3859a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="3859a-137"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3859a-137"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="3859a-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3859a-138">Library</span></span><br/> | <dl> <span data-ttu-id="3859a-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3859a-139"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3859a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3859a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3859a-141">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="3859a-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

