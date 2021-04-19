---
description: Le \_ message AGENTSTATUS de ligne TAPI est envoyé lorsque l’état d’un agent ACD change sur une ligne ouverte par l’application. L’application peut appeler lineGetAgentStatus pour déterminer l’état actuel de l’agent.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: Message LINE_AGENTSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521664"
---
# <a name="line_agentstatus-message"></a><span data-ttu-id="8328c-104">\_Message AGENTSTATUS de ligne</span><span class="sxs-lookup"><span data-stu-id="8328c-104">LINE\_AGENTSTATUS message</span></span>

<span data-ttu-id="8328c-105">Le message **\_ AGENTSTATUS de ligne** TAPI est envoyé lorsque l’état d’un agent ACD change sur une ligne ouverte par l’application.</span><span class="sxs-lookup"><span data-stu-id="8328c-105">The TAPI **LINE\_AGENTSTATUS** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="8328c-106">L’application peut appeler [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) pour déterminer l’état actuel de l’agent.</span><span class="sxs-lookup"><span data-stu-id="8328c-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="8328c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8328c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8328c-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="8328c-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="8328c-109">Handle de l’application sur le périphérique de ligne sur lequel l’état de l’agent a changé.</span><span class="sxs-lookup"><span data-stu-id="8328c-109">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="8328c-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="8328c-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="8328c-111">Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8328c-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="8328c-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="8328c-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="8328c-113">Identificateur de l’adresse sur la ligne sur laquelle l’état de l’agent a été modifié.</span><span class="sxs-lookup"><span data-stu-id="8328c-113">Identifier of the address on the line on which the agent status changed.</span></span> <span data-ttu-id="8328c-114">Un identificateur d’adresse est associé de manière permanente à une adresse ; l’identificateur reste constant entre les mises à niveau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8328c-114">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="8328c-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="8328c-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="8328c-116">Spécifie l’état de l’agent qui a changé ; peut être une combinaison de [**\_ constantes LINEAGENTSTATUS**](lineagentstatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8328c-116">Specifies the agent status that has changed; can be a combination of [**LINEAGENTSTATUS\_ constants**](lineagentstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8328c-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="8328c-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="8328c-118">Si *dwParam2* comprend le \_ bit d’État LINEAGENTSTATUS, *dwParam3* indique la nouvelle valeur du membre **dwState** dans [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span><span class="sxs-lookup"><span data-stu-id="8328c-118">If *dwParam2* includes the LINEAGENTSTATUS\_STATE bit, then *dwParam3* indicates the new value of the **dwState** member in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span></span> <span data-ttu-id="8328c-119">Dans le cas contraire, ce paramètre a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="8328c-119">Otherwise, this parameter is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8328c-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8328c-120">Return value</span></span>

<span data-ttu-id="8328c-121">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="8328c-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8328c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="8328c-122">Remarks</span></span>

<span data-ttu-id="8328c-123">Le message de **ligne \_ AGENTSTATUS** n’est pas envoyé aux applications qui prennent en charge des versions antérieures de TAPI.</span><span class="sxs-lookup"><span data-stu-id="8328c-123">The **LINE\_AGENTSTATUS** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="8328c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8328c-124">Requirements</span></span>



| <span data-ttu-id="8328c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8328c-125">Requirement</span></span> | <span data-ttu-id="8328c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8328c-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8328c-127">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8328c-127">TAPI version</span></span><br/> | <span data-ttu-id="8328c-128">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8328c-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8328c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="8328c-129">Header</span></span><br/>       | <dl> <span data-ttu-id="8328c-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8328c-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8328c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8328c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8328c-132">**LINEAGENTSTATUS**</span><span class="sxs-lookup"><span data-stu-id="8328c-132">**LINEAGENTSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[<span data-ttu-id="8328c-133">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="8328c-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




