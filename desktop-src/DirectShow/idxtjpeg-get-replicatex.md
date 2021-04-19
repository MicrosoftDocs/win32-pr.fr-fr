---
description: La \_ méthode obtenir ReplicateX récupère le nombre de fois où le modèle de réinitialisation est répliqué horizontalement.
ms.assetid: 669a3bde-af8b-4d31-b914-41b71c95de1c
title: 'IDxtJpeg :: get_ReplicateX, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ReplicateX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8855f819cb00d46297220c41deb6b81d6150e0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521643"
---
# <a name="idxtjpegget_replicatex-method"></a><span data-ttu-id="062c6-103">IDxtJpeg :: \_ ReplicateX, méthode</span><span class="sxs-lookup"><span data-stu-id="062c6-103">IDxtJpeg::get\_ReplicateX method</span></span>

> [!Note]  
> <span data-ttu-id="062c6-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="062c6-104">\[Deprecated.</span></span> <span data-ttu-id="062c6-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="062c6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="062c6-106">La `get_ReplicateX` méthode récupère le nombre de fois où le modèle de réinitialisation est répliqué horizontalement.</span><span class="sxs-lookup"><span data-stu-id="062c6-106">The `get_ReplicateX` method retrieves the number of times the wipe pattern is replicated horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="062c6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="062c6-107">Syntax</span></span>


```C++
HRESULT get_ReplicateX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="062c6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="062c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="062c6-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="062c6-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="062c6-110">Reçoit le nombre de fois que le modèle de réinitialisation est répliqué horizontalement.</span><span class="sxs-lookup"><span data-stu-id="062c6-110">Receives the number of times the wipe pattern is replicated horizontally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="062c6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="062c6-111">Return value</span></span>

<span data-ttu-id="062c6-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="062c6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="062c6-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="062c6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="062c6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="062c6-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="062c6-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="062c6-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="062c6-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="062c6-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="062c6-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="062c6-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="062c6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="062c6-118">Requirements</span></span>



| <span data-ttu-id="062c6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="062c6-119">Requirement</span></span> | <span data-ttu-id="062c6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="062c6-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="062c6-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="062c6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="062c6-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="062c6-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="062c6-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="062c6-123">Library</span></span><br/> | <dl> <span data-ttu-id="062c6-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="062c6-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="062c6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="062c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="062c6-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="062c6-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




