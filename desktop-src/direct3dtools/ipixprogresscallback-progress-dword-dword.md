---
description: Rappel qui avertit l’hôte de la progression d’une demande associée.
MS-HAID: vspixengine.IPixProgressCallback\_Progress\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixProgressCallback ::P méthode rogress
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE74599B-C98F-4BDB-ACDF-641F77A35EEB
api_name:
- IPixProgressCallback.Progress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0379ad6fcb5f97825469c97af38453e55585d005
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392660"
---
# <a name="span-idvspixengineipixprogresscallback_progress_dword_dwordspanipixprogresscallbackprogress-method"></a><span data-ttu-id="e9140-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback ::P méthode rogress</span><span class="sxs-lookup"><span data-stu-id="e9140-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback::Progress method</span></span>

<span data-ttu-id="e9140-104">Rappel qui avertit l’hôte de la progression d’une demande associée.</span><span class="sxs-lookup"><span data-stu-id="e9140-104">A callback that notifies the host of the progress of an associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9140-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9140-105">Syntax</span></span>


```C++
HRESULT Progress(
   DWORD current,
   DWORD maxSize
);
```

## <a name="parameters"></a><span data-ttu-id="e9140-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9140-106">Parameters</span></span>

<span data-ttu-id="e9140-107">*actif* </span><span class="sxs-lookup"><span data-stu-id="e9140-107">*current* </span></span>  
<span data-ttu-id="e9140-108">La partie d’une requête est terminée, en tant que nombre d’étapes terminées.</span><span class="sxs-lookup"><span data-stu-id="e9140-108">The portion of a request completed, as a count of the number of steps completed.</span></span>

<span data-ttu-id="e9140-109">*maxSize* </span><span class="sxs-lookup"><span data-stu-id="e9140-109">*maxSize* </span></span>  
<span data-ttu-id="e9140-110">Nombre total d’étapes pour effectuer la demande.</span><span class="sxs-lookup"><span data-stu-id="e9140-110">The total number of steps to complete the request.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9140-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9140-111">Return value</span></span>

<span data-ttu-id="e9140-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e9140-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9140-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e9140-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9140-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9140-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e9140-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9140-115">Header</span></span></p></td><td><span data-ttu-id="e9140-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e9140-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e9140-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9140-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e9140-118">**IPixProgressCallback**</span><span class="sxs-lookup"><span data-stu-id="e9140-118">**IPixProgressCallback**</span></span>](/windows/desktop/direct3dtools/ipixprogresscallback)

 

 
