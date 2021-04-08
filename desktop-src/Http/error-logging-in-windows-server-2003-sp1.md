---
title: Journalisation des erreurs dans Windows Server 2003 SP1
description: Journalisation des erreurs dans Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Journalisation des erreurs dans Windows Server 2003 avec Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b82c816dab39877f700973de3c0c7798034d124
ms.sourcegitcommit: 7bdca1558c21be976be950a213c5a072c449f111
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2019
ms.locfileid: "103679093"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a><span data-ttu-id="ce095-104">Journalisation des erreurs dans Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="ce095-104">Error Logging in Windows Server 2003 SP1</span></span>

## <a name="addition-of-w3c-style-headers"></a><span data-ttu-id="ce095-105">Ajout d’en-têtes de style W3C</span><span class="sxs-lookup"><span data-stu-id="ce095-105">Addition of W3C Style Headers</span></span>

<span data-ttu-id="ce095-106">À compter de Windows Server 2003 avec Service Pack 1 (SP1), le journal des erreurs de l’API du serveur HTTP comprend des en-têtes de style W3C permettant d’analyser les fichiers journaux à l’aide d’analyseurs de journaux standard.</span><span class="sxs-lookup"><span data-stu-id="ce095-106">Starting with Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API error log includes W3C style headers allowing log files to be parsed using standard log parsers.</span></span> <span data-ttu-id="ce095-107">Le modèle ci-dessous répertorie tous les champs qui peuvent être consignés dans le fichier journal des erreurs http.</span><span class="sxs-lookup"><span data-stu-id="ce095-107">The template shown below lists all the fields that can be logged in the http error log file.</span></span>

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a><span data-ttu-id="ce095-108">Journalisation des champs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ce095-108">Logging Additional Fields</span></span>

<span data-ttu-id="ce095-109">Le journal des erreurs HTTP a été étendu pour inclure neuf champs supplémentaires afin de consigner les données relatives aux échecs qui se produisent.</span><span class="sxs-lookup"><span data-stu-id="ce095-109">The HTTP error log has been extended to include nine more fields to log data about failures that occur.</span></span> <span data-ttu-id="ce095-110">Les nouveaux champs d’erreur sont répertoriés ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ce095-110">The new error fields are listed below:</span></span>

-   <span data-ttu-id="ce095-111">Nom de l’ordinateur serveur \[ S-ComputerName\]</span><span class="sxs-lookup"><span data-stu-id="ce095-111">Server Computer Name \[S-COMPUTERNAME\]</span></span>
-   <span data-ttu-id="ce095-112">Agent utilisateur \[ cs ( \_ agent utilisateur)\]</span><span class="sxs-lookup"><span data-stu-id="ce095-112">User Agent \[CS(USER\_AGENT)\]</span></span>
-   <span data-ttu-id="ce095-113">Cookie \[ cs (cookie)\]</span><span class="sxs-lookup"><span data-stu-id="ce095-113">Cookie \[CS(COOKIE)\]</span></span>
-   <span data-ttu-id="ce095-114">\[point de renvoi CS (Referrer)\]</span><span class="sxs-lookup"><span data-stu-id="ce095-114">referrer \[CS(referrer)\]</span></span>
-   <span data-ttu-id="ce095-115">Nom d’hôte \[ CS-Host\]</span><span class="sxs-lookup"><span data-stu-id="ce095-115">Host Name \[CS-HOST\]</span></span>
-   <span data-ttu-id="ce095-116">Octets reçus par le serveur \[ , SC-octets\]</span><span class="sxs-lookup"><span data-stu-id="ce095-116">Bytes received by the server \[SC-BYTES\]</span></span>
-   <span data-ttu-id="ce095-117">Octets reçus et traités par le serveur \[ cs-bytes\]</span><span class="sxs-lookup"><span data-stu-id="ce095-117">Bytes received and processed by the server \[CS-BYTES\]</span></span>
-   <span data-ttu-id="ce095-118">Temps nécessaire pour traiter le temps de requête \[ -pris\]</span><span class="sxs-lookup"><span data-stu-id="ce095-118">Time Taken to process the request \[TIME-TAKEN\]</span></span>
-   <span data-ttu-id="ce095-119">Queue-Name (réservé pour IIS) \[ S-QUEUENAME\]</span><span class="sxs-lookup"><span data-stu-id="ce095-119">Queue-Name (Reserved for IIS) \[S-QUEUENAME\]</span></span>

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a><span data-ttu-id="ce095-120">Sélection des fichiers à consigner dans le fichier journal des erreurs HTTP</span><span class="sxs-lookup"><span data-stu-id="ce095-120">Selecting Fileds to Log in the HTTP Error Log File</span></span>

