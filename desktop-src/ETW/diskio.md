---
description: Cette classe est la classe parente pour les événements d’e/s de disque. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: E, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97f9907e4da51675bb1a5f562931e471ee0e133e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951003"
---
# <a name="diskio-class"></a><span data-ttu-id="792b5-104">E, classe</span><span class="sxs-lookup"><span data-stu-id="792b5-104">DiskIo class</span></span>

<span data-ttu-id="792b5-105">Cette classe est la classe parente pour les événements d’e/s de disque.</span><span class="sxs-lookup"><span data-stu-id="792b5-105">This class is the parent class for disk I/O events.</span></span>

<span data-ttu-id="792b5-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="792b5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="792b5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="792b5-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="792b5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="792b5-108">Members</span></span>

<span data-ttu-id="792b5-109">La classe **e** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="792b5-109">The **DiskIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="792b5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="792b5-110">Remarks</span></span>

<span data-ttu-id="792b5-111">Pour activer les événements d’e/s de disque dans une session de journalisation du noyau NT, spécifiez l’indicateur d' **\_ e/ \_ \_ \_ s disque** de l’indicateur de trace d’événements dans le membre **EnableFlags** d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="792b5-111">To enable disk I/0 events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="792b5-112">Vous pouvez également spécifier un ou plusieurs des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="792b5-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="792b5-113">**indicateur de trace d’événements, \_ \_ \_ initialisation des \_ e/s disque \_**</span><span class="sxs-lookup"><span data-stu-id="792b5-113">**EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT**</span></span>
-   <span data-ttu-id="792b5-114">**\_pilote d' \_ indicateur de trace d’événements \_**</span><span class="sxs-lookup"><span data-stu-id="792b5-114">**EVENT\_TRACE\_FLAG\_DRIVER**</span></span>

<span data-ttu-id="792b5-115">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements d’e/s disque en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**DiskIoGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="792b5-115">Event trace consumers can implement special processing for disk I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**DiskIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="792b5-116">Utilisez les types d’événements suivants pour identifier l’événement d’e/s disque réel lors de la consommation d’événements.</span><span class="sxs-lookup"><span data-stu-id="792b5-116">Use the following event types to identify the actual disk I/O event when consuming events.</span></span>



