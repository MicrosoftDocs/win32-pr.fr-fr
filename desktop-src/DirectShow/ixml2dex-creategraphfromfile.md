---
description: Non implémenté.
ms.assetid: b476e0c9-1432-4644-8002-154797a2a594
title: 'IXml2Dex :: CreateGraphFromFile, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.CreateGraphFromFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 10a2e52716de77f9c62a51c87cbda550b92a8f90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513282"
---
# <a name="ixml2dexcreategraphfromfile-method"></a><span data-ttu-id="5a9d2-103">IXml2Dex :: CreateGraphFromFile, méthode</span><span class="sxs-lookup"><span data-stu-id="5a9d2-103">IXml2Dex::CreateGraphFromFile method</span></span>

> [!Note]  
> <span data-ttu-id="5a9d2-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5a9d2-104">\[Deprecated.</span></span> <span data-ttu-id="5a9d2-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5a9d2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5a9d2-106">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="5a9d2-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a9d2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a9d2-107">Syntax</span></span>


```C++
HRESULT CreateGraphFromFile(
   IUnknown **ppGraph,
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="5a9d2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a9d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a9d2-109">*ppGraph*</span><span class="sxs-lookup"><span data-stu-id="5a9d2-109">*ppGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9d2-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5a9d2-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5a9d2-111">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="5a9d2-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9d2-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5a9d2-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5a9d2-113">*FileName*</span><span class="sxs-lookup"><span data-stu-id="5a9d2-113">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9d2-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5a9d2-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a9d2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a9d2-115">Return value</span></span>

<span data-ttu-id="5a9d2-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5a9d2-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a9d2-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a9d2-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a9d2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5a9d2-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5a9d2-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="5a9d2-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5a9d2-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5a9d2-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5a9d2-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5a9d2-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5a9d2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a9d2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a9d2-123">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="5a9d2-123">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



