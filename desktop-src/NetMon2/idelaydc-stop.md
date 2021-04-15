---
description: La méthode Stop arrête la capture en cours.
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
ms.openlocfilehash: 42c9cc1c4b6da7b5f934dd96f26aa9348c43ac0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484305"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="08136-103">IDelaydC :: Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="08136-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="08136-104">La méthode **Stop** arrête la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="08136-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="08136-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08136-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="08136-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08136-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08136-107">*lpStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="08136-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08136-108">Pointeur vers une structure de [statistiques](statistics.md) qui contient des statistiques réseau, telles que les trames totales et le nombre total d’octets capturés.</span><span class="sxs-lookup"><span data-stu-id="08136-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08136-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08136-109">Return value</span></span>

<span data-ttu-id="08136-110">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="08136-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="08136-111">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="08136-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="08136-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="08136-112">Return code</span></span>                                                                                          | <span data-ttu-id="08136-113">Description</span><span class="sxs-lookup"><span data-stu-id="08136-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08136-114"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="08136-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="08136-115">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="08136-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="08136-116">Appelez [IDelaydC :: Connect](idelaydc-connect.md) pour connecter le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="08136-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="08136-117"><dt>**NMERR \_ pas de \_ capture**</dt></span><span class="sxs-lookup"><span data-stu-id="08136-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="08136-118">Le NPP ne capture pas de données.</span><span class="sxs-lookup"><span data-stu-id="08136-118">The NPP is not capturing data.</span></span> <span data-ttu-id="08136-119">Appelez [IDelaydC :: Start](idelaydc-start.md) pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="08136-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="08136-120"><dt>**NMERR \_ non \_ retardé**</dt></span><span class="sxs-lookup"><span data-stu-id="08136-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="08136-121">Le NPP est connecté au réseau, mais pas avec la méthode [IDelaydC :: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="08136-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="08136-122">Notes</span><span class="sxs-lookup"><span data-stu-id="08136-122">Remarks</span></span>

<span data-ttu-id="08136-123">Quand **IDelaydC :: Stop** est appelé, moniteur réseau arrête la capture des données et ferme le [*fichier de capture*](c.md).</span><span class="sxs-lookup"><span data-stu-id="08136-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="08136-124">(Le nom du fichier de capture a été retourné lors de l’appel de [IDelaydC :: Start](idelaydc-start.md) ).</span><span class="sxs-lookup"><span data-stu-id="08136-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="08136-125">Vous pouvez maintenant examiner le contenu du fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="08136-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="08136-126">Lorsque vous arrêtez et démarrez la capture, veillez à appeler la méthode [IDelaydC :: configure](idelaydc-configure.md) chaque fois que vous appelez [IDelaydC :: Start](idelaydc-start.md) pour redémarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="08136-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="08136-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08136-127">Requirements</span></span>



| <span data-ttu-id="08136-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08136-128">Requirement</span></span> | <span data-ttu-id="08136-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="08136-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08136-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08136-130">Minimum supported client</span></span><br/> | <span data-ttu-id="08136-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08136-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="08136-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08136-132">Minimum supported server</span></span><br/> | <span data-ttu-id="08136-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08136-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="08136-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="08136-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="08136-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="08136-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="08136-136">DLL</span><span class="sxs-lookup"><span data-stu-id="08136-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08136-137"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08136-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08136-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08136-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08136-139">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="08136-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="08136-140">IDelaydC :: Connect</span><span class="sxs-lookup"><span data-stu-id="08136-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="08136-141">IDelaydC :: configure</span><span class="sxs-lookup"><span data-stu-id="08136-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="08136-142">IDelaydC :: Start</span><span class="sxs-lookup"><span data-stu-id="08136-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="08136-143">PORTENT</span><span class="sxs-lookup"><span data-stu-id="08136-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




