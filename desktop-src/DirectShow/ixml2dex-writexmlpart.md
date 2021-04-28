---
description: 'Méthode IXml2Dex :: WriteXMLPart-non implémentée.'
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: 'IXml2Dex :: WriteXMLPart, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 957fa74f09a79f94e2e0feb35c418a711c91c1b0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084357"
---
# <a name="ixml2dexwritexmlpart-method"></a><span data-ttu-id="a1f95-103">IXml2Dex :: WriteXMLPart, méthode</span><span class="sxs-lookup"><span data-stu-id="a1f95-103">IXml2Dex::WriteXMLPart method</span></span>

> [!Note]  
> <span data-ttu-id="a1f95-104">\[Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="a1f95-104">\[Deprecated.</span></span> <span data-ttu-id="a1f95-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a1f95-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a1f95-106">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="a1f95-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f95-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1f95-107">Syntax</span></span>


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="a1f95-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1f95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1f95-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="a1f95-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="a1f95-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a1f95-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a1f95-111">*dStart*</span><span class="sxs-lookup"><span data-stu-id="a1f95-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="a1f95-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a1f95-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a1f95-113">*dEnd*</span><span class="sxs-lookup"><span data-stu-id="a1f95-113">*dEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a1f95-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a1f95-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a1f95-115">*FileName*</span><span class="sxs-lookup"><span data-stu-id="a1f95-115">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="a1f95-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a1f95-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1f95-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a1f95-117">Return value</span></span>

<span data-ttu-id="a1f95-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a1f95-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1f95-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a1f95-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1f95-120">Notes </span><span class="sxs-lookup"><span data-stu-id="a1f95-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a1f95-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="a1f95-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a1f95-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a1f95-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a1f95-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a1f95-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="a1f95-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1f95-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f95-125">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="a1f95-125">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



