---
description: Le \_ message de ligne GROUPSTATUS est envoyé lorsque l’état d’un groupe ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction lineProxyMessage.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: Message LINE_GROUPSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533040"
---
# <a name="line_groupstatus-message"></a><span data-ttu-id="6b9b7-104">\_Message GROUPSTATUS de ligne</span><span class="sxs-lookup"><span data-stu-id="6b9b7-104">LINE\_GROUPSTATUS message</span></span>

<span data-ttu-id="6b9b7-105">Le message de **ligne \_ GROUPSTATUS** est envoyé lorsque l’état d’un groupe ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-105">The **LINE\_GROUPSTATUS** message is sent when the status of an ACD group changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="6b9b7-106">Ce message est généré à l’aide de la fonction [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="6b9b7-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="6b9b7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b9b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b9b7-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="6b9b7-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9b7-109">Handle de l’application sur le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-109">The application's handle to the line device.</span></span> <span data-ttu-id="6b9b7-110">Cela est relatif au gestionnaire de l’agent.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="6b9b7-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="6b9b7-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9b7-112">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="6b9b7-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6b9b7-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9b7-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-114">Reserved.</span></span> <span data-ttu-id="6b9b7-115">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-115">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6b9b7-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6b9b7-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9b7-117">Spécifie l’état du groupe qui a changé.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-117">Specifies the group status that has changed.</span></span> <span data-ttu-id="6b9b7-118">L’application peut appeler [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) pour déterminer les modifications apportées aux groupes disponibles.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-118">The application can invoke [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) to determine the changes in available groups.</span></span> <span data-ttu-id="6b9b7-119">Le paramètre *dwParam2* est une ou plusieurs des [**\_ constantes LINEGROUPSTATUS**](linegroupstatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="6b9b7-119">The *dwParam2* parameter is one or more of the [**LINEGROUPSTATUS\_ constants**](linegroupstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b9b7-120">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="6b9b7-120">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9b7-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-121">Reserved.</span></span> <span data-ttu-id="6b9b7-122">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="6b9b7-122">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b9b7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b9b7-123">Requirements</span></span>



| <span data-ttu-id="6b9b7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b9b7-124">Requirement</span></span> | <span data-ttu-id="6b9b7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b9b7-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6b9b7-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="6b9b7-126">TAPI version</span></span><br/> | <span data-ttu-id="6b9b7-127">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="6b9b7-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="6b9b7-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b9b7-128">Header</span></span><br/>       | <dl> <span data-ttu-id="6b9b7-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b9b7-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b9b7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b9b7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b9b7-131">**lineGetGroupList**</span><span class="sxs-lookup"><span data-stu-id="6b9b7-131">**lineGetGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