<span data-ttu-id="ce095-121">La clé de Registre **ErrorLoggingFields** a été ajoutée pour contrôler les champs consignés dans le journal des erreurs http.</span><span class="sxs-lookup"><span data-stu-id="ce095-121">The **ErrorLoggingFields** registry key has been added to control the fields logged into the HTTP error log.</span></span> <span data-ttu-id="ce095-122">Ces valeurs de Registre se trouvent sous une \\ clé de paramètres http située à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="ce095-122">This registry values is located under an HTTP\\Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

<span data-ttu-id="ce095-123">La valeur de Registre **ErrorLoggingFields** est une valeur DWORD qui contient des valeurs de bit pour chacun des champs pouvant être journalisés.</span><span class="sxs-lookup"><span data-stu-id="ce095-123">The **ErrorLoggingFields** registry value is a DWORD value that contains bit values for each of the fields that can be logged.</span></span> <span data-ttu-id="ce095-124">Pour activer la journalisation d’un champ spécifique, définissez sa valeur de bit correspondante sur 1 et redémarrez le service HTTP.</span><span class="sxs-lookup"><span data-stu-id="ce095-124">To enable logging of a specific field, set its corresponding bit value to 1 and restart the HTTP service.</span></span> <span data-ttu-id="ce095-125">Pour désactiver la journalisation, définissez la valeur de bit sur 0.</span><span class="sxs-lookup"><span data-stu-id="ce095-125">To disable logging, set the bit value to 0.</span></span> <span data-ttu-id="ce095-126">Pour configurer plusieurs champs, utilisez une opération or au niveau du bit des valeurs individuelles.</span><span class="sxs-lookup"><span data-stu-id="ce095-126">To configure multiple fields, use a bitwise OR of the individual values.</span></span> <span data-ttu-id="ce095-127">Par exemple, pour activer les champs de journalisation des cookies et des référents, la valeur doit être 0x00020000 \| 0x00040000 = 0x00060000.</span><span class="sxs-lookup"><span data-stu-id="ce095-127">For example, to turn on the Cookie and Referrer logging fields, the value should be 0x00020000 \| 0x00040000 = 0x00060000.</span></span> <span data-ttu-id="ce095-128">Si la clé de Registre **ErrorLoggingFields** est absente, les champs par défaut sont journalisés.</span><span class="sxs-lookup"><span data-stu-id="ce095-128">If the **ErrorLoggingFields** registry key is absent, the default fields are logged.</span></span> <span data-ttu-id="ce095-129">La valeur **ErrorLoggingFields** pour enregistrer les champs par défaut est 0x7c884c7.</span><span class="sxs-lookup"><span data-stu-id="ce095-129">The **ErrorLoggingFields** value to log the default fields is 0x7c884c7.</span></span> <span data-ttu-id="ce095-130">Pour activer la journalisation de tous les champs affichés dans le tableau ci-dessous, définissez la valeur sur 0x7dff4e7.</span><span class="sxs-lookup"><span data-stu-id="ce095-130">To enable logging for all the fields shown in the table below, set the value to 0x7dff4e7.</span></span>

<span data-ttu-id="ce095-131">Les champs de journalisation des erreurs sont répertoriés dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ce095-131">The error logging fields are listed in the following table:</span></span>



