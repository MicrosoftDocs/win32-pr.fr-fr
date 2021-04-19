---
description: La \_ méthode obtenir la réplication récupère le nombre de fois où le modèle de réinitialisation est répliqué verticalement.
ms.assetid: 347e1ffa-bb39-4980-b8af-5806a23d1334
title: 'IDxtJpeg :: get_ReplicateY, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ae5c68d153b64783f84a6c4c4a8ba7f5d5f0f24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543351"
---
# <a name="idxtjpegget_replicatey-method"></a><span data-ttu-id="c1ec4-103">IDxtJpeg :: obtient la \_ méthode de réplication</span><span class="sxs-lookup"><span data-stu-id="c1ec4-103">IDxtJpeg::get\_ReplicateY method</span></span>

> [!Note]  
> <span data-ttu-id="c1ec4-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c1ec4-104">\[Deprecated.</span></span> <span data-ttu-id="c1ec4-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c1ec4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c1ec4-106">La `get_ReplicateY` méthode récupère le nombre de fois où le modèle de réinitialisation est répliqué verticalement.</span><span class="sxs-lookup"><span data-stu-id="c1ec4-106">The `get_ReplicateY` method retrieves the number of times the wipe pattern is replicated vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1ec4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1ec4-107">Syntax</span></span>


```C++
HRESULT get_ReplicateY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c1ec4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1ec4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1ec4-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c1ec4-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c1ec4-110">Reçoit le nombre de fois que le modèle de réinitialisation est répliqué verticalement.</span><span class="sxs-lookup"><span data-stu-id="c1ec4-110">Receives the number of times the wipe pattern is replicated vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1ec4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1ec4-111">Return value</span></span>

<span data-ttu-id="c1ec4-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c1ec4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c1ec4-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1ec4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1ec4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c1ec4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c1ec4-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="c1ec4-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c1ec4-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c1ec4-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c1ec4-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c1ec4-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1ec4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1ec4-118">Requirements</span></span>



| <span data-ttu-id="c1ec4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1ec4-119">Requirement</span></span> | <span data-ttu-id="c1ec4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1ec4-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ec4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1ec4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c1ec4-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1ec4-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c1ec4-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c1ec4-123">Library</span></span><br/> | <dl> <span data-ttu-id="c1ec4-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1ec4-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1ec4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1ec4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1ec4-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="c1ec4-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




