---
description: 'IRTC :: Stop, méthode : la méthode Stop arrête la capture en cours.'
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
ms.openlocfilehash: 10bf0886032c93288435ade05fec46077d53753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113517"
---
# <a name="irtcstop-method"></a><span data-ttu-id="3c44b-103">IRTC :: Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="3c44b-103">IRTC::Stop method</span></span>

<span data-ttu-id="3c44b-104">La méthode **Stop** arrête la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="3c44b-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c44b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c44b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="3c44b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c44b-106">Parameters</span></span>

<span data-ttu-id="3c44b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3c44b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c44b-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3c44b-108">Return value</span></span>

<span data-ttu-id="3c44b-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3c44b-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3c44b-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="3c44b-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="3c44b-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3c44b-111">Return code</span></span>                                                                                          | <span data-ttu-id="3c44b-112">Description</span><span class="sxs-lookup"><span data-stu-id="3c44b-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c44b-113"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="3c44b-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3c44b-114">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="3c44b-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="3c44b-115">Appelez [IRTC :: Connect](irtc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="3c44b-115">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="3c44b-116"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="3c44b-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="3c44b-117">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="3c44b-117">The NPP is not capturing data.</span></span> <span data-ttu-id="3c44b-118">Appelez [IRTC :: Start](irtc-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="3c44b-118">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="3c44b-119"><dt>**NMERR \_ pas de \_ temps réel**</dt></span><span class="sxs-lookup"><span data-stu-id="3c44b-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="3c44b-120">Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="3c44b-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="3c44b-121">Notes </span><span class="sxs-lookup"><span data-stu-id="3c44b-121">Remarks</span></span>

<span data-ttu-id="3c44b-122">Lorsque vous redémarrez la capture après avoir appelé la méthode **IRTC :: Stop** , veillez à appeler [IRTC :: configure](irtc-configure.md) chaque fois que vous appelez [IRTC :: Start](irtc-start.md) pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="3c44b-122">When you restart the capture after calling the **IRTC::Stop** method, make sure to call [IRTC::Configure](irtc-configure.md) each time you call [IRTC::Start](irtc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c44b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c44b-123">Requirements</span></span>



| <span data-ttu-id="3c44b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c44b-124">Requirement</span></span> | <span data-ttu-id="3c44b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c44b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c44b-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c44b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3c44b-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c44b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="3c44b-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c44b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3c44b-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c44b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="3c44b-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c44b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c44b-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c44b-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="3c44b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3c44b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c44b-133"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c44b-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c44b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c44b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c44b-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="3c44b-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="3c44b-136">IRTC :: Connect</span><span class="sxs-lookup"><span data-stu-id="3c44b-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="3c44b-137">IRTC :: configure</span><span class="sxs-lookup"><span data-stu-id="3c44b-137">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="3c44b-138">IRTC :: Start</span><span class="sxs-lookup"><span data-stu-id="3c44b-138">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