| <span data-ttu-id="792b5-117">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="792b5-117">Event type</span></span>                                                                      | <span data-ttu-id="792b5-118">Description</span><span class="sxs-lookup"><span data-stu-id="792b5-118">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="792b5-119">**Événement \_ \_Lecture des \_ e \_ /s du type de suivi**(la valeur du type d’événement est 10)</span><span class="sxs-lookup"><span data-stu-id="792b5-119">**EVENT\_TRACE\_TYPE\_IO\_READ**(Event type value is 10)</span></span><br/>             | <span data-ttu-id="792b5-120">Événement Read.</span><span class="sxs-lookup"><span data-stu-id="792b5-120">Read event.</span></span> <span data-ttu-id="792b5-121">La classe [**e \_ TypeGroup1**](diskio-typegroup1.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="792b5-121">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                              |
| <span data-ttu-id="792b5-122">**Événement \_ Type de TRACE \_ \_ \_ écriture d’e/s**(la valeur du type d’événement est 11)</span><span class="sxs-lookup"><span data-stu-id="792b5-122">**EVENT\_TRACE\_TYPE\_IO\_WRITE**(Event type value is 11)</span></span><br/>            | <span data-ttu-id="792b5-123">Événement d’écriture.</span><span class="sxs-lookup"><span data-stu-id="792b5-123">Write event.</span></span> <span data-ttu-id="792b5-124">La classe [**e \_ TypeGroup1**](diskio-typegroup1.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="792b5-124">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                             |
| <span data-ttu-id="792b5-125">**Événement \_ Type de TRACE \_ \_ e \_ Read \_ init**(type d’événement : valeur 12)</span><span class="sxs-lookup"><span data-stu-id="792b5-125">**EVENT\_TRACE\_TYPE\_IO\_READ\_INIT**(Event type value is 12)</span></span><br/>       | <span data-ttu-id="792b5-126">Initialise l’événement de lecture.</span><span class="sxs-lookup"><span data-stu-id="792b5-126">Initialize read event.</span></span> <span data-ttu-id="792b5-127">La classe [**e \_ TypeGroup2**](diskio-typegroup2.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="792b5-127">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="792b5-128">**Événement \_ Type de suivi \_ \_ e/s \_ écriture/écriture \_**(la valeur du type d’événement est 13)</span><span class="sxs-lookup"><span data-stu-id="792b5-128">**EVENT\_TRACE\_TYPE\_IO\_WRITE\_INIT**(Event type value is 13)</span></span><br/>      | <span data-ttu-id="792b5-129">Initialise l’événement d’écriture.</span><span class="sxs-lookup"><span data-stu-id="792b5-129">Initialize write event.</span></span> <span data-ttu-id="792b5-130">La classe [**e \_ TypeGroup2**](diskio-typegroup2.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="792b5-130">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="792b5-131">**Événement \_ Type de TRACE \_ \_ \_ vidage des e/s**(la valeur du type d’événement est 14)</span><span class="sxs-lookup"><span data-stu-id="792b5-131">**EVENT\_TRACE\_TYPE\_IO\_FLUSH**(Event type value is 14)</span></span><br/>            | <span data-ttu-id="792b5-132">Initialise l’événement d’écriture.</span><span class="sxs-lookup"><span data-stu-id="792b5-132">Initialize write event.</span></span> <span data-ttu-id="792b5-133">La classe [**e \_ TypeGroup3**](diskio-typegroup3.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="792b5-133">The [**DiskIo\_TypeGroup3**](diskio-typegroup3.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="792b5-134">**Événement \_ Type de suivi \_ \_ IO \_ flush \_ init**(la valeur de type d’événement est 15)</span><span class="sxs-lookup"><span data-stu-id="792b5-134">**EVENT\_TRACE\_TYPE\_IO\_FLUSH\_INIT**(Event type value is 15)</span></span><br/>      | <span data-ttu-id="792b5-135">Initialise l’événement Flush.</span><span class="sxs-lookup"><span data-stu-id="792b5-135">Initialize flush event.</span></span> <span data-ttu-id="792b5-136">La classe [**e \_ TypeGroup2**](diskio-typegroup2.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="792b5-136">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="792b5-137">**Événement \_ Type de suivi \_ \_ e/s \_ redirigée \_ init**(la valeur du type d’événement est 16)</span><span class="sxs-lookup"><span data-stu-id="792b5-137">**EVENT\_TRACE\_TYPE\_IO\_REDIRECTED\_INIT**(Event type value is 16)</span></span><br/> | <span data-ttu-id="792b5-138">Initialise l’événement Redirigé.</span><span class="sxs-lookup"><span data-stu-id="792b5-138">Initialize redirected event.</span></span> <span data-ttu-id="792b5-139">Les événements d’e/s redirigés permettent de mapper le disque IOs à un fichier WIM (Windows Imaging Format) sur le nom de fichier dans le fichier WIM.</span><span class="sxs-lookup"><span data-stu-id="792b5-139">Redirected IO events are used to map disk IOs to a Windows Imaging Format (WIM) to the filename within the WIM.</span></span>                  |
| <span data-ttu-id="792b5-140">La valeur du type d’événement est 52</span><span class="sxs-lookup"><span data-stu-id="792b5-140">Event type value is 52</span></span><br/>                                               | <span data-ttu-id="792b5-141">Événement de demande complète du pilote.</span><span class="sxs-lookup"><span data-stu-id="792b5-141">Driver complete request event.</span></span> <span data-ttu-id="792b5-142">La classe MOF [**DriverCompleteRequest**](drivercompleterequest.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="792b5-142">The [**DriverCompleteRequest**](drivercompleterequest.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="792b5-143">La valeur du type d’événement est 53</span><span class="sxs-lookup"><span data-stu-id="792b5-143">Event type value is 53</span></span><br/>                                               | <span data-ttu-id="792b5-144">Événement de retour de demande complet du pilote.</span><span class="sxs-lookup"><span data-stu-id="792b5-144">Driver complete request return event.</span></span> <span data-ttu-id="792b5-145">La classe MOF [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="792b5-145">The [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="792b5-146">La valeur du type d’événement est 37</span><span class="sxs-lookup"><span data-stu-id="792b5-146">Event type value is 37</span></span><br/>                                               | <span data-ttu-id="792b5-147">Événement de routine de fin d’exécution du pilote.</span><span class="sxs-lookup"><span data-stu-id="792b5-147">Driver completion routine event.</span></span> <span data-ttu-id="792b5-148">La classe MOF [**DriverCompletionRoutine**](drivercompletionroutine.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="792b5-148">The [**DriverCompletionRoutine**](drivercompletionroutine.md) MOF class defines the event data for this event.</span></span>              |
| <span data-ttu-id="792b5-149">La valeur du type d’événement est 34</span><span class="sxs-lookup"><span data-stu-id="792b5-149">Event type value is 34</span></span><br/>                                               | <span data-ttu-id="792b5-150">Événement d’appel de fonction principale du pilote.</span><span class="sxs-lookup"><span data-stu-id="792b5-150">Driver major function call event.</span></span> <span data-ttu-id="792b5-151">La classe MOF [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="792b5-151">The [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) MOF class defines the event data for this event.</span></span>             |
| <span data-ttu-id="792b5-152">La valeur du type d’événement est 35</span><span class="sxs-lookup"><span data-stu-id="792b5-152">Event type value is 35</span></span><br/>                                               | <span data-ttu-id="792b5-153">Événement de retour d’appel de fonction principale du pilote.</span><span class="sxs-lookup"><span data-stu-id="792b5-153">Driver major function call return event.</span></span> <span data-ttu-id="792b5-154">La classe MOF [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="792b5-154">The [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="792b5-155">Le fournisseur d’e/s disque ne peut pas identifier le fichier qui est lu ou écrit pendant un événement d’e/s disque.</span><span class="sxs-lookup"><span data-stu-id="792b5-155">The disk I/0 provider cannot identify which file is read or written during a disk I/O event.</span></span> <span data-ttu-id="792b5-156">Pour récupérer le nom du fichier associé à l’événement d’e/s disque, activez le fournisseur d’événements file I/0.</span><span class="sxs-lookup"><span data-stu-id="792b5-156">To retrieve the name of the file associated with the disk I/O event, enable the file I/0 event provider.</span></span>

<span data-ttu-id="792b5-157">Les événements d’e/s de disque sont enregistrés au moment de l’exécution des e/s.</span><span class="sxs-lookup"><span data-stu-id="792b5-157">Disk I/O events are recorded at the I/O completion time.</span></span> <span data-ttu-id="792b5-158">Pour déterminer à quel moment l’opération d’e/s a commencé, utilisez les événements d’initialisation, par exemple, le type de suivi d’événement \_ \_ \_ IO \_ Read \_ init.</span><span class="sxs-lookup"><span data-stu-id="792b5-158">To determine when the I/O operation began, use the initialization events, for example, EVENT\_TRACE\_TYPE\_IO\_READ\_INIT.</span></span>

## <a name="requirements"></a><span data-ttu-id="792b5-159">Spécifications</span><span class="sxs-lookup"><span data-stu-id="792b5-159">Requirements</span></span>



| <span data-ttu-id="792b5-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="792b5-160">Requirement</span></span> | <span data-ttu-id="792b5-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="792b5-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="792b5-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="792b5-162">Minimum supported client</span></span><br/> | <span data-ttu-id="792b5-163">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="792b5-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="792b5-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="792b5-164">Minimum supported server</span></span><br/> | <span data-ttu-id="792b5-165">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="792b5-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="792b5-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="792b5-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="792b5-167">**E \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="792b5-167">**DiskIo\_TypeGroup1**</span></span>](diskio-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="792b5-168">**E \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="792b5-168">**DiskIo\_TypeGroup2**</span></span>](diskio-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="792b5-169">**E \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="792b5-169">**DiskIo\_TypeGroup3**</span></span>](diskio-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="792b5-170">**DriverCompleteRequest**</span><span class="sxs-lookup"><span data-stu-id="792b5-170">**DriverCompleteRequest**</span></span>](drivercompleterequest.md)
</dt> <dt>

[<span data-ttu-id="792b5-171">**DriverCompleteRequestReturn**</span><span class="sxs-lookup"><span data-stu-id="792b5-171">**DriverCompleteRequestReturn**</span></span>](drivercompleterequestreturn.md)
</dt> <dt>

[<span data-ttu-id="792b5-172">**DriverCompletionRoutine**</span><span class="sxs-lookup"><span data-stu-id="792b5-172">**DriverCompletionRoutine**</span></span>](drivercompletionroutine.md)
</dt> <dt>

[<span data-ttu-id="792b5-173">**DriverMajorFunctionCall**</span><span class="sxs-lookup"><span data-stu-id="792b5-173">**DriverMajorFunctionCall**</span></span>](drivermajorfunctioncall.md)
</dt> <dt>

[<span data-ttu-id="792b5-174">**DriverMajorFunctionReturn**</span><span class="sxs-lookup"><span data-stu-id="792b5-174">**DriverMajorFunctionReturn**</span></span>](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
