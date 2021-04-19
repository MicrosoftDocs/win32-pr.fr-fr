---
description: Le \_ message AGENTSPECIFIC de ligne TAPI est envoyé lorsque l’état d’un agent ACD change sur une ligne ouverte par l’application. L’application peut appeler lineGetAgentStatus pour déterminer l’état actuel de l’agent.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: Message LINE_AGENTSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544107"
---
# <a name="line_agentspecific-message"></a><span data-ttu-id="bfabf-104">\_Message AGENTSPECIFIC de ligne</span><span class="sxs-lookup"><span data-stu-id="bfabf-104">LINE\_AGENTSPECIFIC message</span></span>

<span data-ttu-id="bfabf-105">Le message **\_ AGENTSPECIFIC de ligne** TAPI est envoyé lorsque l’état d’un agent ACD change sur une ligne ouverte par l’application.</span><span class="sxs-lookup"><span data-stu-id="bfabf-105">The TAPI **LINE\_AGENTSPECIFIC** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="bfabf-106">L’application peut appeler [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) pour déterminer l’état actuel de l’agent.</span><span class="sxs-lookup"><span data-stu-id="bfabf-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="bfabf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfabf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfabf-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="bfabf-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="bfabf-109">Handle de l’application sur le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="bfabf-109">The application's handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="bfabf-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="bfabf-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="bfabf-111">Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.</span><span class="sxs-lookup"><span data-stu-id="bfabf-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="bfabf-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="bfabf-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="bfabf-113">Index dans le tableau d’identificateurs d’extension de gestionnaire dans la structure [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) de l’extension de gestionnaire à laquelle le message est associé.</span><span class="sxs-lookup"><span data-stu-id="bfabf-113">The index into the array of handler extension identifiers in the [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) structure of the handler extension with which the message is associated.</span></span>

</dd> <dt>

<span data-ttu-id="bfabf-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="bfabf-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="bfabf-115">Spécifique à l’extension du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="bfabf-115">Specific to the handler extension.</span></span> <span data-ttu-id="bfabf-116">En règle générale, cette valeur est utilisée pour forcer l’application à appeler une fonction [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) pour extraire plus de détails sur le message.</span><span class="sxs-lookup"><span data-stu-id="bfabf-116">Generally, this value is used to cause the application to invoke a [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) function to fetch further details about the message.</span></span>

</dd> <dt>

<span data-ttu-id="bfabf-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="bfabf-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="bfabf-118">Spécifique à l’extension du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="bfabf-118">Specific to the handler extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfabf-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfabf-119">Return value</span></span>

<span data-ttu-id="bfabf-120">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="bfabf-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfabf-121">Notes</span><span class="sxs-lookup"><span data-stu-id="bfabf-121">Remarks</span></span>

<span data-ttu-id="bfabf-122">Le message de **ligne \_ AGENTSPECIFIC** n’est pas envoyé aux applications qui prennent en charge des versions antérieures de TAPI.</span><span class="sxs-lookup"><span data-stu-id="bfabf-122">The **LINE\_AGENTSPECIFIC** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfabf-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfabf-123">Requirements</span></span>



| <span data-ttu-id="bfabf-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfabf-124">Requirement</span></span> | <span data-ttu-id="bfabf-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfabf-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bfabf-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="bfabf-126">TAPI version</span></span><br/> | <span data-ttu-id="bfabf-127">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bfabf-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="bfabf-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfabf-128">Header</span></span><br/>       | <dl> <span data-ttu-id="bfabf-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfabf-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfabf-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfabf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfabf-131">**LINEAGENTCAPS**</span><span class="sxs-lookup"><span data-stu-id="bfabf-131">**LINEAGENTCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[<span data-ttu-id="bfabf-132">**lineAgentSpecific**</span><span class="sxs-lookup"><span data-stu-id="bfabf-132">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[<span data-ttu-id="bfabf-133">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="bfabf-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




