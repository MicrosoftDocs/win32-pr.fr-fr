---
description: Le \_ message APPNEWCALLHUB de ligne TAPI est envoyé pour informer une application quand un nouveau hub d’appel a été créé.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: Message LINE_APPNEWCALLHUB (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543874"
---
# <a name="line_appnewcallhub-message"></a><span data-ttu-id="2f2a6-103">\_Message APPNEWCALLHUB de ligne</span><span class="sxs-lookup"><span data-stu-id="2f2a6-103">LINE\_APPNEWCALLHUB message</span></span>

<span data-ttu-id="2f2a6-104">Le message **\_ APPNEWCALLHUB de ligne** TAPI est envoyé pour informer une application quand un nouveau hub d’appel a été créé.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-104">The TAPI **LINE\_APPNEWCALLHUB** message is sent to inform an application when a new call hub has been created.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="2f2a6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f2a6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f2a6-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="2f2a6-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="2f2a6-107">Handle de l’appel.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="2f2a6-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="2f2a6-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="2f2a6-109">Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="2f2a6-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="2f2a6-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="2f2a6-111">Le niveau de suivi sur le nouveau Hub, tel que défini par l’une des [**\_ constantes LINECALLHUBTRACKING**](linecallhubtracking--constants.md).</span><span class="sxs-lookup"><span data-stu-id="2f2a6-111">The tracking level on the new hub, as defined by one of the [**LINECALLHUBTRACKING\_ Constants**](linecallhubtracking--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f2a6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f2a6-112">Return value</span></span>

<span data-ttu-id="2f2a6-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f2a6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2f2a6-114">Remarks</span></span>

<span data-ttu-id="2f2a6-115">Ce message provient de l’interface TAPI plutôt que d’un fournisseur de services, ce qui signifie qu’il n’y a aucun message TSPI correspondant.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-115">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f2a6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f2a6-116">Requirements</span></span>



| <span data-ttu-id="2f2a6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f2a6-117">Requirement</span></span> | <span data-ttu-id="2f2a6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f2a6-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2f2a6-119">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="2f2a6-119">TAPI version</span></span><br/> | <span data-ttu-id="2f2a6-120">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="2f2a6-120">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="2f2a6-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f2a6-121">Header</span></span><br/>       | <dl> <span data-ttu-id="2f2a6-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f2a6-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




