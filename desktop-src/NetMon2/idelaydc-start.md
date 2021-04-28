---
description: 'IDelaydC :: Start, méthode-la méthode start démarre une capture.'
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'IDelaydC :: Start, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 25bf778d9cccce20c736c5f8b83e6af9754ac933
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118437"
---
# <a name="idelaydcstart-method"></a><span data-ttu-id="0cfac-103">IDelaydC :: Start, méthode</span><span class="sxs-lookup"><span data-stu-id="0cfac-103">IDelaydC::Start method</span></span>

<span data-ttu-id="0cfac-104">La méthode **Start** démarre une capture.</span><span class="sxs-lookup"><span data-stu-id="0cfac-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cfac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cfac-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="0cfac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cfac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cfac-107">*pFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0cfac-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfac-108">Pointeur vers le nom du [*fichier de capture*](c.md) utilisé pour stocker les données réseau.</span><span class="sxs-lookup"><span data-stu-id="0cfac-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="0cfac-109">Veillez à mettre en cache ce nom de fichier s’il est nécessaire à des fins de référence ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0cfac-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cfac-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0cfac-110">Return value</span></span>

<span data-ttu-id="0cfac-111">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0cfac-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0cfac-112">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="0cfac-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0cfac-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0cfac-113">Return code</span></span>                                                                                           | <span data-ttu-id="0cfac-114">Description</span><span class="sxs-lookup"><span data-stu-id="0cfac-114">Description</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0cfac-115"><dt>**\_capture NMERR \_ suspendue**</dt></span><span class="sxs-lookup"><span data-stu-id="0cfac-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="0cfac-116">La capture est dans un état suspendu et doit être arrêtée avant de pouvoir être redémarrée.</span><span class="sxs-lookup"><span data-stu-id="0cfac-116">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="0cfac-117">Appelez [**IDelaydC :: Stop**](idelaydc-stop.md) pour arrêter la capture.</span><span class="sxs-lookup"><span data-stu-id="0cfac-117">Call [**IDelaydC::Stop**](idelaydc-stop.md) to stop the capture.</span></span> <span data-ttu-id="0cfac-118">Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="0cfac-118">For more information, see the Remarks section in this topic.</span></span><br/> |
| <dl> <span data-ttu-id="0cfac-119"><dt>**\_capture NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="0cfac-119"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="0cfac-120">La capture a déjà démarré.</span><span class="sxs-lookup"><span data-stu-id="0cfac-120">The capture is already started.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="0cfac-121"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="0cfac-121"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="0cfac-122">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="0cfac-122">The NPP is not connected to the network.</span></span> <span data-ttu-id="0cfac-123">Appelez [**IDelaydC :: Connect**](idelaydc-connect.md) pour vous connecter au réseau.</span><span class="sxs-lookup"><span data-stu-id="0cfac-123">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="0cfac-124"><dt>**NMERR \_ non \_ retardé**</dt></span><span class="sxs-lookup"><span data-stu-id="0cfac-124"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="0cfac-125">Le NPP est connecté au réseau, mais pas avec la méthode [**IDelaydC :: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0cfac-125">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="0cfac-126">Notes </span><span class="sxs-lookup"><span data-stu-id="0cfac-126">Remarks</span></span>

<span data-ttu-id="0cfac-127">L’emplacement du [*fichier de capture*](c.md) est spécifié dans le Registre Windows, mais vous pouvez utiliser Moniteur réseau pour modifier l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="0cfac-127">The location of the [*capture file*](c.md) is specified in your Windows registry, but you can use Network Monitor to change the file's location.</span></span>

<span data-ttu-id="0cfac-128">Pour redémarrer la capture à l’aide de **IDelaydC :: Start** et [**IDelaydC :: Stop**](idelaydc-stop.md), vous devez appeler la méthode [**IDelaydC :: configure**](idelaydc-configure.md) pour reconfigurer la connexion chaque fois que vous appelez la méthode **IDelaydC :: Start** pour redémarrer la capture des données.</span><span class="sxs-lookup"><span data-stu-id="0cfac-128">To restart the capture by using **IDelaydC::Start** and [**IDelaydC::Stop**](idelaydc-stop.md), you must call the [**IDelaydC::Configure**](idelaydc-configure.md) method to reconfigure the connection each time you call the **IDelaydC::Start** method to restart capturing data.</span></span> <span data-ttu-id="0cfac-129">Lorsque vous démarrez et arrêtez la capture à l’aide de ces trois méthodes, un nouveau fichier de capture est créé chaque fois que la capture est démarrée.</span><span class="sxs-lookup"><span data-stu-id="0cfac-129">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="0cfac-130">Vous pouvez également démarrer et arrêter la capture à l’aide des méthodes [**IDelaydC ::P ause**](idelaydc-pause.md) et [**IDelaydC :: Resume**](idelaydc-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="0cfac-130">You can also start and stop the capture by using the [**IDelaydC::Pause**](idelaydc-pause.md) and [**IDelaydC::Resume**](idelaydc-resume.md) methods.</span></span> <span data-ttu-id="0cfac-131">Lorsque vous utilisez ces deux méthodes, les données capturées sont stockées dans le même fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="0cfac-131">When you use these two methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0cfac-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cfac-132">Requirements</span></span>



| <span data-ttu-id="0cfac-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cfac-133">Requirement</span></span> | <span data-ttu-id="0cfac-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cfac-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfac-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cfac-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0cfac-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cfac-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0cfac-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cfac-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0cfac-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cfac-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0cfac-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cfac-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cfac-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cfac-140"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0cfac-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0cfac-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cfac-142"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cfac-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cfac-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cfac-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cfac-144">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="0cfac-144">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="0cfac-145">**IDelaydC :: configure**</span><span class="sxs-lookup"><span data-stu-id="0cfac-145">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="0cfac-146">**IDelaydC :: Connect**</span><span class="sxs-lookup"><span data-stu-id="0cfac-146">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="0cfac-147">**IDelaydC ::P ause**</span><span class="sxs-lookup"><span data-stu-id="0cfac-147">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="0cfac-148">**IDelaydC :: Resume**</span><span class="sxs-lookup"><span data-stu-id="0cfac-148">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="0cfac-149">**IDelaydC :: Stop**</span><span class="sxs-lookup"><span data-stu-id="0cfac-149">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




