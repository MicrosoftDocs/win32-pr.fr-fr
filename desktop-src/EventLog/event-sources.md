---
description: Chaque journal dans la clé EventLog contient des sous-clés appelées sources d’événements. La source de l’événement est le nom du logiciel qui enregistre l’événement.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Sources de l’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544800"
---
# <a name="event-sources"></a><span data-ttu-id="246c2-104">Sources de l’événement</span><span class="sxs-lookup"><span data-stu-id="246c2-104">Event Sources</span></span>

<span data-ttu-id="246c2-105">Chaque journal dans la [clé EventLog](eventlog-key.md) contient des sous-clés appelées *sources d’événements*.</span><span class="sxs-lookup"><span data-stu-id="246c2-105">Each log in the [Eventlog key](eventlog-key.md) contains subkeys called *event sources*.</span></span> <span data-ttu-id="246c2-106">La source de l’événement est le nom du logiciel qui enregistre l’événement.</span><span class="sxs-lookup"><span data-stu-id="246c2-106">The event source is the name of the software that logs the event.</span></span> <span data-ttu-id="246c2-107">Il s’agit généralement du nom de l’application ou du nom d’un sous-composant de l’application si l’application est volumineuse.</span><span class="sxs-lookup"><span data-stu-id="246c2-107">It is often the name of the application or the name of a subcomponent of the application if the application is large.</span></span> <span data-ttu-id="246c2-108">Vous pouvez ajouter au maximum 16 384 sources d’événements au registre.</span><span class="sxs-lookup"><span data-stu-id="246c2-108">You can add a maximum of 16,384 event sources to the registry.</span></span> <span data-ttu-id="246c2-109">Le journal de **sécurité** est réservé à l’usage du système.</span><span class="sxs-lookup"><span data-stu-id="246c2-109">The **Security** log is for system use only.</span></span> <span data-ttu-id="246c2-110">Les pilotes de périphérique doivent ajouter leurs noms dans le journal **système** .</span><span class="sxs-lookup"><span data-stu-id="246c2-110">Device drivers should add their names to the **System** log.</span></span> <span data-ttu-id="246c2-111">Les applications et les services doivent ajouter leurs noms au journal des **applications** ou créer un journal personnalisé.</span><span class="sxs-lookup"><span data-stu-id="246c2-111">Applications and services should add their names to the **Application** log or create a custom log.</span></span>

<span data-ttu-id="246c2-112">La structure des sources d’événements est la suivante :</span><span class="sxs-lookup"><span data-stu-id="246c2-112">The structure of the event sources is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

<span data-ttu-id="246c2-113">Vous ne pouvez pas utiliser un nom de source qui a déjà été utilisé comme nom de journal.</span><span class="sxs-lookup"><span data-stu-id="246c2-113">You cannot use a source name that has already been used as a log name.</span></span> <span data-ttu-id="246c2-114">En outre, les noms de source ne peuvent pas être hiérarchiques ; autrement dit, ils ne peuvent pas contenir de barre oblique inverse (« \\ »).</span><span class="sxs-lookup"><span data-stu-id="246c2-114">In addition, source names cannot be hierarchical; that is, they cannot contain the backslash character ("\\").</span></span>

