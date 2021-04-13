---
description: Non implémenté.
ms.assetid: 25300ba5-3578-4eb3-99e2-d547dbb2b9ee
title: IXml2Dex ::P méthode asteXMLFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.PasteXMLFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1e6df8679dde95e7483fe74eb0d8b1b462d51730
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481320"
---
# <a name="ixml2dexpastexmlfile-method"></a><span data-ttu-id="bd179-103">IXml2Dex ::P méthode asteXMLFile</span><span class="sxs-lookup"><span data-stu-id="bd179-103">IXml2Dex::PasteXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="bd179-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="bd179-104">\[Deprecated.</span></span> <span data-ttu-id="bd179-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bd179-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bd179-106">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="bd179-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd179-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd179-107">Syntax</span></span>


```C++
HRESULT PasteXMLFile(
   IUnknown *pTimeline,
   double   dStart,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="bd179-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd179-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd179-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="bd179-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="bd179-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bd179-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bd179-111">*dStart*</span><span class="sxs-lookup"><span data-stu-id="bd179-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="bd179-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bd179-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bd179-113">*FileName*</span><span class="sxs-lookup"><span data-stu-id="bd179-113">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="bd179-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bd179-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd179-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bd179-115">Return value</span></span>

<span data-ttu-id="bd179-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bd179-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bd179-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd179-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd179-118">Notes</span><span class="sxs-lookup"><span data-stu-id="bd179-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bd179-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="bd179-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bd179-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bd179-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bd179-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bd179-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="bd179-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd179-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd179-123">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="bd179-123">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



