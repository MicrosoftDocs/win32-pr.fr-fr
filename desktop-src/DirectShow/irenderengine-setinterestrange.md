---
description: 'IRenderEngine :: SetInterestRange, méthode non prise en charge.'
ms.assetid: 1e4c3bd4-2540-428f-9ca6-dd4c65c53434
title: 'IRenderEngine :: SetInterestRange, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetInterestRange
api_type:
- COM
api_location: ''
ms.openlocfilehash: ec9790e65efa30b83cf324da4153f20c541733b9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084457"
---
# <a name="irenderenginesetinterestrange-method"></a><span data-ttu-id="224c3-103">IRenderEngine :: SetInterestRange, méthode</span><span class="sxs-lookup"><span data-stu-id="224c3-103">IRenderEngine::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="224c3-104">\[Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="224c3-104">\[Deprecated.</span></span> <span data-ttu-id="224c3-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="224c3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="224c3-106">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="224c3-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="224c3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="224c3-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="224c3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="224c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="224c3-109">*Start*</span><span class="sxs-lookup"><span data-stu-id="224c3-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="224c3-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="224c3-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="224c3-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="224c3-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="224c3-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="224c3-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="224c3-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="224c3-113">Return value</span></span>

<span data-ttu-id="224c3-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="224c3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="224c3-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="224c3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="224c3-116">Notes </span><span class="sxs-lookup"><span data-stu-id="224c3-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="224c3-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="224c3-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="224c3-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="224c3-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="224c3-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="224c3-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="224c3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="224c3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224c3-121">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="224c3-121">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> </dl>

 

 



