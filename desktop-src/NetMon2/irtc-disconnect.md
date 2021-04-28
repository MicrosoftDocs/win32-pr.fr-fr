---
description: IRTC ::D méthode éconnecter-la méthode Disconnect déconnecte le NPP du réseau.
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: IRTC ::D méthode éconnecter (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 43acb88e2c7b6108a162c4715de02375121021f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110717"
---
# <a name="irtcdisconnect-method"></a><span data-ttu-id="d7a84-103">IRTC ::D méthode éconnecter</span><span class="sxs-lookup"><span data-stu-id="d7a84-103">IRTC::Disconnect method</span></span>

<span data-ttu-id="d7a84-104">La **méthode Disconnect** déconnecte le NPP du réseau.</span><span class="sxs-lookup"><span data-stu-id="d7a84-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7a84-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7a84-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="d7a84-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7a84-106">Parameters</span></span>

<span data-ttu-id="d7a84-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d7a84-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7a84-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7a84-108">Return value</span></span>

<span data-ttu-id="d7a84-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d7a84-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d7a84-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="d7a84-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="d7a84-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d7a84-111">Return code</span></span>                                                                                          | <span data-ttu-id="d7a84-112">Description</span><span class="sxs-lookup"><span data-stu-id="d7a84-112">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7a84-113"><dt>**\_capture NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="d7a84-114">Le NPP capture des données.</span><span class="sxs-lookup"><span data-stu-id="d7a84-114">The NPP is capturing data.</span></span> <span data-ttu-id="d7a84-115">Vous ne pouvez pas vous déconnecter du réseau pendant que la capture de données est en cours.</span><span class="sxs-lookup"><span data-stu-id="d7a84-115">You cannot disconnect from the network while the data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="d7a84-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d7a84-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="d7a84-117">The NPP is not connected to the network.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="d7a84-118"><dt>**NMERR \_ pas de \_ temps réel**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-118"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="d7a84-119">Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="d7a84-119">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="d7a84-120">Notes </span><span class="sxs-lookup"><span data-stu-id="d7a84-120">Remarks</span></span>

<span data-ttu-id="d7a84-121">Cette méthode ne peut pas être appelée lorsque le NPP capture des données.</span><span class="sxs-lookup"><span data-stu-id="d7a84-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="d7a84-122">Vous devez appeler la méthode [IRTC :: Stop](irtc-stop.md) avant d’appeler IRTC ::D éconnecter.</span><span class="sxs-lookup"><span data-stu-id="d7a84-122">You must call the [IRTC::Stop](irtc-stop.md) method before calling IRTC::Disconnect.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a84-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7a84-123">Requirements</span></span>



| <span data-ttu-id="d7a84-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7a84-124">Requirement</span></span> | <span data-ttu-id="d7a84-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7a84-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a84-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7a84-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a84-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7a84-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d7a84-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7a84-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a84-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7a84-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d7a84-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7a84-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a84-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d7a84-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d7a84-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7a84-133"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7a84-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7a84-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a84-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="d7a84-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="d7a84-136">IRTC :: Connect</span><span class="sxs-lookup"><span data-stu-id="d7a84-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="d7a84-137">IRTC :: Stop</span><span class="sxs-lookup"><span data-stu-id="d7a84-137">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




