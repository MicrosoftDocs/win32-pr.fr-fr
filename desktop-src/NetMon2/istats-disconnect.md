---
description: Déconnecte le NPP du réseau.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: IStats ::D méthode éconnecter (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a5fa56c05036380b5dba42089979b43d776a4b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520659"
---
# <a name="istatsdisconnect-method"></a><span data-ttu-id="be47b-103">IStats ::D méthode éconnecter</span><span class="sxs-lookup"><span data-stu-id="be47b-103">IStats::Disconnect method</span></span>

<span data-ttu-id="be47b-104">La **méthode Disconnect** déconnecte le NPP du réseau.</span><span class="sxs-lookup"><span data-stu-id="be47b-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="be47b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be47b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="be47b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be47b-106">Parameters</span></span>

<span data-ttu-id="be47b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="be47b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be47b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be47b-108">Return value</span></span>

<span data-ttu-id="be47b-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="be47b-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="be47b-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="be47b-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="be47b-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="be47b-111">Return code</span></span>                                                                                            | <span data-ttu-id="be47b-112">Description</span><span class="sxs-lookup"><span data-stu-id="be47b-112">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="be47b-113"><dt>**\_capture NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="be47b-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="be47b-114">Le NPP capture actuellement des données.</span><span class="sxs-lookup"><span data-stu-id="be47b-114">The NPP is currently capturing data.</span></span> <span data-ttu-id="be47b-115">Vous ne pouvez pas vous déconnecter du réseau pendant qu’une capture de données est en cours.</span><span class="sxs-lookup"><span data-stu-id="be47b-115">You cannot disconnect from the network while a data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="be47b-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="be47b-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="be47b-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="be47b-117">The NPP is not connected to the network.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="be47b-118"><dt>**NMERR \_ non \_ stats \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="be47b-118"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="be47b-119">Le NPP est connecté au réseau, mais pas avec la méthode [**IStats :: Connect**](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="be47b-119">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="be47b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="be47b-120">Remarks</span></span>

<span data-ttu-id="be47b-121">Cette méthode ne peut pas être appelée lorsque le NPP capture des données.</span><span class="sxs-lookup"><span data-stu-id="be47b-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="be47b-122">Appelez d’abord la méthode **IStats ::D éconnecter** , puis appelez [**IStats :: Stop**](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="be47b-122">Call the **IStats::Disconnect** method first and then call [**IStats::Stop**](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be47b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be47b-123">Requirements</span></span>



| <span data-ttu-id="be47b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be47b-124">Requirement</span></span> | <span data-ttu-id="be47b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="be47b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be47b-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be47b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="be47b-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be47b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="be47b-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be47b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="be47b-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be47b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="be47b-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="be47b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="be47b-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="be47b-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="be47b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="be47b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be47b-133"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be47b-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be47b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be47b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be47b-135">**IStats**</span><span class="sxs-lookup"><span data-stu-id="be47b-135">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="be47b-136">**IStats :: Connect**</span><span class="sxs-lookup"><span data-stu-id="be47b-136">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="be47b-137">**IStats :: Stop**</span><span class="sxs-lookup"><span data-stu-id="be47b-137">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 