| <span data-ttu-id="ce095-132">Champ de journal</span><span class="sxs-lookup"><span data-stu-id="ce095-132">Log field</span></span>            | <span data-ttu-id="ce095-133">Consigné par défaut</span><span class="sxs-lookup"><span data-stu-id="ce095-133">Logged by default</span></span> | <span data-ttu-id="ce095-134">Valeur en bits</span><span class="sxs-lookup"><span data-stu-id="ce095-134">Bit value</span></span>  |
|----------------------|-------------------|------------|
| <span data-ttu-id="ce095-135">Date</span><span class="sxs-lookup"><span data-stu-id="ce095-135">Date</span></span>                 | <span data-ttu-id="ce095-136">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-136">Yes</span></span>               | <span data-ttu-id="ce095-137">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ce095-137">0x00000001</span></span> |
| <span data-ttu-id="ce095-138">Temps</span><span class="sxs-lookup"><span data-stu-id="ce095-138">Time</span></span>                 | <span data-ttu-id="ce095-139">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-139">Yes</span></span>               | <span data-ttu-id="ce095-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ce095-140">0x00000002</span></span> |
| <span data-ttu-id="ce095-141">Nom de l’ordinateur serveur</span><span class="sxs-lookup"><span data-stu-id="ce095-141">Server Computer Name</span></span> | <span data-ttu-id="ce095-142">Non</span><span class="sxs-lookup"><span data-stu-id="ce095-142">No</span></span>                | <span data-ttu-id="ce095-143">0x00000020</span><span class="sxs-lookup"><span data-stu-id="ce095-143">0x00000020</span></span> |
| <span data-ttu-id="ce095-144">Adresse IP du client</span><span class="sxs-lookup"><span data-stu-id="ce095-144">Client IP Address</span></span>    | <span data-ttu-id="ce095-145">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-145">Yes</span></span>               | <span data-ttu-id="ce095-146">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ce095-146">0x00000004</span></span> |
| <span data-ttu-id="ce095-147">Port client</span><span class="sxs-lookup"><span data-stu-id="ce095-147">Client Port</span></span>          | <span data-ttu-id="ce095-148">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-148">Yes</span></span>               | <span data-ttu-id="ce095-149">0x00400000</span><span class="sxs-lookup"><span data-stu-id="ce095-149">0x00400000</span></span> |
| <span data-ttu-id="ce095-150">Adresse IP du serveur</span><span class="sxs-lookup"><span data-stu-id="ce095-150">Server IP Address</span></span>    | <span data-ttu-id="ce095-151">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-151">Yes</span></span>               | <span data-ttu-id="ce095-152">0x00000040</span><span class="sxs-lookup"><span data-stu-id="ce095-152">0x00000040</span></span> |
| <span data-ttu-id="ce095-153">Port du serveur</span><span class="sxs-lookup"><span data-stu-id="ce095-153">Server Port</span></span>          | <span data-ttu-id="ce095-154">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-154">Yes</span></span>               | <span data-ttu-id="ce095-155">0x00008000</span><span class="sxs-lookup"><span data-stu-id="ce095-155">0x00008000</span></span> |
| <span data-ttu-id="ce095-156">Version du protocole</span><span class="sxs-lookup"><span data-stu-id="ce095-156">Protocol Version</span></span>     | <span data-ttu-id="ce095-157">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-157">Yes</span></span>               | <span data-ttu-id="ce095-158">0x00080000</span><span class="sxs-lookup"><span data-stu-id="ce095-158">0x00080000</span></span> |
| <span data-ttu-id="ce095-159">Méthode</span><span class="sxs-lookup"><span data-stu-id="ce095-159">Method</span></span>               | <span data-ttu-id="ce095-160">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-160">Yes</span></span>               | <span data-ttu-id="ce095-161">0x00000080</span><span class="sxs-lookup"><span data-stu-id="ce095-161">0x00000080</span></span> |
| <span data-ttu-id="ce095-162">URI</span><span class="sxs-lookup"><span data-stu-id="ce095-162">URI</span></span>                  | <span data-ttu-id="ce095-163">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-163">Yes</span></span>               | <span data-ttu-id="ce095-164">0x00800000</span><span class="sxs-lookup"><span data-stu-id="ce095-164">0x00800000</span></span> |
| <span data-ttu-id="ce095-165">User Agent</span><span class="sxs-lookup"><span data-stu-id="ce095-165">User Agent</span></span>           | <span data-ttu-id="ce095-166">Non</span><span class="sxs-lookup"><span data-stu-id="ce095-166">No</span></span>                | <span data-ttu-id="ce095-167">0x00010000</span><span class="sxs-lookup"><span data-stu-id="ce095-167">0x00010000</span></span> |
| <span data-ttu-id="ce095-168">Cookie</span><span class="sxs-lookup"><span data-stu-id="ce095-168">Cookie</span></span>               | <span data-ttu-id="ce095-169">Non</span><span class="sxs-lookup"><span data-stu-id="ce095-169">No</span></span>                | <span data-ttu-id="ce095-170">0x00020000</span><span class="sxs-lookup"><span data-stu-id="ce095-170">0x00020000</span></span> |
| <span data-ttu-id="ce095-171">référant</span><span class="sxs-lookup"><span data-stu-id="ce095-171">referrer</span></span>             | <span data-ttu-id="ce095-172">Non</span><span class="sxs-lookup"><span data-stu-id="ce095-172">No</span></span>                | <span data-ttu-id="ce095-173">0x00040000</span><span class="sxs-lookup"><span data-stu-id="ce095-173">0x00040000</span></span> |
| <span data-ttu-id="ce095-174">Host</span><span class="sxs-lookup"><span data-stu-id="ce095-174">Host</span></span>                 | <span data-ttu-id="ce095-175">Non</span><span class="sxs-lookup"><span data-stu-id="ce095-175">No</span></span>                | <span data-ttu-id="ce095-176">0x00100000</span><span class="sxs-lookup"><span data-stu-id="ce095-176">0x00100000</span></span> |
| <span data-ttu-id="ce095-177">État du protocole</span><span class="sxs-lookup"><span data-stu-id="ce095-177">Protocol Status</span></span>      | <span data-ttu-id="ce095-178">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-178">Yes</span></span>               | <span data-ttu-id="ce095-179">0x00000400</span><span class="sxs-lookup"><span data-stu-id="ce095-179">0x00000400</span></span> |
| <span data-ttu-id="ce095-180">SC-Bytes</span><span class="sxs-lookup"><span data-stu-id="ce095-180">SC-Bytes</span></span>             | <span data-ttu-id="ce095-181">Non</span><span class="sxs-lookup"><span data-stu-id="ce095-181">No</span></span>                | <span data-ttu-id="ce095-182">0x00001000</span><span class="sxs-lookup"><span data-stu-id="ce095-182">0x00001000</span></span> |
| <span data-ttu-id="ce095-183">CS-Bytes</span><span class="sxs-lookup"><span data-stu-id="ce095-183">CS-Bytes</span></span>             | <span data-ttu-id="ce095-184">Non</span><span class="sxs-lookup"><span data-stu-id="ce095-184">No</span></span>                | <span data-ttu-id="ce095-185">0x00002000</span><span class="sxs-lookup"><span data-stu-id="ce095-185">0x00002000</span></span> |
| <span data-ttu-id="ce095-186">Durée</span><span class="sxs-lookup"><span data-stu-id="ce095-186">Time Taken</span></span>           | <span data-ttu-id="ce095-187">Non</span><span class="sxs-lookup"><span data-stu-id="ce095-187">No</span></span>                | <span data-ttu-id="ce095-188">0x00004000</span><span class="sxs-lookup"><span data-stu-id="ce095-188">0x00004000</span></span> |
| <span data-ttu-id="ce095-189">SiteId</span><span class="sxs-lookup"><span data-stu-id="ce095-189">SiteId</span></span>               | <span data-ttu-id="ce095-190">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-190">Yes</span></span>               | <span data-ttu-id="ce095-191">0x01000000</span><span class="sxs-lookup"><span data-stu-id="ce095-191">0x01000000</span></span> |
| <span data-ttu-id="ce095-192">Phrase motif</span><span class="sxs-lookup"><span data-stu-id="ce095-192">Reason Phrase</span></span>        | <span data-ttu-id="ce095-193">Oui</span><span class="sxs-lookup"><span data-stu-id="ce095-193">Yes</span></span>               | <span data-ttu-id="ce095-194">0x02000000</span><span class="sxs-lookup"><span data-stu-id="ce095-194">0x02000000</span></span> |
| <span data-ttu-id="ce095-195">Nom de la file d’attente</span><span class="sxs-lookup"><span data-stu-id="ce095-195">Queue Name</span></span>           | <span data-ttu-id="ce095-196">Non</span><span class="sxs-lookup"><span data-stu-id="ce095-196">No</span></span>                | <span data-ttu-id="ce095-197">0x04000000</span><span class="sxs-lookup"><span data-stu-id="ce095-197">0x04000000</span></span> |
| <span data-ttu-id="ce095-198">ID de flux</span><span class="sxs-lookup"><span data-stu-id="ce095-198">Stream Id</span></span>            | <span data-ttu-id="ce095-199">Non</span><span class="sxs-lookup"><span data-stu-id="ce095-199">No</span></span>                | <span data-ttu-id="ce095-200">0x ????????</span><span class="sxs-lookup"><span data-stu-id="ce095-200">0x????????</span></span> |



 

