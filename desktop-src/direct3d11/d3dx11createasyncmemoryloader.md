---
title: D3DX11CreateAsyncMemoryLoader, fonction (D3DX11async. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Consultez la section Notes. Créez un chargeur de mémoire asynchrone.'
ms.assetid: 0bf1e6a2-a968-4644-a7b4-e847ed4f7450
keywords:
- Fonction D3DX11CreateAsyncMemoryLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncMemoryLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16c91b0537f79fb60a5b256789c13d664401ecc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992296"
---
# <a name="d3dx11createasyncmemoryloader-function"></a><span data-ttu-id="1a847-106">D3DX11CreateAsyncMemoryLoader fonction)</span><span class="sxs-lookup"><span data-stu-id="1a847-106">D3DX11CreateAsyncMemoryLoader function</span></span>

> [!Note]  
> <span data-ttu-id="1a847-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1a847-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="1a847-108">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1a847-108">See Remarks.</span></span>

 

<span data-ttu-id="1a847-109">Créez un chargeur de mémoire asynchrone.</span><span class="sxs-lookup"><span data-stu-id="1a847-109">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a847-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a847-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="1a847-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a847-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a847-112">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a847-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a847-113">Type : **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1a847-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1a847-114">Pointeur vers les données.</span><span class="sxs-lookup"><span data-stu-id="1a847-114">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="1a847-115">*cbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a847-115">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a847-116">Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1a847-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1a847-117">Taille des données.</span><span class="sxs-lookup"><span data-stu-id="1a847-117">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="1a847-118">*ppDataLoader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1a847-118">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a847-119">Type : **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1a847-119">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="1a847-120">Adresse d’un pointeur vers le chargeur de données asynchrones (voir [**interface ID3DX11DataLoader**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="1a847-120">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a847-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a847-121">Return value</span></span>

<span data-ttu-id="1a847-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1a847-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1a847-123">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1a847-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1a847-124">Notes</span><span class="sxs-lookup"><span data-stu-id="1a847-124">Remarks</span></span>

<span data-ttu-id="1a847-125">Il n’y a aucune implémentation du chargeur asynchrone en dehors de D3DX 10 et D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="1a847-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="1a847-126">Pour les applications du Windows Store, les exemples DirectX (par exemple, l' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluent le module **BasicLoader** qui utilise le modèle de programmation asynchrone Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="1a847-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="1a847-127">Pour les applications de bureau Win32, vous pouvez utiliser le [Runtime d’accès concurrentiel](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) pour implémenter un modèle semblable au Windows Runtime modèle de programmation asynchrone.</span><span class="sxs-lookup"><span data-stu-id="1a847-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a847-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1a847-128">Requirements</span></span>



| <span data-ttu-id="1a847-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a847-129">Requirement</span></span> | <span data-ttu-id="1a847-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a847-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a847-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a847-131">Header</span></span><br/>  | <dl> <span data-ttu-id="1a847-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a847-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="1a847-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a847-133">Library</span></span><br/> | <dl> <span data-ttu-id="1a847-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a847-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1a847-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a847-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a847-136">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="1a847-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

