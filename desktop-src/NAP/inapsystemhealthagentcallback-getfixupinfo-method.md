---
title: Méthode INapSystemHealthAgentCallback GetFixupInfo (NapSystemHealthAgent. h)
description: Est appelé par NapAgent pour déterminer l’état de l’agent d’intégrité système pendant le traitement d’un SoHResponse.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- Méthode GetFixupInfo NAP
- Méthode GetFixupInfo NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode GetFixupInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104140"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a><span data-ttu-id="37d6d-106">INapSystemHealthAgentCallback :: GetFixupInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="37d6d-106">INapSystemHealthAgentCallback::GetFixupInfo method</span></span>

> [!Note]  
> <span data-ttu-id="37d6d-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="37d6d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="37d6d-108">La méthode **INapSystemHealthAgentCallback :: GetFixupInfo** est appelée par le NapAgent pour déterminer l’état de l’agent d’intégrité système, pendant le traitement d’un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="37d6d-108">The **INapSystemHealthAgentCallback::GetFixupInfo** method is called by the NapAgent to determine the state of the system health agent, while it is processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="37d6d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37d6d-109">Syntax</span></span>


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="37d6d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37d6d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37d6d-111">*informations* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="37d6d-111">*info* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37d6d-112">Pointeur vers un pointeur vers une structure [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) qui contient l’état de correction de l’agent.</span><span class="sxs-lookup"><span data-stu-id="37d6d-112">A pointer to a pointer to a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure that contains the fix-up status of the agent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37d6d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37d6d-113">Return value</span></span>

<span data-ttu-id="37d6d-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="37d6d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="37d6d-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="37d6d-115">Return code</span></span>                                                                          | <span data-ttu-id="37d6d-116">Description</span><span class="sxs-lookup"><span data-stu-id="37d6d-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="37d6d-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="37d6d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="37d6d-118">Indique la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="37d6d-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="37d6d-119">Notes</span><span class="sxs-lookup"><span data-stu-id="37d6d-119">Remarks</span></span>

<span data-ttu-id="37d6d-120">Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.</span><span class="sxs-lookup"><span data-stu-id="37d6d-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="37d6d-121">L’agent d’intégrité système doit retourner **S \_ OK** immédiatement sans blocage.</span><span class="sxs-lookup"><span data-stu-id="37d6d-121">The system health agent must return **S\_OK** immediately without blocking.</span></span>

## <a name="requirements"></a><span data-ttu-id="37d6d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37d6d-122">Requirements</span></span>



| <span data-ttu-id="37d6d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37d6d-123">Requirement</span></span> | <span data-ttu-id="37d6d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d6d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37d6d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37d6d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="37d6d-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37d6d-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="37d6d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37d6d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="37d6d-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37d6d-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="37d6d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="37d6d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="37d6d-130"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="37d6d-130"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="37d6d-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="37d6d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="37d6d-132"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="37d6d-132"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37d6d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37d6d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d6d-134">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="37d6d-134">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