## <a name="time-and-date-rollover"></a><span data-ttu-id="ce095-201">Substitution d’heure et de date</span><span class="sxs-lookup"><span data-stu-id="ce095-201">Time and Date Rollover</span></span>

<span data-ttu-id="ce095-202">Par défaut, un nouveau fichier journal des erreurs HTTP est créé (substitution de fichier terme) quand le fichier journal actuel atteint une taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ce095-202">By default, a new HTTP error log file is created (termed file rollover) when the current log file reaches a specified size.</span></span> <span data-ttu-id="ce095-203">À compter de Windows Server 2003 avec SP1, de nouveaux fichiers journaux des erreurs peuvent être créés en fonction de la date et de l’heure.</span><span class="sxs-lookup"><span data-stu-id="ce095-203">Starting with Windows Server 2003 with SP1, new error log files can be created based on date and time.</span></span> <span data-ttu-id="ce095-204">Les substitutions de date et d’heure sont contrôlées par deux nouvelles valeurs de Registre : **ErrorLoggingRolloverType** et **ErrorLoggingLocaltimeRollover**.</span><span class="sxs-lookup"><span data-stu-id="ce095-204">Time and date rollover are controlled by two new registry values: **ErrorLoggingRolloverType** and **ErrorLoggingLocaltimeRollover**.</span></span> <span data-ttu-id="ce095-205">Pour permettre la substitution d’heure et de date, ces valeurs de Registre doivent être ajoutées au registre.</span><span class="sxs-lookup"><span data-stu-id="ce095-205">To enable time and date rollover, these registry values must be added to the registry.</span></span> <span data-ttu-id="ce095-206">Le service http doit être redémarré lorsque ces clés sont ajoutées au registre.</span><span class="sxs-lookup"><span data-stu-id="ce095-206">The Http service must be restarted when these keys are added to the registry.</span></span> <span data-ttu-id="ce095-207">Les clés de registre de substitution du fichier journal sont créées sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="ce095-207">The log file rollover registry keys are created under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

