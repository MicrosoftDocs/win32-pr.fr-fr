---
description: Le \_ message de ligne QUEUESTATUS est envoyé lorsque l’état d’une file d’attente ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction lineProxyMessage.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: Message LINE_QUEUESTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525283"
---
# <a name="line_queuestatus-message"></a><span data-ttu-id="b2685-104">\_Message QUEUESTATUS de ligne</span><span class="sxs-lookup"><span data-stu-id="b2685-104">LINE\_QUEUESTATUS message</span></span>

<span data-ttu-id="b2685-105">Le message de **ligne \_ QUEUESTATUS** est envoyé lorsque l’état d’une file d’attente ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte.</span><span class="sxs-lookup"><span data-stu-id="b2685-105">The **LINE\_QUEUESTATUS** message is sent when the status of an ACD queue changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="b2685-106">Ce message est généré à l’aide de la fonction [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="b2685-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="b2685-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2685-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2685-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="b2685-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b2685-109">Handle de l’application sur le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="b2685-109">The application's handle to the line device.</span></span> <span data-ttu-id="b2685-110">Cela est relatif au gestionnaire de l’agent.</span><span class="sxs-lookup"><span data-stu-id="b2685-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="b2685-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="b2685-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b2685-112">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="b2685-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="b2685-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b2685-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b2685-114">Identificateur de la file d’attente dont l’État a changé.</span><span class="sxs-lookup"><span data-stu-id="b2685-114">The identifier of the queue whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="b2685-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b2685-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b2685-116">Spécifie l’état de la file d’attente qui a changé.</span><span class="sxs-lookup"><span data-stu-id="b2685-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="b2685-117">Il peut s’agir d’une ou plusieurs des [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b2685-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2685-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b2685-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b2685-119">Réservé.</span><span class="sxs-lookup"><span data-stu-id="b2685-119">Reserved.</span></span> <span data-ttu-id="b2685-120">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b2685-120">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2685-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2685-121">Requirements</span></span>



| <span data-ttu-id="b2685-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2685-122">Requirement</span></span> | <span data-ttu-id="b2685-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2685-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b2685-124">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="b2685-124">TAPI version</span></span><br/> | <span data-ttu-id="b2685-125">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="b2685-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="b2685-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2685-126">Header</span></span><br/>       | <dl> <span data-ttu-id="b2685-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2685-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2685-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2685-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2685-129">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="b2685-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




