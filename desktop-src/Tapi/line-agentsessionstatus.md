---
description: Le \_ message de ligne AGENTSESSIONSTATUS est envoyé lorsque l’état d’une session de l’agent ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction lineProxyMessage.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: Message LINE_AGENTSESSIONSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537809"
---
# <a name="line_agentsessionstatus-message"></a><span data-ttu-id="34b23-104">\_Message AGENTSESSIONSTATUS de ligne</span><span class="sxs-lookup"><span data-stu-id="34b23-104">LINE\_AGENTSESSIONSTATUS message</span></span>

<span data-ttu-id="34b23-105">Le message de **ligne \_ AGENTSESSIONSTATUS** est envoyé lorsque l’état d’une session de l’agent ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte.</span><span class="sxs-lookup"><span data-stu-id="34b23-105">The **LINE\_AGENTSESSIONSTATUS** message is sent when the status of an ACD agent session changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="34b23-106">Ce message est généré à l’aide de la fonction [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="34b23-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="34b23-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34b23-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34b23-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="34b23-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="34b23-109">Handle de l’application sur le périphérique de ligne sur lequel l’état de session de l’agent a été modifié.</span><span class="sxs-lookup"><span data-stu-id="34b23-109">The application's handle to the line device on which the agent session status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="34b23-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="34b23-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="34b23-111">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="34b23-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="34b23-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="34b23-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="34b23-113">Handle de la session de l’agent dont l’État a changé.</span><span class="sxs-lookup"><span data-stu-id="34b23-113">A handle of the agent session whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="34b23-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="34b23-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="34b23-115">Spécifie l’état de session de l’agent qui a changé.</span><span class="sxs-lookup"><span data-stu-id="34b23-115">Specifies the agent session status that has changed.</span></span> <span data-ttu-id="34b23-116">Il peut s’agir d’une ou plusieurs **lignes \_ AGENTSESSIONSTATUS**.</span><span class="sxs-lookup"><span data-stu-id="34b23-116">Can be one or more of the **LINE\_AGENTSESSIONSTATUS**.</span></span>

</dd> <dt>

<span data-ttu-id="34b23-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="34b23-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="34b23-118">Si *dwParam2* comprend le \_ bit d’État LINEAGENTSTATUSEX, *dwParam3* indique la nouvelle valeur de l’état de l’agent, qui est l’une des [**\_ constantes LINEAGENTSTATEEX**](lineagentstateex--constants.md).</span><span class="sxs-lookup"><span data-stu-id="34b23-118">If *dwParam2* includes the LINEAGENTSTATUSEX\_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="34b23-119">Sinon, *dwParam3* a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="34b23-119">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34b23-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34b23-120">Requirements</span></span>



| <span data-ttu-id="34b23-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34b23-121">Requirement</span></span> | <span data-ttu-id="34b23-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="34b23-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="34b23-123">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="34b23-123">TAPI version</span></span><br/> | <span data-ttu-id="34b23-124">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="34b23-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="34b23-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="34b23-125">Header</span></span><br/>       | <dl> <span data-ttu-id="34b23-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="34b23-126"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b23-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34b23-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b23-128">**lineGetAgentSessionInfo**</span><span class="sxs-lookup"><span data-stu-id="34b23-128">**lineGetAgentSessionInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[<span data-ttu-id="34b23-129">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="34b23-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