<span data-ttu-id="ce095-208">La clé de Registre **ErrorLoggingRolloverType** indique le type de substitution souhaité et est défini par défaut sur la substitution basée sur la taille.</span><span class="sxs-lookup"><span data-stu-id="ce095-208">The **ErrorLoggingRolloverType** registry key indicates the type of rollover desired and is by default set to size based rollover.</span></span> <span data-ttu-id="ce095-209">La substitution peut également être définie sur une base quotidienne, hebdomadaire, mensuelle ou horaire.</span><span class="sxs-lookup"><span data-stu-id="ce095-209">Rollover can also be set to occur on a daily, weekly, monthly, or hourly basis.</span></span> <span data-ttu-id="ce095-210">Lorsque la substitution de fichier est basée sur le temps, une valeur **ErrorLoggingLocaltimeRollover** de 0 indique que l’heure de substitution est exprimée en GMT et une valeur de 1 indique que l’heure de substitution est exprimée en heure locale.</span><span class="sxs-lookup"><span data-stu-id="ce095-210">When file rollover is based on time, an **ErrorLoggingLocaltimeRollover** value of 0 indicates that the rollover time is expressed in GMT, and a value of 1 indicates that the rollover time is expressed in local time.</span></span> <span data-ttu-id="ce095-211">La clé **ErrorLoggingRolloverType** peut prendre une valeur comprise entre 0 et 4, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ce095-211">The **ErrorLoggingRolloverType** key can take a value from 0 to 4 as listed in the following table.</span></span>



