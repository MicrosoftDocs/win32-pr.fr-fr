---
description: La \_ méthode obtenir ScaleX récupère la quantité d’étirement horizontal de la réinitialisation.
ms.assetid: 74c3f60b-68d9-4a8e-a6e5-767ce281a9fb
title: 'IDxtJpeg :: get_ScaleX, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0532e3c068c0ea9641d1fffbcc3d1327290bae02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535996"
---
# <a name="idxtjpegget_scalex-method"></a><span data-ttu-id="ef866-103">IDxtJpeg :: obtene \_ ScaleX, méthode</span><span class="sxs-lookup"><span data-stu-id="ef866-103">IDxtJpeg::get\_ScaleX method</span></span>

> [!Note]  
> <span data-ttu-id="ef866-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ef866-104">\[Deprecated.</span></span> <span data-ttu-id="ef866-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef866-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ef866-106">La `get_ScaleX` méthode récupère la quantité par laquelle la réinitialisation est étirée horizontalement.</span><span class="sxs-lookup"><span data-stu-id="ef866-106">The `get_ScaleX` method retrieves the amount by which the wipe is stretched horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef866-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef866-107">Syntax</span></span>


```C++
HRESULT get_ScaleX(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ef866-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef866-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef866-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ef866-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ef866-110">Reçoit la valeur par laquelle la réinitialisation est étirée horizontalement, sous la forme d’un pourcentage de la définition de la réinitialisation d’origine.</span><span class="sxs-lookup"><span data-stu-id="ef866-110">Receives the amount by which the wipe is stretched horizontally, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="ef866-111">Par exemple, la valeur 1,0 signifie aucun étirement, et 2,0 signifie l’étirement de 200%.</span><span class="sxs-lookup"><span data-stu-id="ef866-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef866-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef866-112">Return value</span></span>

<span data-ttu-id="ef866-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ef866-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ef866-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef866-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef866-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ef866-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ef866-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="ef866-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ef866-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ef866-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ef866-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ef866-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef866-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef866-119">Requirements</span></span>



| <span data-ttu-id="ef866-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef866-120">Requirement</span></span> | <span data-ttu-id="ef866-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef866-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef866-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef866-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ef866-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef866-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ef866-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef866-124">Library</span></span><br/> | <dl> <span data-ttu-id="ef866-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef866-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef866-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef866-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef866-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="ef866-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




