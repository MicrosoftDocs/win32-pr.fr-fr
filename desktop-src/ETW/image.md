---
description: Cette classe est la classe parente pour les événements d’image. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Classe Image
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973307"
---
# <a name="image-class"></a><span data-ttu-id="5bf9f-104">Classe Image</span><span class="sxs-lookup"><span data-stu-id="5bf9f-104">Image class</span></span>

<span data-ttu-id="5bf9f-105">Cette classe est la classe parente pour les événements d’image.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-105">This class is the parent class for image events.</span></span>

<span data-ttu-id="5bf9f-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bf9f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bf9f-107">Syntax</span></span>

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="5bf9f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5bf9f-108">Members</span></span>

<span data-ttu-id="5bf9f-109">La classe **image** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-109">The **Image** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bf9f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5bf9f-110">Remarks</span></span>

<span data-ttu-id="5bf9f-111">Pour activer les événements d’image dans une session de journalisation du noyau NT, spécifiez l’indicateur de chargement d’image de l’indicateur de trace d’événements dans le membre **EnableFlags** de la structure des [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5bf9f-111">To enable image events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_IMAGE\_LOAD** flag in the **EnableFlags** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="5bf9f-112">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de chargement d’image en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**ImageLoadGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="5bf9f-112">Event trace consumers can implement special processing for image load events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ImageLoadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="5bf9f-113">Utilisez les types d’événements suivants pour identifier les événements de chargement d’image lors de l’utilisation d’événements.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-113">Use the following event types to identify image load events when consuming events.</span></span>



| <span data-ttu-id="5bf9f-114">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="5bf9f-114">Event type</span></span>                                                          | <span data-ttu-id="5bf9f-115">Description</span><span class="sxs-lookup"><span data-stu-id="5bf9f-115">Description</span></span>                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf9f-116">**Événement \_ Type de TRACE \_ \_ Load**(la valeur de type d’événement est 10)</span><span class="sxs-lookup"><span data-stu-id="5bf9f-116">**EVENT\_TRACE\_TYPE\_LOAD**(Event type value is 10)</span></span><br/>     | <span data-ttu-id="5bf9f-117">Événement de chargement d’image.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-117">Image load event.</span></span> <span data-ttu-id="5bf9f-118">Généré lors du chargement d’une DLL ou d’un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-118">Generated when a DLL or executable file is loaded.</span></span> <span data-ttu-id="5bf9f-119">Le fournisseur génère un seul événement pour la première fois qu’une DLL donnée est chargée.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-119">The provider generates only one event for the first time a given DLL is loaded.</span></span> <span data-ttu-id="5bf9f-120">La classe MOF de [**\_ chargement d’image**](image-load.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-120">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="5bf9f-121">**Événement \_ \_ \_ Fin du type de suivi**(la valeur du type d’événement est 2)</span><span class="sxs-lookup"><span data-stu-id="5bf9f-121">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>       | <span data-ttu-id="5bf9f-122">Événement de déchargement d’image.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-122">Image unload event.</span></span> <span data-ttu-id="5bf9f-123">Généré lorsqu’une DLL ou un fichier exécutable est déchargé.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-123">Generated when a DLL or executable file is unloaded.</span></span> <span data-ttu-id="5bf9f-124">Le fournisseur génère un seul événement pour la dernière fois qu’une DLL donnée est déchargée.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-124">The provider generates only one event for the last time a given DLL is unloaded.</span></span> <span data-ttu-id="5bf9f-125">La classe MOF de [**\_ chargement d’image**](image-load.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-125">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="5bf9f-126">**Événement \_ Type de suivi \_ \_ DC \_ Start**(la valeur du type d’événement est 3)</span><span class="sxs-lookup"><span data-stu-id="5bf9f-126">**EVENT\_TRACE\_TYPE\_DC\_START**(Event type value is 3)</span></span><br/> | <span data-ttu-id="5bf9f-127">Événement de démarrage de la collecte de données.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-127">Data collection start event.</span></span> <span data-ttu-id="5bf9f-128">Énumère toutes les images chargées au début de la trace.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-128">Enumerates all loaded images at the beginning of the trace.</span></span> <span data-ttu-id="5bf9f-129">La classe MOF de [**\_ chargement d’image**](image-load.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-129">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="5bf9f-130">**Événement \_ \_Type de \_ trace \_ end DC**(la valeur du type d’événement est 4)</span><span class="sxs-lookup"><span data-stu-id="5bf9f-130">**EVENT\_TRACE\_TYPE\_DC\_END**(Event type value is 4)</span></span><br/>   | <span data-ttu-id="5bf9f-131">Événement de fin de la collecte de données.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-131">Data collection end event.</span></span> <span data-ttu-id="5bf9f-132">Énumère toutes les images chargées à la fin de la trace.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-132">Enumerates all loaded images at the end of the trace.</span></span> <span data-ttu-id="5bf9f-133">La classe MOF de [**\_ chargement d’image**](image-load.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="5bf9f-133">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="5bf9f-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5bf9f-134">Requirements</span></span>



| <span data-ttu-id="5bf9f-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bf9f-135">Requirement</span></span> | <span data-ttu-id="5bf9f-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bf9f-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5bf9f-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bf9f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5bf9f-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bf9f-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5bf9f-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bf9f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5bf9f-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bf9f-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5bf9f-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bf9f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bf9f-142">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="5bf9f-142">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="5bf9f-143">**Chargement d’image \_**</span><span class="sxs-lookup"><span data-stu-id="5bf9f-143">**Image\_Load**</span></span>](image-load.md)
</dt> <dt>

[<span data-ttu-id="5bf9f-144">**Image \_ v0**</span><span class="sxs-lookup"><span data-stu-id="5bf9f-144">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="5bf9f-145">**Image \_ v1**</span><span class="sxs-lookup"><span data-stu-id="5bf9f-145">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 
