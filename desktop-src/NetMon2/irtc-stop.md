---
description: La méthode Stop arrête la capture en cours.
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'IRTC :: Stop, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f25bf9d56a6f41acefad9a552dd2f591158bc74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519636"
---
# <a name="irtcstop-method"></a><span data-ttu-id="6a3b8-103">IRTC :: Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="6a3b8-103">IRTC::Stop method</span></span>

<span data-ttu-id="6a3b8-104">La méthode **Stop** arrête la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="6a3b8-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a3b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a3b8-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="6a3b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a3b8-106">Parameters</span></span>

<span data-ttu-id="6a3b8-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6a3b8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a3b8-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a3b8-108">Return value</span></span>

<span data-ttu-id="6a3b8-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6a3b8-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6a3b8-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="6a3b8-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="6a3b8-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6a3b8-111">Return code</span></span>                                                                                          | <span data-ttu-id="6a3b8-112">Description</span><span class="sxs-lookup"><span data-stu-id="6a3b8-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6a3b8-113"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="6a3b8-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="6a3b8-114">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="6a3b8-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="6a3b8-115">Appelez [IRTC :: Connect](irtc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="6a3b8-115">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="6a3b8-116"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="6a3b8-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="6a3b8-117">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="6a3b8-117">The NPP is not capturing data.</span></span> <span data-ttu-id="6a3b8-118">Appelez [IRTC :: Start](irtc-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="6a3b8-118">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="6a3b8-119"><dt>**NMERR \_ pas de \_ temps réel**</dt></span><span class="sxs-lookup"><span data-stu-id="6a3b8-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="6a3b8-120">Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="6a3b8-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="6a3b8-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6a3b8-121">Remarks</span></span>

<span data-ttu-id="6a3b8-122">Lorsque vous redémarrez la capture après avoir appelé la méthode **IRTC :: Stop** , veillez à appeler [IRTC :: configure](irtc-configure.md) chaque fois que vous appelez [IRTC :: Start](irtc-start.md) pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="6a3b8-122">When you restart the capture after calling the **IRTC::Stop** method, make sure to call [IRTC::Configure](irtc-configure.md) each time you call [IRTC::Start](irtc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a3b8-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a3b8-123">Requirements</span></span>



| <span data-ttu-id="6a3b8-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a3b8-124">Requirement</span></span> | <span data-ttu-id="6a3b8-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a3b8-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a3b8-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a3b8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6a3b8-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a3b8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6a3b8-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a3b8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6a3b8-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a3b8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6a3b8-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a3b8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a3b8-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a3b8-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6a3b8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6a3b8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a3b8-133"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a3b8-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a3b8-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a3b8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a3b8-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="6a3b8-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="6a3b8-136">IRTC :: Connect</span><span class="sxs-lookup"><span data-stu-id="6a3b8-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="6a3b8-137">IRTC :: configure</span><span class="sxs-lookup"><span data-stu-id="6a3b8-137">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="6a3b8-138">IRTC :: Start</span><span class="sxs-lookup"><span data-stu-id="6a3b8-138">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




