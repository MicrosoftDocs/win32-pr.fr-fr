---
description: La \_ méthode put ReplicateX spécifie le nombre de fois que le modèle de réinitialisation est répliqué horizontalement.
ms.assetid: 8baa641c-c063-4c22-8b00-3559c173d627
title: IDxtJpeg ::p ut_ReplicateX, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08d892619fe1e6f8222b40d45e634a350e4e9b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532244"
---
# <a name="idxtjpegput_replicatex-method"></a><span data-ttu-id="536d3-103">IDxtJpeg ::p ut \_ ReplicateX, méthode</span><span class="sxs-lookup"><span data-stu-id="536d3-103">IDxtJpeg::put\_ReplicateX method</span></span>

> [!Note]  
> <span data-ttu-id="536d3-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="536d3-104">\[Deprecated.</span></span> <span data-ttu-id="536d3-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="536d3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="536d3-106">La `put_ReplicateX` méthode spécifie le nombre de fois que le modèle de réinitialisation est répliqué horizontalement.</span><span class="sxs-lookup"><span data-stu-id="536d3-106">The `put_ReplicateX` method specifies the number of times the wipe pattern is replicated horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="536d3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="536d3-107">Syntax</span></span>


```C++
HRESULT put_ReplicateX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="536d3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="536d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="536d3-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="536d3-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="536d3-110">Nombre de fois où le modèle de réinitialisation est répliqué horizontalement.</span><span class="sxs-lookup"><span data-stu-id="536d3-110">The number of times the wipe pattern is replicated horizontally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="536d3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="536d3-111">Return value</span></span>

<span data-ttu-id="536d3-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="536d3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="536d3-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="536d3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="536d3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="536d3-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="536d3-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="536d3-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="536d3-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="536d3-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="536d3-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="536d3-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="536d3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="536d3-118">Requirements</span></span>



| <span data-ttu-id="536d3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="536d3-119">Requirement</span></span> | <span data-ttu-id="536d3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="536d3-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="536d3-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="536d3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="536d3-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="536d3-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="536d3-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="536d3-123">Library</span></span><br/> | <dl> <span data-ttu-id="536d3-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="536d3-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="536d3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="536d3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="536d3-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="536d3-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




