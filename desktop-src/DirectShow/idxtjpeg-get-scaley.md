---
description: La \_ méthode d’extraction à l’échelle récupère la quantité par laquelle la réinitialisation est étirée verticalement.
ms.assetid: d8b80f19-2ec5-4d66-bd13-d6f7b5144345
title: 'IDxtJpeg :: get_ScaleY, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4ca3feb0177ad1c9172721ca312e810fdb105b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526370"
---
# <a name="idxtjpegget_scaley-method"></a><span data-ttu-id="56730-103">IDxtJpeg :: obtient la \_ méthode ScaleY</span><span class="sxs-lookup"><span data-stu-id="56730-103">IDxtJpeg::get\_ScaleY method</span></span>

> [!Note]  
> <span data-ttu-id="56730-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="56730-104">\[Deprecated.</span></span> <span data-ttu-id="56730-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="56730-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="56730-106">La `get_ScaleY` méthode récupère la valeur de l’étirement vertical de la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="56730-106">The `get_ScaleY` method retrieves the amount by which the wipe is stretched vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="56730-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56730-107">Syntax</span></span>


```C++
HRESULT get_ScaleY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="56730-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56730-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56730-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="56730-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="56730-110">Reçoit la valeur par laquelle la réinitialisation est étirée verticalement, sous la forme d’un pourcentage de la définition de la réinitialisation d’origine.</span><span class="sxs-lookup"><span data-stu-id="56730-110">Receives the amount by which the wipe is stretched vertically, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="56730-111">Par exemple, la valeur 1,0 signifie aucun étirement, et 2,0 signifie l’étirement de 200%.</span><span class="sxs-lookup"><span data-stu-id="56730-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56730-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56730-112">Return value</span></span>

<span data-ttu-id="56730-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="56730-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56730-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56730-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="56730-115">Notes</span><span class="sxs-lookup"><span data-stu-id="56730-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="56730-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="56730-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="56730-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="56730-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="56730-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="56730-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56730-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56730-119">Requirements</span></span>



| <span data-ttu-id="56730-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56730-120">Requirement</span></span> | <span data-ttu-id="56730-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="56730-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56730-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="56730-122">Header</span></span><br/>  | <dl> <span data-ttu-id="56730-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="56730-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="56730-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="56730-124">Library</span></span><br/> | <dl> <span data-ttu-id="56730-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56730-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56730-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56730-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56730-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="56730-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




