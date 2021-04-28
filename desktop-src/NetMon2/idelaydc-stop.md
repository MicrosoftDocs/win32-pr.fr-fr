---
description: 'IDelaydC :: Stop, méthode : la méthode Stop arrête la capture en cours.'
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'IDelaydC :: Stop, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 38be5b6ba4c3f6edcd716f4d0235150e96dd692a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110777"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="81e3c-103">IDelaydC :: Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="81e3c-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="81e3c-104">La méthode **Stop** arrête la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="81e3c-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e3c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81e3c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="81e3c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81e3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81e3c-107">*lpStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="81e3c-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81e3c-108">Pointeur vers une structure de [statistiques](statistics.md) qui contient des statistiques réseau, telles que les trames totales et le nombre total d’octets capturés.</span><span class="sxs-lookup"><span data-stu-id="81e3c-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81e3c-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="81e3c-109">Return value</span></span>

<span data-ttu-id="81e3c-110">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="81e3c-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="81e3c-111">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="81e3c-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="81e3c-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="81e3c-112">Return code</span></span>                                                                                          | <span data-ttu-id="81e3c-113">Description</span><span class="sxs-lookup"><span data-stu-id="81e3c-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81e3c-114"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="81e3c-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="81e3c-115">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="81e3c-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="81e3c-116">Appelez [IDelaydC :: Connect](idelaydc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="81e3c-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="81e3c-117"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="81e3c-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="81e3c-118">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="81e3c-118">The NPP is not capturing data.</span></span> <span data-ttu-id="81e3c-119">Appelez [IDelaydC :: Start](idelaydc-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="81e3c-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="81e3c-120"><dt>**NMERR \_ non \_ retardé**</dt></span><span class="sxs-lookup"><span data-stu-id="81e3c-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="81e3c-121">Le NPP est connecté au réseau, mais pas avec la méthode [IDelaydC :: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="81e3c-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="81e3c-122">Notes </span><span class="sxs-lookup"><span data-stu-id="81e3c-122">Remarks</span></span>

<span data-ttu-id="81e3c-123">Quand **IDelaydC :: Stop** est appelé, moniteur réseau arrête la capture des données et ferme le [*fichier de capture*](c.md).</span><span class="sxs-lookup"><span data-stu-id="81e3c-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="81e3c-124">(Le nom du fichier de capture a été retourné lors de l’appel de [IDelaydC :: Start](idelaydc-start.md) ).</span><span class="sxs-lookup"><span data-stu-id="81e3c-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="81e3c-125">Vous pouvez maintenant examiner le contenu du fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="81e3c-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="81e3c-126">Lorsque vous arrêtez et démarrez la capture, veillez à appeler la méthode [IDelaydC :: configure](idelaydc-configure.md) chaque fois que vous appelez [IDelaydC :: Start](idelaydc-start.md) pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="81e3c-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="81e3c-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81e3c-127">Requirements</span></span>



| <span data-ttu-id="81e3c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81e3c-128">Requirement</span></span> | <span data-ttu-id="81e3c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="81e3c-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e3c-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81e3c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="81e3c-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81e3c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="81e3c-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81e3c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="81e3c-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81e3c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="81e3c-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="81e3c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="81e3c-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="81e3c-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="81e3c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="81e3c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81e3c-137"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81e3c-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81e3c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81e3c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e3c-139">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="81e3c-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="81e3c-140">IDelaydC :: Connect</span><span class="sxs-lookup"><span data-stu-id="81e3c-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="81e3c-141">IDelaydC :: configure</span><span class="sxs-lookup"><span data-stu-id="81e3c-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="81e3c-142">IDelaydC :: Start</span><span class="sxs-lookup"><span data-stu-id="81e3c-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="81e3c-143">PORTENT</span><span class="sxs-lookup"><span data-stu-id="81e3c-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