| <span data-ttu-id="ce095-212">Valeur du type de substitution</span><span class="sxs-lookup"><span data-stu-id="ce095-212">Rollover type value</span></span> | <span data-ttu-id="ce095-213">Description</span><span class="sxs-lookup"><span data-stu-id="ce095-213">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce095-214">0</span><span class="sxs-lookup"><span data-stu-id="ce095-214">0</span></span>                   | <span data-ttu-id="ce095-215">Substitution basée sur la taille.</span><span class="sxs-lookup"><span data-stu-id="ce095-215">Size based rollover.</span></span> <span data-ttu-id="ce095-216">Les fichiers journaux sont restaurés lorsque le fichier atteint la taille définie dans la clé de Registre **ErrorLogFileTruncateSize** .</span><span class="sxs-lookup"><span data-stu-id="ce095-216">Log files are rolled over when the file reaches the size defined in the **ErrorLogFileTruncateSize** registry key.</span></span> |
| <span data-ttu-id="ce095-217">1</span><span class="sxs-lookup"><span data-stu-id="ce095-217">1</span></span>                   | <span data-ttu-id="ce095-218">La substitution du fichier journal a lieu quotidiennement.</span><span class="sxs-lookup"><span data-stu-id="ce095-218">Log file rollover occurs daily.</span></span>                                                                                                         |
| <span data-ttu-id="ce095-219">2</span><span class="sxs-lookup"><span data-stu-id="ce095-219">2</span></span>                   | <span data-ttu-id="ce095-220">La substitution du fichier journal se produit toutes les semaines.</span><span class="sxs-lookup"><span data-stu-id="ce095-220">Log file rollover occurs weekly.</span></span>                                                                                                        |
| <span data-ttu-id="ce095-221">3</span><span class="sxs-lookup"><span data-stu-id="ce095-221">3</span></span>                   | <span data-ttu-id="ce095-222">La substitution du fichier journal a lieu tous les mois.</span><span class="sxs-lookup"><span data-stu-id="ce095-222">Log file rollover occurs monthly.</span></span>                                                                                                       |
| <span data-ttu-id="ce095-223">4</span><span class="sxs-lookup"><span data-stu-id="ce095-223">4</span></span>                   | <span data-ttu-id="ce095-224">La substitution de fichier journal se produit toutes les heures.</span><span class="sxs-lookup"><span data-stu-id="ce095-224">Log file rollover occurs hourly.</span></span>                                                                                                        |



 

<span data-ttu-id="ce095-225">Les conventions d’affectation de noms pour les fichiers qui stockent les journaux d’erreurs sont différentes pour la taille, la date et la substitution temporelle.</span><span class="sxs-lookup"><span data-stu-id="ce095-225">The naming conventions for files that store the error logs are different for size, date, and time based rollover.</span></span> <span data-ttu-id="ce095-226">Le tableau suivant répertorie les conventions d’affectation de noms pour les fichiers journaux http.</span><span class="sxs-lookup"><span data-stu-id="ce095-226">The following table lists the naming conventions for Http log files.</span></span>



