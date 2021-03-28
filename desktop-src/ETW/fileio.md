---
description: Cette classe est la classe parente pour les événements d’e/s de fichier. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: FileIo (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f7c032cb7af325efa1d2ea76702068fc7b3be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972798"
---
# <a name="fileio-class"></a><span data-ttu-id="e5731-104">FileIo (classe)</span><span class="sxs-lookup"><span data-stu-id="e5731-104">FileIo class</span></span>

<span data-ttu-id="e5731-105">Cette classe est la classe parente pour les événements d’e/s de fichier.</span><span class="sxs-lookup"><span data-stu-id="e5731-105">This class is the parent class for file I/O events.</span></span>

<span data-ttu-id="e5731-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="e5731-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5731-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5731-107">Syntax</span></span>

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="e5731-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e5731-108">Members</span></span>

<span data-ttu-id="e5731-109">La classe **FileIo** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="e5731-109">The **FileIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5731-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e5731-110">Remarks</span></span>

<span data-ttu-id="e5731-111">Pour activer les événements d’e/s de fichier dans une session de journalisation du noyau NT, spécifiez l’indicateur d' **\_ \_ \_ \_ \_ e/s de fichier disque** de l’indicateur de trace d’événements dans le membre **EnableFlags** d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="e5731-111">To enable the File IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="e5731-112">Vous pouvez également spécifier un ou plusieurs des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="e5731-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="e5731-113">**\_ \_ \_ e/s de fichier d’indicateur de trace d’événements \_**</span><span class="sxs-lookup"><span data-stu-id="e5731-113">**EVENT\_TRACE\_FLAG\_FILE\_IO**</span></span>
-   <span data-ttu-id="e5731-114">**événement d’indicateur de trace d’événements \_ \_ \_ \_ \_ init**</span><span class="sxs-lookup"><span data-stu-id="e5731-114">**EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT**</span></span>

<span data-ttu-id="e5731-115">Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements d’e/s de fichier en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**FileIoGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* .</span><span class="sxs-lookup"><span data-stu-id="e5731-115">Event trace consumers can implement special processing for file I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**FileIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="e5731-116">Utilisez les types d’événements suivants pour identifier l’événement réel lors de la consommation d’événements.</span><span class="sxs-lookup"><span data-stu-id="e5731-116">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="e5731-117">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="e5731-117">Event type</span></span>             | <span data-ttu-id="e5731-118">Description</span><span class="sxs-lookup"><span data-stu-id="e5731-118">Description</span></span>                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5731-119">La valeur du type d’événement est 0</span><span class="sxs-lookup"><span data-stu-id="e5731-119">Event type value is 0</span></span>  | <span data-ttu-id="e5731-120">Événement de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="e5731-120">File name event.</span></span> <span data-ttu-id="e5731-121">La classe MOF [**\_ nom FileIo**](fileio-name.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-121">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                               |
| <span data-ttu-id="e5731-122">La valeur du type d’événement est 32</span><span class="sxs-lookup"><span data-stu-id="e5731-122">Event type value is 32</span></span> | <span data-ttu-id="e5731-123">Événement de création de fichier.</span><span class="sxs-lookup"><span data-stu-id="e5731-123">File create event.</span></span> <span data-ttu-id="e5731-124">La classe MOF [**\_ nom FileIo**](fileio-name.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-124">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="e5731-125">La valeur du type d’événement est 35</span><span class="sxs-lookup"><span data-stu-id="e5731-125">Event type value is 35</span></span> | <span data-ttu-id="e5731-126">Événement de suppression de fichier.</span><span class="sxs-lookup"><span data-stu-id="e5731-126">File delete event.</span></span> <span data-ttu-id="e5731-127">La classe MOF [**\_ nom FileIo**](fileio-name.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-127">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="e5731-128">La valeur du type d’événement est 36</span><span class="sxs-lookup"><span data-stu-id="e5731-128">Event type value is 36</span></span> | <span data-ttu-id="e5731-129">Événement d’arrêt de fichier.</span><span class="sxs-lookup"><span data-stu-id="e5731-129">File rundown event.</span></span> <span data-ttu-id="e5731-130">Énumère tous les fichiers ouverts sur l’ordinateur à la fin de la session de suivi.</span><span class="sxs-lookup"><span data-stu-id="e5731-130">Enumerates all open files on the computer at the end of the trace session.</span></span> <span data-ttu-id="e5731-131">La classe MOF [**\_ nom FileIo**](fileio-name.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-131">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="e5731-132">La valeur du type d’événement est 64</span><span class="sxs-lookup"><span data-stu-id="e5731-132">Event type value is 64</span></span> | <span data-ttu-id="e5731-133">Événement de création de fichier.</span><span class="sxs-lookup"><span data-stu-id="e5731-133">File create event.</span></span> <span data-ttu-id="e5731-134">La classe [**FileIo \_ Create**](fileio-create.md) MOF définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-134">The [**FileIo\_Create**](fileio-create.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="e5731-135">La valeur du type d’événement est 72</span><span class="sxs-lookup"><span data-stu-id="e5731-135">Event type value is 72</span></span> | <span data-ttu-id="e5731-136">Événement d’énumération de répertoire.</span><span class="sxs-lookup"><span data-stu-id="e5731-136">Directory enumeration event.</span></span> <span data-ttu-id="e5731-137">La [**classe \_ DirEnum FileIo de FileIo**](fileio-direnum.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-137">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                             |
| <span data-ttu-id="e5731-138">La valeur du type d’événement est 77</span><span class="sxs-lookup"><span data-stu-id="e5731-138">Event type value is 77</span></span> | <span data-ttu-id="e5731-139">Événement de notification d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="e5731-139">Directory notification event.</span></span> <span data-ttu-id="e5731-140">La [**classe \_ DirEnum FileIo de FileIo**](fileio-direnum.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-140">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="e5731-141">La valeur du type d’événement est 69</span><span class="sxs-lookup"><span data-stu-id="e5731-141">Event type value is 69</span></span> | <span data-ttu-id="e5731-142">Définir un événement d’informations.</span><span class="sxs-lookup"><span data-stu-id="e5731-142">Set information event.</span></span> <span data-ttu-id="e5731-143">La classe MOF [**\_ info de FileIo**](fileio-info.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-143">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="e5731-144">La valeur du type d’événement est 70</span><span class="sxs-lookup"><span data-stu-id="e5731-144">Event type value is 70</span></span> | <span data-ttu-id="e5731-145">Supprimer un événement de fichier.</span><span class="sxs-lookup"><span data-stu-id="e5731-145">Delete file event.</span></span> <span data-ttu-id="e5731-146">La classe MOF [**\_ info de FileIo**](fileio-info.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-146">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="e5731-147">La valeur du type d’événement est 71</span><span class="sxs-lookup"><span data-stu-id="e5731-147">Event type value is 71</span></span> | <span data-ttu-id="e5731-148">Renommer l’événement de fichier.</span><span class="sxs-lookup"><span data-stu-id="e5731-148">Rename file event.</span></span> <span data-ttu-id="e5731-149">La classe MOF [**\_ info de FileIo**](fileio-info.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-149">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="e5731-150">La valeur du type d’événement est 74</span><span class="sxs-lookup"><span data-stu-id="e5731-150">Event type value is 74</span></span> | <span data-ttu-id="e5731-151">Événement d’informations de fichier de requête.</span><span class="sxs-lookup"><span data-stu-id="e5731-151">Query file information event.</span></span> <span data-ttu-id="e5731-152">La classe MOF [**\_ info de FileIo**](fileio-info.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-152">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="e5731-153">La valeur du type d’événement est 75</span><span class="sxs-lookup"><span data-stu-id="e5731-153">Event type value is 75</span></span> | <span data-ttu-id="e5731-154">Événement de contrôle du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e5731-154">File system control event.</span></span> <span data-ttu-id="e5731-155">La classe MOF [**\_ info de FileIo**](fileio-info.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-155">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="e5731-156">La valeur du type d’événement est 76</span><span class="sxs-lookup"><span data-stu-id="e5731-156">Event type value is 76</span></span> | <span data-ttu-id="e5731-157">Événement de fin d’opération.</span><span class="sxs-lookup"><span data-stu-id="e5731-157">End of operation event.</span></span> <span data-ttu-id="e5731-158">La classe MOF [**\_ ouverte FileIo**](fileio-opend.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-158">The [**FileIo\_OpEnd**](fileio-opend.md) MOF class defines the event data for this event.</span></span>                                                                      |
| <span data-ttu-id="e5731-159">La valeur du type d’événement est 67</span><span class="sxs-lookup"><span data-stu-id="e5731-159">Event type value is 67</span></span> | <span data-ttu-id="e5731-160">Événement de lecture de fichier.</span><span class="sxs-lookup"><span data-stu-id="e5731-160">File read event.</span></span> <span data-ttu-id="e5731-161">La classe MOF [**\_ ReadWrite de FileIo**](fileio-readwrite.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-161">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="e5731-162">La valeur du type d’événement est 68</span><span class="sxs-lookup"><span data-stu-id="e5731-162">Event type value is 68</span></span> | <span data-ttu-id="e5731-163">Événement d’écriture de fichier.</span><span class="sxs-lookup"><span data-stu-id="e5731-163">File write event.</span></span> <span data-ttu-id="e5731-164">La classe MOF [**\_ ReadWrite de FileIo**](fileio-readwrite.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-164">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                    |
| <span data-ttu-id="e5731-165">La valeur du type d’événement est 65</span><span class="sxs-lookup"><span data-stu-id="e5731-165">Event type value is 65</span></span> | <span data-ttu-id="e5731-166">Événement de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="e5731-166">Clean up event.</span></span> <span data-ttu-id="e5731-167">L’événement est généré lorsque le dernier handle du fichier est libéré.</span><span class="sxs-lookup"><span data-stu-id="e5731-167">The event is generated when the last handle to the file is released.</span></span> <span data-ttu-id="e5731-168">La [**classe \_ SimpleOp FileIo de FileIo**](fileio-simpleop.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-168">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="e5731-169">La valeur du type d’événement est 66</span><span class="sxs-lookup"><span data-stu-id="e5731-169">Event type value is 66</span></span> | <span data-ttu-id="e5731-170">Événement de fermeture.</span><span class="sxs-lookup"><span data-stu-id="e5731-170">Close event.</span></span> <span data-ttu-id="e5731-171">L’événement est généré lorsque l’objet fichier est libéré.</span><span class="sxs-lookup"><span data-stu-id="e5731-171">The event is generated when the file object is freed.</span></span> <span data-ttu-id="e5731-172">La [**classe \_ SimpleOp FileIo de FileIo**](fileio-simpleop.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-172">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>                     |
| <span data-ttu-id="e5731-173">La valeur du type d’événement est 73</span><span class="sxs-lookup"><span data-stu-id="e5731-173">Event type value is 73</span></span> | <span data-ttu-id="e5731-174">Événement de vidage.</span><span class="sxs-lookup"><span data-stu-id="e5731-174">Flush event.</span></span> <span data-ttu-id="e5731-175">Cet événement est généré lorsque les mémoires tampons de fichier sont entièrement vidées sur le disque.</span><span class="sxs-lookup"><span data-stu-id="e5731-175">This event is generated when the file buffers are fully flushed to disk.</span></span> <span data-ttu-id="e5731-176">La [**classe \_ SimpleOp FileIo de FileIo**](fileio-simpleop.md) définit les données d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5731-176">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="e5731-177">Les événements d’e/s de fichier sont journalisés au début de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e5731-177">File IO events are logged at the beginning of the operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5731-178">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e5731-178">Requirements</span></span>



| <span data-ttu-id="e5731-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5731-179">Requirement</span></span> | <span data-ttu-id="e5731-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5731-180">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e5731-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5731-181">Minimum supported client</span></span><br/> | <span data-ttu-id="e5731-182">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5731-182">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e5731-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5731-183">Minimum supported server</span></span><br/> | <span data-ttu-id="e5731-184">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5731-184">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5731-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5731-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5731-186">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="e5731-186">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="e5731-187">**FileIo \_ v0**</span><span class="sxs-lookup"><span data-stu-id="e5731-187">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> <dt>

[<span data-ttu-id="e5731-188">**FileIo \_ v1**</span><span class="sxs-lookup"><span data-stu-id="e5731-188">**FileIo\_V1**</span></span>](fileio-v1.md)
</dt> </dl>

 

 
