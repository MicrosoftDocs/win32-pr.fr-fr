---
description: La méthode SetPortInfo définit la valeur de port 16 bits pour le premier port et le nombre de ports nécessaires pour une session.
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: 'ITMedia :: SetPortInfo, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c605c1768316871f6c3c9ec10f991f21c1643794
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527336"
---
# <a name="itmediasetportinfo-method"></a><span data-ttu-id="dd64a-103">ITMedia :: SetPortInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="dd64a-103">ITMedia::SetPortInfo method</span></span>

<span data-ttu-id="dd64a-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dd64a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dd64a-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="dd64a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dd64a-106">La méthode **SetPortInfo** définit la valeur de port 16 bits pour le premier port et le nombre de ports nécessaires pour une session.</span><span class="sxs-lookup"><span data-stu-id="dd64a-106">The **SetPortInfo** method sets the 16-bit port value for the first port and the number of ports needed for a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd64a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd64a-107">Syntax</span></span>


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="dd64a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd64a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd64a-109">*StartPort* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd64a-109">*StartPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd64a-110">Port de démarrage.</span><span class="sxs-lookup"><span data-stu-id="dd64a-110">Starting port.</span></span> <span data-ttu-id="dd64a-111">Il peut s’agir d’une valeur comprise dans la plage 0-65535.</span><span class="sxs-lookup"><span data-stu-id="dd64a-111">This can be a value in the range 0-65535.</span></span>

</dd> <dt>

<span data-ttu-id="dd64a-112">*NumPorts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd64a-112">*NumPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd64a-113">Nombre de ports.</span><span class="sxs-lookup"><span data-stu-id="dd64a-113">Number of ports.</span></span> <span data-ttu-id="dd64a-114">Il peut s’agir d’une valeur comprise dans la plage 0-65535.</span><span class="sxs-lookup"><span data-stu-id="dd64a-114">This can be a value in the range 0-65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd64a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd64a-115">Return value</span></span>

<span data-ttu-id="dd64a-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="dd64a-116">This method can return one of these values.</span></span>



| <span data-ttu-id="dd64a-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dd64a-117">Return code</span></span>                                                                                   | <span data-ttu-id="dd64a-118">Description</span><span class="sxs-lookup"><span data-stu-id="dd64a-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="dd64a-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd64a-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dd64a-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="dd64a-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="dd64a-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dd64a-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dd64a-122">Le paramètre *StartPort ou NumPorts* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="dd64a-122">The *StartPort or NumPorts* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="dd64a-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="dd64a-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dd64a-124">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="dd64a-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="dd64a-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="dd64a-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="dd64a-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dd64a-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="dd64a-127"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="dd64a-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="dd64a-128">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="dd64a-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="dd64a-129">Notes</span><span class="sxs-lookup"><span data-stu-id="dd64a-129">Remarks</span></span>

<span data-ttu-id="dd64a-130">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="dd64a-130">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="dd64a-131">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="dd64a-131">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd64a-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd64a-132">Requirements</span></span>



| <span data-ttu-id="dd64a-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd64a-133">Requirement</span></span> | <span data-ttu-id="dd64a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd64a-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd64a-135">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="dd64a-135">TAPI version</span></span><br/> | <span data-ttu-id="dd64a-136">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="dd64a-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="dd64a-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd64a-137">Header</span></span><br/>       | <dl> <span data-ttu-id="dd64a-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd64a-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd64a-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd64a-139">Library</span></span><br/>      | <dl> <span data-ttu-id="dd64a-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd64a-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dd64a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dd64a-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="dd64a-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd64a-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd64a-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd64a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd64a-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="dd64a-144">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




