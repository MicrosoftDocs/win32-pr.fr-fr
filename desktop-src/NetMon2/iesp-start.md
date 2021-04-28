---
description: 'IESP :: Start, méthode-la méthode start démarre une capture.'
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'IESP :: Start, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 6dd0d1159132e594b6d48ea6799da5846eeb626e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103797"
---
# <a name="iespstart-method"></a><span data-ttu-id="2c08f-103">IESP :: Start, méthode</span><span class="sxs-lookup"><span data-stu-id="2c08f-103">IESP::Start method</span></span>

<span data-ttu-id="2c08f-104">La méthode **Start** démarre une capture.</span><span class="sxs-lookup"><span data-stu-id="2c08f-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c08f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c08f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="2c08f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c08f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c08f-107">*pFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2c08f-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c08f-108">Pointeur vers le nom du [*fichier de capture*](c.md) utilisé pour stocker les données réseau.</span><span class="sxs-lookup"><span data-stu-id="2c08f-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="2c08f-109">Veillez à mettre en cache ce nom de fichier s’il est nécessaire à des fins de référence ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2c08f-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c08f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2c08f-110">Return value</span></span>

<span data-ttu-id="2c08f-111">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2c08f-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2c08f-112">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="2c08f-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="2c08f-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2c08f-113">Return code</span></span>                                                                                           | <span data-ttu-id="2c08f-114">Description</span><span class="sxs-lookup"><span data-stu-id="2c08f-114">Description</span></span>                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c08f-115"><dt>**\_capture NMERR \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="2c08f-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="2c08f-116">La capture est suspendue et doit être arrêtée avant de pouvoir être redémarrée.</span><span class="sxs-lookup"><span data-stu-id="2c08f-116">The capture is paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="2c08f-117">Appelez [IESP :: Stop](iesp-stop.md) pour arrêter la capture.</span><span class="sxs-lookup"><span data-stu-id="2c08f-117">Call [IESP::Stop](iesp-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="2c08f-118"><dt>**\_capture NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="2c08f-118"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="2c08f-119">La capture a déjà démarré.</span><span class="sxs-lookup"><span data-stu-id="2c08f-119">The capture is already started.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="2c08f-120"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="2c08f-120"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="2c08f-121">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="2c08f-121">The NPP is not connected to the network.</span></span> <span data-ttu-id="2c08f-122">Appelez [IESP :: Connect](iesp-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="2c08f-122">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/>          |
| <dl> <span data-ttu-id="2c08f-123"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="2c08f-123"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="2c08f-124">Le NPP est connecté au réseau, mais pas avec la méthode [IESP :: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="2c08f-124">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="2c08f-125">Notes </span><span class="sxs-lookup"><span data-stu-id="2c08f-125">Remarks</span></span>

<span data-ttu-id="2c08f-126">L’emplacement du [*fichier de capture*](c.md) est spécifié dans le Registre Windows, mais vous pouvez utiliser Moniteur réseau pour modifier l’emplacement du répertoire.</span><span class="sxs-lookup"><span data-stu-id="2c08f-126">The location of the [*capture file*](c.md) is specified in the Windows registry, but you can use Network Monitor to change the directory location.</span></span>

<span data-ttu-id="2c08f-127">Lorsque vous redémarrez la capture à l’aide des méthodes IESP :: Start et [IESP :: Stop](iesp-stop.md) , vous devez appeler la méthode [IESP :: configure](iesp-configure.md) pour reconfigurer la connexion chaque fois que vous appelez IESP :: Start pour redémarrer la capture des données.</span><span class="sxs-lookup"><span data-stu-id="2c08f-127">When you restart the capture by using the IESP::Start and [IESP::Stop](iesp-stop.md) methods, you must call the [IESP::Configure](iesp-configure.md) method to reconfigure the connection each time you call IESP::Start to restart capturing data.</span></span> <span data-ttu-id="2c08f-128">Lorsque vous démarrez et arrêtez la capture à l’aide de ces trois méthodes, un nouveau fichier de capture est créé chaque fois que la capture est démarrée.</span><span class="sxs-lookup"><span data-stu-id="2c08f-128">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="2c08f-129">Vous pouvez également démarrer et arrêter la capture à l’aide des méthodes [IESP ::P ause](iesp-pause.md) et [IESP :: Resume](iesp-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="2c08f-129">You can also start and stop the capture by using the [IESP::Pause](iesp-pause.md) and [IESP::Resume](iesp-resume.md) methods.</span></span> <span data-ttu-id="2c08f-130">Lorsque ces deux méthodes sont utilisées, les données capturées sont stockées dans le même fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="2c08f-130">When these two methods are used, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c08f-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c08f-131">Requirements</span></span>



| <span data-ttu-id="2c08f-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c08f-132">Requirement</span></span> | <span data-ttu-id="2c08f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c08f-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c08f-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c08f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2c08f-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c08f-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2c08f-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c08f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2c08f-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c08f-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2c08f-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c08f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c08f-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c08f-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2c08f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2c08f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c08f-141"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c08f-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c08f-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c08f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c08f-143">IESP</span><span class="sxs-lookup"><span data-stu-id="2c08f-143">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="2c08f-144">IESP :: configure</span><span class="sxs-lookup"><span data-stu-id="2c08f-144">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="2c08f-145">IESP :: Connect</span><span class="sxs-lookup"><span data-stu-id="2c08f-145">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="2c08f-146">IESP ::P ause</span><span class="sxs-lookup"><span data-stu-id="2c08f-146">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="2c08f-147">IESP :: Resume</span><span class="sxs-lookup"><span data-stu-id="2c08f-147">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="2c08f-148">IESP :: Stop</span><span class="sxs-lookup"><span data-stu-id="2c08f-148">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




