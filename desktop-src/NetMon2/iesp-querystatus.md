---
description: Récupère l’État NPP.
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: 'IESP :: QueryStatus, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3435ed832484042bfeb9229e4b46fa34441cb395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202311"
---
# <a name="iespquerystatus-method"></a><span data-ttu-id="73dfb-103">IESP :: QueryStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="73dfb-103">IESP::QueryStatus method</span></span>

<span data-ttu-id="73dfb-104">La méthode **QueryStatus** récupère l’État NPP.</span><span class="sxs-lookup"><span data-stu-id="73dfb-104">The **QueryStatus** method retrieves the NPP status.</span></span>

## <a name="syntax"></a><span data-ttu-id="73dfb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73dfb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="73dfb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73dfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73dfb-107">*pNetworkStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="73dfb-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73dfb-108">Pointeur vers une structure [NETWORKSTATUS](networkstatus.md) retournée qui indique l’état actuel (capture, pause, arrêtée, etc.) du NPP.</span><span class="sxs-lookup"><span data-stu-id="73dfb-108">A pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="73dfb-109">L’utilisateur doit allouer et libérer la mémoire pour la structure NETWORKSTATUS.</span><span class="sxs-lookup"><span data-stu-id="73dfb-109">The user must allocate and free the memory for the NETWORKSTATUS structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73dfb-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73dfb-110">Return value</span></span>

<span data-ttu-id="73dfb-111">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="73dfb-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="73dfb-112">Si la méthode échoue, la valeur de retour est le code d’erreur suivant :</span><span class="sxs-lookup"><span data-stu-id="73dfb-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="73dfb-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="73dfb-113">Return code</span></span>                                                                                              | <span data-ttu-id="73dfb-114">Description</span><span class="sxs-lookup"><span data-stu-id="73dfb-114">Description</span></span>                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73dfb-115"><dt>**\_paramètre NMERR non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="73dfb-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="73dfb-116">Le paramètre *pNetworkStatus* ne pointe pas vers une structure [NETWORKSTATUS](networkstatus.md) valide.</span><span class="sxs-lookup"><span data-stu-id="73dfb-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="73dfb-117">Allouez de la mémoire pour cette structure et appelez à nouveau **IESP :: QueryStatus** .</span><span class="sxs-lookup"><span data-stu-id="73dfb-117">Allocate memory for this structure and call **IESP::QueryStatus** again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73dfb-118">Notes</span><span class="sxs-lookup"><span data-stu-id="73dfb-118">Remarks</span></span>

<span data-ttu-id="73dfb-119">Cette méthode peut être appelée à tout moment après l’appel de [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="73dfb-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="73dfb-120">Vous pouvez appeler cette méthode pour voir si le NPP est connecté au réseau, pour déterminer l’état de la capture en cours et pour déterminer si des déclencheurs sont en attente.</span><span class="sxs-lookup"><span data-stu-id="73dfb-120">You can call this method to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="73dfb-121">Avant d’appeler cette méthode, allouez la mémoire requise pour la structure [NETWORKSTATUS](networkstatus.md) et libérez cette mémoire lorsque la structure n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="73dfb-121">Before calling this method, allocate the memory required for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer required.</span></span>

## <a name="requirements"></a><span data-ttu-id="73dfb-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73dfb-122">Requirements</span></span>



| <span data-ttu-id="73dfb-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73dfb-123">Requirement</span></span> | <span data-ttu-id="73dfb-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="73dfb-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73dfb-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73dfb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="73dfb-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73dfb-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="73dfb-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73dfb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="73dfb-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73dfb-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="73dfb-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="73dfb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="73dfb-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="73dfb-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="73dfb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="73dfb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73dfb-132"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73dfb-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73dfb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73dfb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73dfb-134">IESP</span><span class="sxs-lookup"><span data-stu-id="73dfb-134">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="73dfb-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="73dfb-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="73dfb-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="73dfb-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