| <span data-ttu-id="ce095-227">Type Tollover</span><span class="sxs-lookup"><span data-stu-id="ce095-227">Tollover type</span></span> | <span data-ttu-id="ce095-228">Nom du fichier journal</span><span class="sxs-lookup"><span data-stu-id="ce095-228">Log file name</span></span>  | <span data-ttu-id="ce095-229">Description</span><span class="sxs-lookup"><span data-stu-id="ce095-229">Description</span></span>                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce095-230">Taille</span><span class="sxs-lookup"><span data-stu-id="ce095-230">Size</span></span>          | <span data-ttu-id="ce095-231">HTTPERRn. LOG</span><span class="sxs-lookup"><span data-stu-id="ce095-231">HTTPERRn.LOG</span></span>   | <span data-ttu-id="ce095-232">Le fichier journal est recyclé lorsqu’il atteint une taille spécifique.</span><span class="sxs-lookup"><span data-stu-id="ce095-232">The log file is recycled when it reaches a specific size.</span></span> <span data-ttu-id="ce095-233">n est le numéro de fichier et est incrémenté lorsque le fichier journal est restauré.</span><span class="sxs-lookup"><span data-stu-id="ce095-233">n is the file number and is incremented when the log file is rolled over.</span></span> |
| <span data-ttu-id="ce095-234">Quotidien</span><span class="sxs-lookup"><span data-stu-id="ce095-234">Daily</span></span>         | <span data-ttu-id="ce095-235">htYYMMDD. log</span><span class="sxs-lookup"><span data-stu-id="ce095-235">htYYMMDD.log</span></span>   | <span data-ttu-id="ce095-236">Le fichier journal est recyclé quotidiennement.</span><span class="sxs-lookup"><span data-stu-id="ce095-236">The log file is recycled daily.</span></span>                                                                                                     |
| <span data-ttu-id="ce095-237">Hebdomadaire</span><span class="sxs-lookup"><span data-stu-id="ce095-237">Weekly</span></span>        | <span data-ttu-id="ce095-238">htYYMMww. log</span><span class="sxs-lookup"><span data-stu-id="ce095-238">htYYMMww.log</span></span>   | <span data-ttu-id="ce095-239">Le fichier journal est recyclé chaque semaine, où SS est la semaine du mois.</span><span class="sxs-lookup"><span data-stu-id="ce095-239">The log file is recycled weekly, where ww is the week of the month.</span></span>                                                                 |
| <span data-ttu-id="ce095-240">Mensuelle</span><span class="sxs-lookup"><span data-stu-id="ce095-240">Monthly</span></span>       | <span data-ttu-id="ce095-241">htYYMM. log</span><span class="sxs-lookup"><span data-stu-id="ce095-241">htYYMM.log</span></span>     | <span data-ttu-id="ce095-242">Le fichier journal est recyclé chaque mois.</span><span class="sxs-lookup"><span data-stu-id="ce095-242">The log file is recycled every month.</span></span>                                                                                               |
| <span data-ttu-id="ce095-243">Toutes les heures</span><span class="sxs-lookup"><span data-stu-id="ce095-243">Hourly</span></span>        | <span data-ttu-id="ce095-244">htYYMMDDhh. log</span><span class="sxs-lookup"><span data-stu-id="ce095-244">htYYMMDDhh.log</span></span> | <span data-ttu-id="ce095-245">Le fichier journal est recyclé toutes les heures, où HH est l’heure du jour exprimée en notation de 0-24 heures.</span><span class="sxs-lookup"><span data-stu-id="ce095-245">The log file is recycled hourly, where hh is the hour of the day expressed in 0-24 hour notation.</span></span>                                   |



 

 

 




