---
description: La méthode Disconnect déconnecte le NPP du réseau.
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: IDelaydC ::D méthode éconnecter (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d192aa80f543706eea4bc197bc3dc8d57dd64aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112219"
---
# <a name="idelaydcdisconnect-method"></a><span data-ttu-id="75178-103">IDelaydC ::D méthode éconnecter</span><span class="sxs-lookup"><span data-stu-id="75178-103">IDelaydC::Disconnect method</span></span>

<span data-ttu-id="75178-104">La **méthode Disconnect** déconnecte le NPP du réseau.</span><span class="sxs-lookup"><span data-stu-id="75178-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="75178-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75178-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="75178-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75178-106">Parameters</span></span>

<span data-ttu-id="75178-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="75178-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75178-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75178-108">Return value</span></span>

<span data-ttu-id="75178-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="75178-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="75178-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="75178-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="75178-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="75178-111">Return code</span></span>                                                                                          | <span data-ttu-id="75178-112">Description</span><span class="sxs-lookup"><span data-stu-id="75178-112">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="75178-113"><dt>**\_capture NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="75178-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="75178-114">Le NPP capture des données.</span><span class="sxs-lookup"><span data-stu-id="75178-114">The NPP is capturing data.</span></span> <span data-ttu-id="75178-115">Vous ne pouvez pas déconnecter le NPP du réseau lors d’une capture.</span><span class="sxs-lookup"><span data-stu-id="75178-115">You cannot disconnect the NPP from the network during a capture.</span></span><br/>            |
| <dl> <span data-ttu-id="75178-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="75178-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="75178-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="75178-117">The NPP is not connected to the network.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="75178-118"><dt>**NMERR \_ non \_ retardé**</dt></span><span class="sxs-lookup"><span data-stu-id="75178-118"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="75178-119">Le NPP est connecté au réseau, mais pas avec la méthode [IDelaydC :: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="75178-119">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="75178-120">Notes</span><span class="sxs-lookup"><span data-stu-id="75178-120">Remarks</span></span>

<span data-ttu-id="75178-121">Cette méthode ne peut pas être appelée lorsque le NPP capture des données.</span><span class="sxs-lookup"><span data-stu-id="75178-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="75178-122">Vous devez appeler la méthode **IDelaydC :: Stop** avant d’appeler **Disconnect**.</span><span class="sxs-lookup"><span data-stu-id="75178-122">You must call the **IDelaydC::Stop** method before calling **Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="75178-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75178-123">Requirements</span></span>



| <span data-ttu-id="75178-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75178-124">Requirement</span></span> | <span data-ttu-id="75178-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="75178-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75178-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75178-126">Minimum supported client</span></span><br/> | <span data-ttu-id="75178-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75178-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="75178-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75178-128">Minimum supported server</span></span><br/> | <span data-ttu-id="75178-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75178-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="75178-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="75178-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="75178-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="75178-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="75178-132">DLL</span><span class="sxs-lookup"><span data-stu-id="75178-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75178-133"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75178-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75178-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75178-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75178-135">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="75178-135">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="75178-136">IDelaydC :: Connect</span><span class="sxs-lookup"><span data-stu-id="75178-136">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="75178-137">IDelaydC :: Stop</span><span class="sxs-lookup"><span data-stu-id="75178-137">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




