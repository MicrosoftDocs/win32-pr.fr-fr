---
title: Méthode IMsTscAxEvents OnFatalError
description: Appelé lorsque le contrôle client rencontre une erreur irrécupérable.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnFatalError
- Méthode OnFatalError Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnFatalError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73402ac178bcb2ac3dc03c0adda092d3b49f6ba3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843849"
---
# <a name="imstscaxeventsonfatalerror-method"></a><span data-ttu-id="af3ed-106">IMsTscAxEvents :: OnFatalError, méthode</span><span class="sxs-lookup"><span data-stu-id="af3ed-106">IMsTscAxEvents::OnFatalError method</span></span>

<span data-ttu-id="af3ed-107">Appelé lorsque le contrôle client rencontre une erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="af3ed-107">Called when the client control encounters a fatal error.</span></span>

## <a name="syntax"></a><span data-ttu-id="af3ed-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af3ed-108">Syntax</span></span>


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="af3ed-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af3ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af3ed-110">*ErrorCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af3ed-110">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af3ed-111">Indique le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="af3ed-111">Indicates the error code.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="af3ed-112"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="af3ed-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="af3ed-113">Une erreur inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="af3ed-113">An unknown error has occurred.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="af3ed-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="af3ed-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="af3ed-115">Code d’erreur interne 1.</span><span class="sxs-lookup"><span data-stu-id="af3ed-115">Internal error code 1.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="af3ed-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="af3ed-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="af3ed-117">Une erreur de mémoire insuffisante s’est produite.</span><span class="sxs-lookup"><span data-stu-id="af3ed-117">An out-of-memory error has occurred.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="af3ed-118"><span id="3"></span>**1,3**</span><span class="sxs-lookup"><span data-stu-id="af3ed-118"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="af3ed-119">Une erreur de création de fenêtre s’est produite.</span><span class="sxs-lookup"><span data-stu-id="af3ed-119">A window-creation error has occurred.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="af3ed-120"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="af3ed-120"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="af3ed-121">Code d’erreur interne 2.</span><span class="sxs-lookup"><span data-stu-id="af3ed-121">Internal error code 2.</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="af3ed-122"><span id="5"></span>**5,5**</span><span class="sxs-lookup"><span data-stu-id="af3ed-122"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="af3ed-123">Code d’erreur interne 3.</span><span class="sxs-lookup"><span data-stu-id="af3ed-123">Internal error code 3.</span></span> <span data-ttu-id="af3ed-124">Cet État n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="af3ed-124">This is not a valid state.</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="af3ed-125"><span id="6"></span>**6,3**</span><span class="sxs-lookup"><span data-stu-id="af3ed-125"><span id="6"></span>**6**</span></span>


</dt> <dd>

<span data-ttu-id="af3ed-126">Code d’erreur interne 4.</span><span class="sxs-lookup"><span data-stu-id="af3ed-126">Internal error code 4.</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="af3ed-127"><span id="7"></span>**Commission(7**</span><span class="sxs-lookup"><span data-stu-id="af3ed-127"><span id="7"></span>**7**</span></span>


</dt> <dd>

<span data-ttu-id="af3ed-128">Une erreur irrécupérable s’est produite lors de la connexion du client.</span><span class="sxs-lookup"><span data-stu-id="af3ed-128">An unrecoverable error has occurred during client connection.</span></span>

</dd> <dt>

<span id="100"></span>

<span data-ttu-id="af3ed-129"><span id="100"></span>**100**</span><span class="sxs-lookup"><span data-stu-id="af3ed-129"><span id="100"></span>**100**</span></span>


</dt> <dd>

<span data-ttu-id="af3ed-130">Erreur d’initialisation Winsock.</span><span class="sxs-lookup"><span data-stu-id="af3ed-130">Winsock initialization error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af3ed-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af3ed-131">Return value</span></span>

<span data-ttu-id="af3ed-132">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="af3ed-132">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af3ed-133">Notes</span><span class="sxs-lookup"><span data-stu-id="af3ed-133">Remarks</span></span>

<span data-ttu-id="af3ed-134">En réponse à cet événement, le conteneur affiche un message d’erreur et s’arrête.</span><span class="sxs-lookup"><span data-stu-id="af3ed-134">In response to this event, the container displays an error message and shuts down.</span></span>

<span data-ttu-id="af3ed-135">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="af3ed-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af3ed-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af3ed-136">Requirements</span></span>



| <span data-ttu-id="af3ed-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af3ed-137">Requirement</span></span> | <span data-ttu-id="af3ed-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="af3ed-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af3ed-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af3ed-139">Minimum supported client</span></span><br/> | <span data-ttu-id="af3ed-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af3ed-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="af3ed-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af3ed-141">Minimum supported server</span></span><br/> | <span data-ttu-id="af3ed-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af3ed-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="af3ed-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="af3ed-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="af3ed-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af3ed-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="af3ed-145">DLL</span><span class="sxs-lookup"><span data-stu-id="af3ed-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af3ed-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af3ed-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="af3ed-147">IID</span><span class="sxs-lookup"><span data-stu-id="af3ed-147">IID</span></span><br/>                      | <span data-ttu-id="af3ed-148">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="af3ed-148">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="af3ed-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af3ed-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af3ed-150">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="af3ed-150">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





