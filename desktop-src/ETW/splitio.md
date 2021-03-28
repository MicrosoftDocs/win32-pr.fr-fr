---
description: Cette classe est la classe parente pour les événements d’e/s fractionnées. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: SplitIo, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: f2efc14ce8804852f983ebe9dcb852c8c0669899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972794"
---
# <a name="splitio-class"></a><span data-ttu-id="32e86-104">SplitIo, classe</span><span class="sxs-lookup"><span data-stu-id="32e86-104">SplitIo class</span></span>

<span data-ttu-id="32e86-105">Cette classe est la classe parente pour les événements d’e/s fractionnées.</span><span class="sxs-lookup"><span data-stu-id="32e86-105">This class is the parent class for split IO events.</span></span>

<span data-ttu-id="32e86-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="32e86-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e86-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32e86-107">Syntax</span></span>

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="32e86-108">Membres</span><span class="sxs-lookup"><span data-stu-id="32e86-108">Members</span></span>

<span data-ttu-id="32e86-109">La classe **SplitIo** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="32e86-109">The **SplitIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="32e86-110">Notes</span><span class="sxs-lookup"><span data-stu-id="32e86-110">Remarks</span></span>

<span data-ttu-id="32e86-111">Pour activer les événements d’e/s fractionnés dans une session de journalisation du noyau NT, spécifiez l’indicateur d' **\_ \_ \_ \_ e/s Split** de l’indicateur de suivi d’événement dans le membre **EnableFlags** d’une structure de [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="32e86-111">To enable split IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_SPLIT\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="32e86-112">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements d’e/s fractionnées en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**SplitIoGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="32e86-112">Event trace consumers can implement special processing for split IO events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**SplitIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="32e86-113">Utilisez le type d’événement suivant pour identifier l’événement réel lors de la consommation d’événements.</span><span class="sxs-lookup"><span data-stu-id="32e86-113">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="32e86-114">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="32e86-114">Event type</span></span>           | <span data-ttu-id="32e86-115">Description</span><span class="sxs-lookup"><span data-stu-id="32e86-115">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32e86-116">Valeur de type d’événement, 32</span><span class="sxs-lookup"><span data-stu-id="32e86-116">Event type value, 32</span></span> | <span data-ttu-id="32e86-117">Événement de fractionnement d’e/s.</span><span class="sxs-lookup"><span data-stu-id="32e86-117">Split IO event.</span></span> <span data-ttu-id="32e86-118">La classe [**SplitIo \_ info**](splitio-info.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="32e86-118">The [**SplitIo\_Info**](splitio-info.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="32e86-119">Les événements de fractionnement des e/s indiquent que les demandes d’e/s ont été fractionnées en plusieurs demandes d’e/s disque en raison du disque de mise en miroir sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="32e86-119">Split IO events indicate that the IO requests have been split into multiple disk IO requests due to the underlying mirroring disk hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="32e86-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="32e86-120">Requirements</span></span>



| <span data-ttu-id="32e86-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32e86-121">Requirement</span></span> | <span data-ttu-id="32e86-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="32e86-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="32e86-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32e86-123">Minimum supported client</span></span><br/> | <span data-ttu-id="32e86-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32e86-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="32e86-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32e86-125">Minimum supported server</span></span><br/> | <span data-ttu-id="32e86-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32e86-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