<span data-ttu-id="246c2-115">Chaque source d’événement contient des informations (par exemple, un [fichier de message](message-files.md)) spécifiques au logiciel qui consignera les événements, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="246c2-115">Each event source contains information (such as a [message file](message-files.md)) specific to the software that will be logging the events, as shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="246c2-116">Valeur de Registre</span><span class="sxs-lookup"><span data-stu-id="246c2-116">Registry Value</span></span></th>
<th><span data-ttu-id="246c2-117">Description</span><span class="sxs-lookup"><span data-stu-id="246c2-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="246c2-118"><strong>CategoryCount</strong></span><span class="sxs-lookup"><span data-stu-id="246c2-118"><strong>CategoryCount</strong></span></span></td>
<td><span data-ttu-id="246c2-119">Nombre de catégories d’événements prises en charge.</span><span class="sxs-lookup"><span data-stu-id="246c2-119">Number of event categories supported.</span></span> <span data-ttu-id="246c2-120">Cette valeur est de type <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="246c2-120">This value is of type <strong>REG_DWORD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="246c2-121"><strong>CategoryMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="246c2-121"><strong>CategoryMessageFile</strong></span></span></td>
<td><span data-ttu-id="246c2-122">Chemin d’accès au fichier de message de catégorie.</span><span class="sxs-lookup"><span data-stu-id="246c2-122">Path to the category message file.</span></span> <span data-ttu-id="246c2-123">Un fichier de message de catégorie contient des chaînes dépendantes de la langue qui décrivent les catégories.</span><span class="sxs-lookup"><span data-stu-id="246c2-123">A category message file contains language-dependent strings that describe the categories.</span></span> <span data-ttu-id="246c2-124">Cette valeur peut être de type <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="246c2-124">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="246c2-125"><strong>EventMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="246c2-125"><strong>EventMessageFile</strong></span></span></td>
<td><span data-ttu-id="246c2-126">Chemin d’accès à un ou plusieurs fichiers de messages d’événement ; Utilisez un point-virgule pour délimiter plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="246c2-126">Path to one or more event message files; use a semicolon to delimit multiple files.</span></span> <span data-ttu-id="246c2-127">Un fichier de message d’événement contient des chaînes dépendantes de la langue qui décrivent les événements.</span><span class="sxs-lookup"><span data-stu-id="246c2-127">An event message file contains language-dependent strings that describe the events.</span></span> <span data-ttu-id="246c2-128">Cette valeur peut être de type <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="246c2-128">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="246c2-129"><strong>ParameterMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="246c2-129"><strong>ParameterMessageFile</strong></span></span></td>
<td><span data-ttu-id="246c2-130">Chemin d’accès au fichier de messages de paramètres.</span><span class="sxs-lookup"><span data-stu-id="246c2-130">Path to the parameter message file.</span></span> <span data-ttu-id="246c2-131">Un fichier de message de paramètre contient des chaînes indépendantes du langage qui doivent être insérées dans les chaînes de description de l’événement.</span><span class="sxs-lookup"><span data-stu-id="246c2-131">A parameter message file contains language-independent strings that are to be inserted into the event description strings.</span></span> <span data-ttu-id="246c2-132">Cette valeur peut être de type <strong>REG_SZ</strong> ou <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="246c2-132">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="246c2-133"><strong>TypesSupported</strong></span><span class="sxs-lookup"><span data-stu-id="246c2-133"><strong>TypesSupported</strong></span></span></td>
<td><span data-ttu-id="246c2-134">Masque de rébinaire des types pris en charge.</span><span class="sxs-lookup"><span data-stu-id="246c2-134">Bitmask of supported types.</span></span> <span data-ttu-id="246c2-135">Cette valeur est de type <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="246c2-135">This value is of type <strong>REG_DWORD</strong>.</span></span> <span data-ttu-id="246c2-136">Il peut s’agir d’une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="246c2-136">It can be one or more of the following values:</span></span> <dl> <span data-ttu-id="246c2-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span><span class="sxs-lookup"><span data-stu-id="246c2-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span></span><br /><span data-ttu-id="246c2-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span><span class="sxs-lookup"><span data-stu-id="246c2-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span></span><br /><span data-ttu-id="246c2-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span><span class="sxs-lookup"><span data-stu-id="246c2-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span></span><br /><span data-ttu-id="246c2-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span><span class="sxs-lookup"><span data-stu-id="246c2-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span></span><br /><span data-ttu-id="246c2-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span><span class="sxs-lookup"><span data-stu-id="246c2-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="246c2-142">Lorsqu’une application utilise la fonction [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) ou [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) pour obtenir un handle vers un journal des événements, le service de journalisation des événements recherche la source d’événement spécifiée dans le registre.</span><span class="sxs-lookup"><span data-stu-id="246c2-142">When an application uses the [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to get a handle to an event log, the event logging service searches for the specified event source in the registry.</span></span> <span data-ttu-id="246c2-143">Par exemple, le journal des **applications** peut contenir des sources d’événements pour Microsoft SQL Server et Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="246c2-143">For example, the **Application** log might contain event sources for Microsoft SQL Server and Microsoft Excel.</span></span> <span data-ttu-id="246c2-144">Si une application utilise [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) ou **OpenEventLog** avec un nom source d’application, SQL ou Excel, le service de journalisation des événements retourne un handle au journal des **applications** .</span><span class="sxs-lookup"><span data-stu-id="246c2-144">If an application uses [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or **OpenEventLog** with a source name of Application, SQL, or Excel, the event logging service returns a handle to the **Application** log.</span></span>

<span data-ttu-id="246c2-145">Une application peut utiliser le journal des **applications** sans ajouter une nouvelle source d’événement au registre.</span><span class="sxs-lookup"><span data-stu-id="246c2-145">An application can use the **Application** log without adding a new event source to the registry.</span></span> <span data-ttu-id="246c2-146">Si l’application appelle [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) et transmet un nom de source qui est introuvable dans le registre, le service de journalisation des événements utilise par défaut le journal des **applications** .</span><span class="sxs-lookup"><span data-stu-id="246c2-146">If the application calls [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) and passes a source name that cannot be found in the registry, the event-logging service uses the **Application** log by default.</span></span> <span data-ttu-id="246c2-147">Toutefois, étant donné qu’il n’y a aucun fichier de message, les observateur d’événements ne peuvent pas mapper d’identificateurs d’événements ou de catégories d’événements à une chaîne de description, et affichent une erreur.</span><span class="sxs-lookup"><span data-stu-id="246c2-147">However, because there are no message files, the Event Viewer cannot map any event identifiers or event categories to a description string, and will display an error.</span></span> <span data-ttu-id="246c2-148">Pour cette raison, vous devez ajouter une source d’événement unique au registre pour votre application et spécifier un fichier de message.</span><span class="sxs-lookup"><span data-stu-id="246c2-148">For this reason, you should add a unique event source to the registry for your application and specify a message file.</span></span>

 

 



