---
description: Le \_ message de ligne AGENTSTATUSEX est envoyé lorsque l’état d’un agent ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction lineProxyMessage.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: Message LINE_AGENTSTATUSEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541424"
---
# <a name="line_agentstatusex-message"></a><span data-ttu-id="39465-104">\_Message AGENTSTATUSEX de ligne</span><span class="sxs-lookup"><span data-stu-id="39465-104">LINE\_AGENTSTATUSEX message</span></span>

<span data-ttu-id="39465-105">Le message de **ligne \_ AGENTSTATUSEX** est envoyé lorsque l’état d’un agent ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte.</span><span class="sxs-lookup"><span data-stu-id="39465-105">The **LINE\_AGENTSTATUSEX** message is sent when the status of an ACD agent changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="39465-106">Ce message est généré à l’aide de la fonction [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="39465-106">This message is generated using [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="39465-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39465-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39465-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="39465-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="39465-109">Handle de l’application sur le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="39465-109">The application's handle to the line device.</span></span> <span data-ttu-id="39465-110">Cela est relatif au gestionnaire de l’agent.</span><span class="sxs-lookup"><span data-stu-id="39465-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="39465-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="39465-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="39465-112">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="39465-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="39465-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="39465-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="39465-114">Handle de l’agent dont l’État a changé.</span><span class="sxs-lookup"><span data-stu-id="39465-114">The handle of the agent whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="39465-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="39465-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="39465-116">Spécifie l’état de la file d’attente qui a changé.</span><span class="sxs-lookup"><span data-stu-id="39465-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="39465-117">Il peut s’agir d’une ou plusieurs des [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="39465-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="39465-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="39465-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="39465-119">Si *dwParam2* comprend le \_ bit d’État LINEAGENTSTATUSEX, *dwParam3* indique la nouvelle valeur de l’état de l’agent, qui est l’une des [**\_ constantes LINEAGENTSTATEEX**](lineagentstateex--constants.md).</span><span class="sxs-lookup"><span data-stu-id="39465-119">If *dwParam2* includes the LINEAGENTSTATUSEX \_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="39465-120">Sinon, *dwParam3* a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="39465-120">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39465-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39465-121">Requirements</span></span>



| <span data-ttu-id="39465-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39465-122">Requirement</span></span> | <span data-ttu-id="39465-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="39465-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="39465-124">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="39465-124">TAPI version</span></span><br/> | <span data-ttu-id="39465-125">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="39465-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="39465-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="39465-126">Header</span></span><br/>       | <dl> <span data-ttu-id="39465-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="39465-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39465-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39465-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39465-129">**lineGetAgentInfo**</span><span class="sxs-lookup"><span data-stu-id="39465-129">**lineGetAgentInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[<span data-ttu-id="39465-130">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="39465-130">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




