---
description: Rappel qui avertit l’hôte des erreurs retournées par la requête associée.
MS-HAID: vspixengine.IPixErrorCallback\_ErrorListCallback\_DWORD\_Issue\_arr\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixErrorCallback :: ErrorListCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B345846D-4853-4F6B-AB79-42265720451D
api_name:
- IPixErrorCallback.ErrorListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 91754cd7db13165efcb66e9bc87b8e4661842fce
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514730"
---
# <a name="span-idvspixengineipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arrspanipixerrorcallbackerrorlistcallback-method"></a><span data-ttu-id="6e097-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>IPixErrorCallback :: ErrorListCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="6e097-103"><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>IPixErrorCallback::ErrorListCallback method</span></span>

<span data-ttu-id="6e097-104">Rappel qui avertit l’hôte des erreurs retournées par la requête associée.</span><span class="sxs-lookup"><span data-stu-id="6e097-104">A callback that notifies the host of errors returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e097-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e097-105">Syntax</span></span>


```C++
HRESULT ErrorListCallback(
   DWORD    count,
   Issue [] count0_errorList,
   DWORD    count,
   Issue [] count0_warningList
);
```

## <a name="parameters"></a><span data-ttu-id="6e097-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e097-106">Parameters</span></span>

<span data-ttu-id="6e097-107">*saut* </span><span class="sxs-lookup"><span data-stu-id="6e097-107">*count* </span></span>  
<span data-ttu-id="6e097-108">Nombre d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="6e097-108">The number of errors.</span></span>

<span data-ttu-id="6e097-109">*count0 \_ Erreurs* </span><span class="sxs-lookup"><span data-stu-id="6e097-109">*count0\_errorList* </span></span>  
<span data-ttu-id="6e097-110">Erreurs.</span><span class="sxs-lookup"><span data-stu-id="6e097-110">The errors.</span></span>

<span data-ttu-id="6e097-111">*saut* </span><span class="sxs-lookup"><span data-stu-id="6e097-111">*count* </span></span>  
<span data-ttu-id="6e097-112">Nombre de warningns.</span><span class="sxs-lookup"><span data-stu-id="6e097-112">The number of warningns.</span></span>

<span data-ttu-id="6e097-113">*count0 \_ warningList* </span><span class="sxs-lookup"><span data-stu-id="6e097-113">*count0\_warningList* </span></span>  
<span data-ttu-id="6e097-114">Avertissements.</span><span class="sxs-lookup"><span data-stu-id="6e097-114">The warnings.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e097-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e097-115">Return value</span></span>

<span data-ttu-id="6e097-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6e097-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e097-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e097-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e097-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e097-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6e097-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e097-119">Header</span></span></p></td><td><span data-ttu-id="6e097-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6e097-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6e097-121"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e097-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6e097-122">**IPixErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="6e097-122">**IPixErrorCallback**</span></span>](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
