---
description: Définit un pointeur vers une fonction de rappel facultative qui calcule le pourcentage de calculs de l’harmonique sphérique (SH) terminé et donne à l’appelant la possibilité d’abandonner le simulateur.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'ID3DXPRTEngine :: SetCallBack, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9c2cfe710bc41ff71267e381fa0bf576688f9df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539458"
---
# <a name="id3dxprtenginesetcallback-method"></a><span data-ttu-id="9dea8-103">ID3DXPRTEngine :: SetCallBack, méthode</span><span class="sxs-lookup"><span data-stu-id="9dea8-103">ID3DXPRTEngine::SetCallBack method</span></span>

<span data-ttu-id="9dea8-104">Définit un pointeur vers une fonction de rappel facultative qui calcule le pourcentage de calculs de l’harmonique sphérique (SH) terminé et donne à l’appelant la possibilité d’abandonner le simulateur.</span><span class="sxs-lookup"><span data-stu-id="9dea8-104">Sets a pointer to an optional callback function that computes the percentage of spherical harmonic (SH) computations completed and gives the caller the option of aborting the simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dea8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9dea8-105">Syntax</span></span>


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="9dea8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9dea8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dea8-107">*PCB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9dea8-107">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dea8-108">Type : **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="9dea8-108">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="9dea8-109">Pointeur vers la fonction de rappel [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) qui calcule le pourcentage de calculs SH terminés.</span><span class="sxs-lookup"><span data-stu-id="9dea8-109">Pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that computes the percentage of SH computations completed.</span></span> <span data-ttu-id="9dea8-110">La fonction de rappel doit être implémentée pour retourner \_ OK pour continuer à exécuter le simulateur.</span><span class="sxs-lookup"><span data-stu-id="9dea8-110">The callback function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="9dea8-111">Toute autre valeur abandonne le simulateur.</span><span class="sxs-lookup"><span data-stu-id="9dea8-111">Any other value will abort the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="9dea8-112">*Fréquence* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9dea8-112">*Frequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dea8-113">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9dea8-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9dea8-114">Fréquence des appels de rappel.</span><span class="sxs-lookup"><span data-stu-id="9dea8-114">Frequency of callback calls.</span></span> <span data-ttu-id="9dea8-115">L’inverse de la fréquence est approximativement le nombre de fois où la fonction de rappel sera appelée.</span><span class="sxs-lookup"><span data-stu-id="9dea8-115">The inverse of Frequency is approximately the number of times the callback function will be called.</span></span>

</dd> <dt>

<span data-ttu-id="9dea8-116">*lpUserContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9dea8-116">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dea8-117">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9dea8-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9dea8-118">Pointeur vers une valeur définie par l’utilisateur qui est passée à la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="9dea8-118">Pointer to a user-defined value which is passed to the callback function.</span></span> <span data-ttu-id="9dea8-119">Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="9dea8-119">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dea8-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9dea8-120">Return value</span></span>

<span data-ttu-id="9dea8-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9dea8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9dea8-122">La valeur de retour est \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9dea8-122">The return value is S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dea8-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dea8-123">Requirements</span></span>



| <span data-ttu-id="9dea8-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9dea8-124">Requirement</span></span> | <span data-ttu-id="9dea8-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dea8-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dea8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9dea8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9dea8-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dea8-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9dea8-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9dea8-128">Library</span></span><br/> | <dl> <span data-ttu-id="9dea8-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9dea8-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9dea8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dea8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dea8-131">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="9dea8-131">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
