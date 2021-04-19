---
description: La méthode ApplyChanges applique toutes les propriétés qui ont été modifiées.
ms.assetid: dece1e61-7fe1-40f1-8d1d-89b5a334d04e
title: 'IDxtJpeg :: ApplyChanges, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.ApplyChanges
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 522df2fc362b0332d4eb41e9a2f10201bfcdec9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537422"
---
# <a name="idxtjpegapplychanges-method"></a><span data-ttu-id="bad9b-103">IDxtJpeg :: ApplyChanges, méthode</span><span class="sxs-lookup"><span data-stu-id="bad9b-103">IDxtJpeg::ApplyChanges method</span></span>

> [!Note]  
> <span data-ttu-id="bad9b-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="bad9b-104">\[Deprecated.</span></span> <span data-ttu-id="bad9b-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bad9b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bad9b-106">La `ApplyChanges` méthode applique toutes les propriétés qui ont changé.</span><span class="sxs-lookup"><span data-stu-id="bad9b-106">The `ApplyChanges` method applies any properties that have changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad9b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bad9b-107">Syntax</span></span>


```C++
HRESULT ApplyChanges();
```



## <a name="parameters"></a><span data-ttu-id="bad9b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bad9b-108">Parameters</span></span>

<span data-ttu-id="bad9b-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bad9b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bad9b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bad9b-110">Return value</span></span>

<span data-ttu-id="bad9b-111">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bad9b-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bad9b-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bad9b-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bad9b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bad9b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bad9b-114">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="bad9b-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bad9b-115">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bad9b-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bad9b-116">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bad9b-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bad9b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bad9b-117">Requirements</span></span>



| <span data-ttu-id="bad9b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bad9b-118">Requirement</span></span> | <span data-ttu-id="bad9b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bad9b-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bad9b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bad9b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bad9b-121"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad9b-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bad9b-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bad9b-122">Library</span></span><br/> | <dl> <span data-ttu-id="bad9b-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bad9b-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bad9b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bad9b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad9b-125">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="bad9b-125">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




