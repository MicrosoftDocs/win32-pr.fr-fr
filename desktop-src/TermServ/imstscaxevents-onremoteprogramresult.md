---
title: Méthode IMsTscAxEvents OnRemoteProgramResult
description: Appelée lorsqu’un programme RemoteApp retourne un résultat au contrôle client.
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRemoteProgramResult
- Méthode OnRemoteProgramResult Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRemoteProgramResult
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramResult
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880e4fb3f6453114415f5bcc07a0afb9c176a1bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104314"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a><span data-ttu-id="59f90-106">IMsTscAxEvents :: OnRemoteProgramResult, méthode</span><span class="sxs-lookup"><span data-stu-id="59f90-106">IMsTscAxEvents::OnRemoteProgramResult method</span></span>

<span data-ttu-id="59f90-107">Appelée lorsqu’un programme RemoteApp retourne un résultat au contrôle client.</span><span class="sxs-lookup"><span data-stu-id="59f90-107">Called when a RemoteApp program returns a result to the client control.</span></span>

## <a name="syntax"></a><span data-ttu-id="59f90-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59f90-108">Syntax</span></span>


```C++
VOID OnRemoteProgramResult(
  [in] BSTR                bstrRemoteProgram,
  [in] RemoteProgramResult lError,
  [in] VARIANT_BOOL        vbIsExecutable
);
```



## <a name="parameters"></a><span data-ttu-id="59f90-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59f90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59f90-110">*bstrRemoteProgram* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59f90-110">*bstrRemoteProgram* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59f90-111">Nom du programme RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="59f90-111">The name of the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="59f90-112">*lError* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59f90-112">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59f90-113">Résultat de la tentative de lancement du programme RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="59f90-113">The result of the attempt to launch the RemoteApp program.</span></span>

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span data-ttu-id="59f90-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="59f90-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="59f90-115">Le programme RemoteApp s’est correctement lancé.</span><span class="sxs-lookup"><span data-stu-id="59f90-115">The RemoteApp program launched successfully.</span></span>

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span data-ttu-id="59f90-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="59f90-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="59f90-117">La session à distance est verrouillée et le programme RemoteApp ne peut pas être lancé.</span><span class="sxs-lookup"><span data-stu-id="59f90-117">The remote session is locked and the RemoteApp program cannot be launched.</span></span> <span data-ttu-id="59f90-118">L’utilisateur doit entrer ses informations d’identification pour déverrouiller la session, puis lancer le programme RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="59f90-118">The user must enter their credentials to unlock the session, and then launch the RemoteApp program.</span></span>

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span data-ttu-id="59f90-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="59f90-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="59f90-120">Le programme RemoteApp a renvoyé une erreur de protocole.</span><span class="sxs-lookup"><span data-stu-id="59f90-120">The RemoteApp program returned a protocol error.</span></span>

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span data-ttu-id="59f90-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="59f90-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="59f90-122">Le programme RemoteApp n’est pas dans la liste approuvée du serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="59f90-122">The RemoteApp program is not in the approved list of the RD Session Host server.</span></span>

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span data-ttu-id="59f90-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="59f90-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="59f90-124">Le chemin d’accès réseau au programme RemoteApp a été refusé.</span><span class="sxs-lookup"><span data-stu-id="59f90-124">The network path to the RemoteApp program was denied.</span></span>

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span data-ttu-id="59f90-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="59f90-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="59f90-126">Le fichier programme RemoteApp est introuvable.</span><span class="sxs-lookup"><span data-stu-id="59f90-126">The RemoteApp program file was not found.</span></span>

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span data-ttu-id="59f90-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="59f90-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="59f90-128">Échec du lancement du programme RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="59f90-128">The RemoteApp program failed to launch.</span></span>

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span data-ttu-id="59f90-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))</span><span class="sxs-lookup"><span data-stu-id="59f90-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))</span></span>


</dt> <dd>

<span data-ttu-id="59f90-130">Impossible de lancer le programme RemoteApp, car la session affiche actuellement le Bureau sécurisé.</span><span class="sxs-lookup"><span data-stu-id="59f90-130">The RemoteApp program cannot be launched because the session is currently displaying the secure desktop.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="59f90-131">*vbIsExecutable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59f90-131">*vbIsExecutable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59f90-132">Indique si le programme RemoteApp a été lancé directement, en utilisant le nom de l’exécutable ou indirectement, à l’aide d’une association de fichier.</span><span class="sxs-lookup"><span data-stu-id="59f90-132">Indicates whether the RemoteApp program was launched directly, by using the executable name or indirectly, by using a file association.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59f90-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59f90-133">Return value</span></span>

<span data-ttu-id="59f90-134">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="59f90-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59f90-135">Notes</span><span class="sxs-lookup"><span data-stu-id="59f90-135">Remarks</span></span>

<span data-ttu-id="59f90-136">Implémentez cette méthode dans votre récepteur d’événements pour recevoir une notification indiquant qu’un programme RemoteApp a retourné un résultat.</span><span class="sxs-lookup"><span data-stu-id="59f90-136">Implement this method in your event sink to receive notification that a RemoteApp program returned a result.</span></span>

<span data-ttu-id="59f90-137">Cette méthode est appelée immédiatement après que le contrôle ActiveX a tenté de lancer le programme RemoteApp et le paramètre *lError* indique le résultat de la tentative.</span><span class="sxs-lookup"><span data-stu-id="59f90-137">This method is called immediately after the ActiveX control attempts to launch the RemoteApp program, and the *lError* parameter indicates the result of the attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="59f90-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59f90-138">Requirements</span></span>



| <span data-ttu-id="59f90-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59f90-139">Requirement</span></span> | <span data-ttu-id="59f90-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="59f90-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59f90-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59f90-141">Minimum supported client</span></span><br/> | <span data-ttu-id="59f90-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="59f90-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="59f90-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59f90-143">Minimum supported server</span></span><br/> | <span data-ttu-id="59f90-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59f90-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="59f90-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="59f90-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="59f90-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59f90-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="59f90-147">DLL</span><span class="sxs-lookup"><span data-stu-id="59f90-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59f90-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59f90-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="59f90-149">IID</span><span class="sxs-lookup"><span data-stu-id="59f90-149">IID</span></span><br/>                      | <span data-ttu-id="59f90-150">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="59f90-150">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="59f90-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59f90-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59f90-152">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="59f90-152">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





