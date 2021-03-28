---
description: La session de suivi d’événements autologger enregistre les événements qui se produisent au début du processus de démarrage du système d’exploitation.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Configuration et démarrage d’une session de journalisation automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b17e7e818193aa4fa316d17a0e4392e41b55dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973850"
---
# <a name="configuring-and-starting-an-autologger-session"></a><span data-ttu-id="7eb99-103">Configuration et démarrage d’une session de journalisation automatique</span><span class="sxs-lookup"><span data-stu-id="7eb99-103">Configuring and Starting an AutoLogger Session</span></span>

<span data-ttu-id="7eb99-104">La session de suivi d’événements autologger enregistre les événements qui se produisent au début du processus de démarrage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7eb99-104">The AutoLogger event tracing session records events that occur early in the operating system boot process.</span></span> <span data-ttu-id="7eb99-105">Les applications et les pilotes de périphériques peuvent utiliser la session de journalisation automatique pour capturer des suivis avant que l’utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="7eb99-105">Applications and device drivers can use the AutoLogger session to capture traces before the user logs in.</span></span> <span data-ttu-id="7eb99-106">Notez que certains pilotes de périphérique, tels que les pilotes de périphériques de disque, ne sont pas chargés au moment du démarrage de la session de journalisation automatique.</span><span class="sxs-lookup"><span data-stu-id="7eb99-106">Note that some device drivers, such as disk device drivers, are not loaded at the time the AutoLogger session begins.</span></span>

<span data-ttu-id="7eb99-107">L’enregistreur automatique diffère de l’enregistreur d’événements global des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="7eb99-107">The AutoLogger differs from the Global Logger in the following ways:</span></span>

-   <span data-ttu-id="7eb99-108">Vous pouvez spécifier une ou plusieurs sessions de journalisation automatique (le journal global était une session unique à laquelle tous les événements ont été consignés).</span><span class="sxs-lookup"><span data-stu-id="7eb99-108">You can specify one or more AutoLogger sessions (the Global Logger was a single session to which everyone logged events).</span></span>
-   <span data-ttu-id="7eb99-109">Le journal automatique envoie une notification d’activation aux fournisseurs au démarrage de la session (le journal global n’a pas envoyé de notification d’activation aux fournisseurs, de sorte que les fournisseurs devaient s’appuyer sur d’autres moyens pour savoir si la session de journalisation globale a été démarrée pour commencer à enregistrer des événements).</span><span class="sxs-lookup"><span data-stu-id="7eb99-109">The AutoLogger sends an enable notification to the providers when the session starts (the Global Logger did not send an enable notification to the providers, so the providers had to rely on other means to know if the Global Logger session was started in order to begin logging events).</span></span>
-   <span data-ttu-id="7eb99-110">Le journal automatique ne prend pas en charge la journalisation des événements du journal de noyau NT (voir le membre **EnableFlags** des [**Propriétés de \_ suivi \_ d’événement**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span><span class="sxs-lookup"><span data-stu-id="7eb99-110">The AutoLogger does not support logging NT Kernel Logger events (see the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span></span> <span data-ttu-id="7eb99-111">Pour consigner les événements du journal de noyau NT, vous devez utiliser l’enregistreur d’événements [Global](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="7eb99-111">To log NT Kernel Logger events, you must use the [Global Logger](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="7eb99-112">Pour plus d’informations sur la vue globale de l’enregistreur d’événements, consultez [configuration et démarrage de la session d’enregistreur](configuring-and-starting-the-global-logger-session.md)d’événements globale.</span><span class="sxs-lookup"><span data-stu-id="7eb99-112">For more information on the Global Logger seesion, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

> [!Note]  
> <span data-ttu-id="7eb99-113">ETW prend en charge le journal automatique sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7eb99-113">ETW supports the AutoLogger on Windows Vista and later.</span></span> <span data-ttu-id="7eb99-114">Utilisez l' [enregistreur](configuring-and-starting-the-global-logger-session.md) d’événements global sur les systèmes d’exploitation antérieurs.</span><span class="sxs-lookup"><span data-stu-id="7eb99-114">Use the [Global Logger](configuring-and-starting-the-global-logger-session.md) on earlier operating systems.</span></span>

 

<span data-ttu-id="7eb99-115">Vous utilisez le registre pour configurer la session de journalisation automatique.</span><span class="sxs-lookup"><span data-stu-id="7eb99-115">You use the registry to configure the AutoLogger session.</span></span> <span data-ttu-id="7eb99-116">Ajoutez la clé de Registre suivante, si elle n’est pas déjà présente :</span><span class="sxs-lookup"><span data-stu-id="7eb99-116">Add the following registry key, if it is not already present:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

<span data-ttu-id="7eb99-117">Sous la clé de l' **enregistreur** automatique, créez une clé pour chaque session de journalisation automatique que vous souhaitez configurer, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="7eb99-117">Under the **Autologger** key create a key for each AutoLogger session that you want to configure as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="7eb99-118">Pour chaque session, créez une clé pour chaque fournisseur que vous souhaitez activer dans la session.</span><span class="sxs-lookup"><span data-stu-id="7eb99-118">For each session, create a key for each provider that you want to enable to the session.</span></span> <span data-ttu-id="7eb99-119">Utilisez le GUID du fournisseur comme clé.</span><span class="sxs-lookup"><span data-stu-id="7eb99-119">Use the provider's GUID as the key.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="7eb99-120">Le tableau suivant décrit les valeurs que vous pouvez définir pour chaque session de journalisation automatique.</span><span class="sxs-lookup"><span data-stu-id="7eb99-120">The following table describes the values that you can define for each AutoLogger session.</span></span> <span data-ttu-id="7eb99-121">Vous devez disposer de privilèges d’administrateur pour spécifier ces valeurs de registre.</span><span class="sxs-lookup"><span data-stu-id="7eb99-121">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="7eb99-122">La valeur de **début** et de **GUID** sont les seules valeurs requises pour démarrer la session de journalisation automatique. toutes les autres valeurs ont des paramètres par défaut qui sont utilisés si la valeur n’est pas présente dans le registre.</span><span class="sxs-lookup"><span data-stu-id="7eb99-122">The **Start** and **Guid** value are the only values required to start the AutoLogger session; all other values have default settings that are used if the value is not present in the registry.</span></span> <span data-ttu-id="7eb99-123">En règle générale, vous devez utiliser les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="7eb99-123">Typically, you should use the default values.</span></span> <span data-ttu-id="7eb99-124">Si vous spécifiez une valeur que ETW ne peut pas prendre en charge, ETW remplace la valeur.</span><span class="sxs-lookup"><span data-stu-id="7eb99-124">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7eb99-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7eb99-125">Value</span></span></th>
<th><span data-ttu-id="7eb99-126">Type</span><span class="sxs-lookup"><span data-stu-id="7eb99-126">Type</span></span></th>
<th><span data-ttu-id="7eb99-127">Description</span><span class="sxs-lookup"><span data-stu-id="7eb99-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7eb99-128"><strong>BufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-128"><strong>BufferSize</strong></span></span></td>
<td><span data-ttu-id="7eb99-129"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-129"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-130">Taille de chaque mémoire tampon, en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="7eb99-130">The size of each buffer, in kilobytes.</span></span> <span data-ttu-id="7eb99-131">Doit être inférieur à un mégaoctet.</span><span class="sxs-lookup"><span data-stu-id="7eb99-131">Should be less than one megabyte.</span></span> <span data-ttu-id="7eb99-132">ETW utilise la taille de la mémoire physique pour calculer cette valeur.</span><span class="sxs-lookup"><span data-stu-id="7eb99-132">ETW uses the size of physical memory to calculate this value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb99-133"><strong>ClockType</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-133"><strong>ClockType</strong></span></span></td>
<td><span data-ttu-id="7eb99-134"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-134"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-135">Minuteur à utiliser lors de la journalisation de l’horodatage pour chaque événement.</span><span class="sxs-lookup"><span data-stu-id="7eb99-135">The timer to use when logging the time stamp for each event.</span></span>
<ul>
<li><span data-ttu-id="7eb99-136">1 = valeur de compteur de performance (haute résolution)</span><span class="sxs-lookup"><span data-stu-id="7eb99-136">1 = Performance counter value (high resolution)</span></span></li>
<li><span data-ttu-id="7eb99-137">2 = minuterie du système</span><span class="sxs-lookup"><span data-stu-id="7eb99-137">2 = System timer</span></span></li>
<li><span data-ttu-id="7eb99-138">3 = compteur du cycle de l’UC</span><span class="sxs-lookup"><span data-stu-id="7eb99-138">3 = CPU cycle counter</span></span></li>
</ul>
<span data-ttu-id="7eb99-139">Pour obtenir une description de chaque type d’horloge, consultez le membre <strong>ClientContext</strong> de <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7eb99-139">For a description of each clock type, see the <strong>ClientContext</strong> member of <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span></span><br/> <span data-ttu-id="7eb99-140">La valeur par défaut est 1 (valeur du compteur de performances) sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7eb99-140">The default value is 1 (performance counter value) on Windows Vista and later.</span></span> <span data-ttu-id="7eb99-141">Avant Windows Vista, la valeur par défaut est 2 (horloge système).</span><span class="sxs-lookup"><span data-stu-id="7eb99-141">Prior to Windows Vista, the default value is 2 (system timer).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb99-142"><strong>DisableRealtimePersistence</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-142"><strong>DisableRealtimePersistence</strong></span></span></td>
<td><span data-ttu-id="7eb99-143"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-143"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-144">Pour désactiver la persistance en temps réel, définissez cette valeur sur 1.</span><span class="sxs-lookup"><span data-stu-id="7eb99-144">To disable real time persistence, set this value to 1.</span></span> <span data-ttu-id="7eb99-145">La valeur par défaut est 0 (activé) pour les sessions en temps réel.</span><span class="sxs-lookup"><span data-stu-id="7eb99-145">The default is 0 (enabled) for real time sessions.</span></span><br/> <span data-ttu-id="7eb99-146">Si la persistance en temps réel est activée, les événements en temps réel qui n’ont pas été remis au moment de l’arrêt de l’ordinateur sont conservés.</span><span class="sxs-lookup"><span data-stu-id="7eb99-146">If real time persistence is enabled, real-time events that were not delivered by the time the computer was shutdown will be persisted.</span></span> <span data-ttu-id="7eb99-147">Les événements seront ensuite remis au consommateur la prochaine fois que le consommateur se connectera à la session.</span><span class="sxs-lookup"><span data-stu-id="7eb99-147">The events will then be delivered to the consumer the next time the consumer connects to the session.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb99-148"><strong>FileCounter</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-148"><strong>FileCounter</strong></span></span></td>
<td><span data-ttu-id="7eb99-149"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-149"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-150">Ne définissez pas cette valeur ou modifiez-la.</span><span class="sxs-lookup"><span data-stu-id="7eb99-150">Do not set or modify this value.</span></span> <span data-ttu-id="7eb99-151">Cette valeur est le numéro de série utilisé pour incrémenter le nom du fichier journal si <strong>FileMax</strong> est spécifié.</span><span class="sxs-lookup"><span data-stu-id="7eb99-151">This value is the serial number used to increment the log file name if <strong>FileMax</strong> is specified.</span></span> <span data-ttu-id="7eb99-152">Si la valeur n’est pas valide, 1 est utilisé.</span><span class="sxs-lookup"><span data-stu-id="7eb99-152">If the value is not valid, 1 will be assumed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb99-153"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-153"><strong>FileName</strong></span></span></td>
<td><span data-ttu-id="7eb99-154"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-154"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="7eb99-155">Chemin d’accès complet du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="7eb99-155">The fully qualified path of the log file.</span></span> <span data-ttu-id="7eb99-156">Le chemin d’accès à ce fichier doit exister.</span><span class="sxs-lookup"><span data-stu-id="7eb99-156">The path to this file must exist.</span></span> <span data-ttu-id="7eb99-157">Le fichier journal est un fichier journal séquentiel.</span><span class="sxs-lookup"><span data-stu-id="7eb99-157">The log file is a sequential log file.</span></span> <span data-ttu-id="7eb99-158">Le chemin d’accès est limité à 1024 caractères.</span><span class="sxs-lookup"><span data-stu-id="7eb99-158">The path is limited to 1024 characters.</span></span><br/> <span data-ttu-id="7eb99-159">Si <strong>filename</strong> n’est pas spécifié, les événements sont écrits dans%SystemRoot%\System32\LogFiles\WMI\ <sessionname> . etl.</span><span class="sxs-lookup"><span data-stu-id="7eb99-159">If <strong>FileName</strong> is not specified, events are written to %SystemRoot%\System32\LogFiles\WMI\<sessionname>.etl.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb99-160"><strong>FileMax</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-160"><strong>FileMax</strong></span></span></td>
<td><span data-ttu-id="7eb99-161"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-161"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-162">Nombre maximal d’instances du fichier journal créé par ETW.</span><span class="sxs-lookup"><span data-stu-id="7eb99-162">The maximum number of instances of the log file that ETW creates.</span></span> <span data-ttu-id="7eb99-163">Si le fichier journal spécifié dans <strong>filename</strong> existe, ETW ajoute la valeur <strong>FileCounter</strong> au nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="7eb99-163">If the log file specified in <strong>FileName</strong> exists, ETW appends the <strong>FileCounter</strong> value to the file name.</span></span> <span data-ttu-id="7eb99-164">Par exemple, si le nom du fichier journal par défaut est utilisé, le formulaire est%SystemRoot%\System32\LogFiles\WMI\ <sessionname> . etl. NNNN.</span><span class="sxs-lookup"><span data-stu-id="7eb99-164">For example, if the default log file name is used, the form is %SystemRoot%\System32\LogFiles\WMI\<sessionname>.etl.NNNN.</span></span> <br/> <span data-ttu-id="7eb99-165">La première fois que l’ordinateur est démarré, le nom de fichier est <sessionname> . etl. 0001, la deuxième fois, le nom de fichier est <sessionname> . etl. 0002, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="7eb99-165">The first time the computer is started, the file name is <sessionname>.etl.0001, the second time the file name is <sessionname>.etl.0002, and so on.</span></span> <span data-ttu-id="7eb99-166">Si <strong>FileMax</strong> a la valeur 3, au quatrième redémarrage de l’ordinateur, ETW rétablit la valeur 1 pour le compteur et remplace <sessionname> . etl. 0001, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="7eb99-166">If <strong>FileMax</strong> is 3, on the fourth restart of the computer, ETW resets the counter to 1 and overwrites <sessionname>.etl.0001, if it exists.</span></span><br/> <span data-ttu-id="7eb99-167">Le nombre maximal d’instances du fichier journal pris en charge est de 16.</span><span class="sxs-lookup"><span data-stu-id="7eb99-167">The maximum number of instances of the log file that are supported is 16.</span></span><br/> <span data-ttu-id="7eb99-168">N’utilisez pas cette fonctionnalité avec le mode de fichier journal <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> .</span><span class="sxs-lookup"><span data-stu-id="7eb99-168">Do not use this feature with the <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> log file mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb99-169"><strong>FlushTimer</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-169"><strong>FlushTimer</strong></span></span></td>
<td><span data-ttu-id="7eb99-170"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-170"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-171">Fréquence, en secondes, de vidage forcé des mémoires tampons de trace.</span><span class="sxs-lookup"><span data-stu-id="7eb99-171">How often, in seconds, the trace buffers are forcibly flushed.</span></span> <span data-ttu-id="7eb99-172">La durée de vidage minimale est de 1 seconde.</span><span class="sxs-lookup"><span data-stu-id="7eb99-172">The minimum flush time is 1 second.</span></span> <span data-ttu-id="7eb99-173">Ce vidage forcé s’ajoute au vidage automatique qui se produit lorsqu’une mémoire tampon est saturée et lorsque la session de trace s’arrête.</span><span class="sxs-lookup"><span data-stu-id="7eb99-173">This forced flush is in addition to the automatic flush that occurs when a buffer is full and when the trace session stops.</span></span> <br/> <span data-ttu-id="7eb99-174">Dans le cas d’un enregistreur d’événements en temps réel, la valeur zéro (valeur par défaut) signifie que le temps de vidage sera défini sur 1 seconde.</span><span class="sxs-lookup"><span data-stu-id="7eb99-174">For the case of a real-time logger, a value of zero (the default value) means that the flush time will be set to 1 second.</span></span> <span data-ttu-id="7eb99-175">Un enregistreur d’événements en temps réel est lorsque <strong>LogFileMode</strong> a la valeur <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="7eb99-175">A real-time logger is when <strong>LogFileMode</strong> is set to <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="7eb99-176">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="7eb99-176">The default value is 0.</span></span> <span data-ttu-id="7eb99-177">Par défaut, les mémoires tampons sont vidées uniquement lorsqu’elles sont pleines.</span><span class="sxs-lookup"><span data-stu-id="7eb99-177">By default, buffers are flushed only when they are full.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb99-178"><strong>Uniques</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-178"><strong>Guid</strong></span></span></td>
<td><span data-ttu-id="7eb99-179"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-179"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="7eb99-180">Chaîne qui contient un GUID qui identifie de façon unique la session.</span><span class="sxs-lookup"><span data-stu-id="7eb99-180">A string that contains a GUID that uniquely identifies the session.</span></span> <span data-ttu-id="7eb99-181">Cette valeur est requise.</span><span class="sxs-lookup"><span data-stu-id="7eb99-181">This value is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb99-182"><strong>LogFileMode</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-182"><strong>LogFileMode</strong></span></span></td>
<td><span data-ttu-id="7eb99-183"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-183"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-184">Spécifiez un ou plusieurs modes de journal.</span><span class="sxs-lookup"><span data-stu-id="7eb99-184">Specify one or more log modes.</span></span> <span data-ttu-id="7eb99-185">Pour connaître les valeurs possibles, consultez <a href="logging-mode-constants.md">constantes de mode de journalisation</a>.</span><span class="sxs-lookup"><span data-stu-id="7eb99-185">For possible values, see <a href="logging-mode-constants.md">Logging Mode Constants</a>.</span></span> <span data-ttu-id="7eb99-186">La valeur par défaut est <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="7eb99-186">The default is <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span></span> <span data-ttu-id="7eb99-187">Au lieu d’écrire dans un fichier journal, vous pouvez spécifier <strong>EVENT_TRACE_BUFFERING_MODE</strong> ou <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="7eb99-187">Instead of writing to a log file, you can specify either <strong>EVENT_TRACE_BUFFERING_MODE</strong> or <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="7eb99-188">La spécification de <strong>EVENT_TRACE_BUFFERING_MODE</strong> permet d’éviter le coût de vidage du contenu de la session sur le disque lorsque le système de fichiers devient disponible.</span><span class="sxs-lookup"><span data-stu-id="7eb99-188">Specifying <strong>EVENT_TRACE_BUFFERING_MODE</strong> avoids the cost of flushing the contents of the session to disk when the file system becomes available.</span></span> <br/> <span data-ttu-id="7eb99-189">Notez que l’utilisation de <strong>EVENT_TRACE_BUFFERING_MODE</strong> amène le système à ignorer la valeur <strong>MaximumBuffers</strong> , car la taille de la mémoire tampon est à la place le produit de <strong>MinimumBuffers</strong> et <strong>bufferSize</strong>.</span><span class="sxs-lookup"><span data-stu-id="7eb99-189">Note that using <strong>EVENT_TRACE_BUFFERING_MODE</strong> will cause the system to ignore the <strong>MaximumBuffers</strong> value, as the buffer size is instead the product of <strong>MinimumBuffers</strong> and <strong>BufferSize</strong>.</span></span><br/> <span data-ttu-id="7eb99-190">Les sessions de journal automatique ne prennent pas en charge le mode de journalisation <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> .</span><span class="sxs-lookup"><span data-stu-id="7eb99-190">AutoLogger sessions do not support the <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> logging mode.</span></span><br/> <span data-ttu-id="7eb99-191">Si <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> est spécifié, <strong>bufferSize</strong> doit être fourni explicitement et doit être le même dans l’enregistreur d’événements et le fichier ajouté.</span><span class="sxs-lookup"><span data-stu-id="7eb99-191">If <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> is specified, <strong>BufferSize</strong> must be explicitly provided and must be the same in both the logger and the file being appended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb99-192"><strong>MaxFileSize</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-192"><strong>MaxFileSize</strong></span></span></td>
<td><span data-ttu-id="7eb99-193"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-193"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-194">Taille maximale du fichier journal, en mégaoctets.</span><span class="sxs-lookup"><span data-stu-id="7eb99-194">The maximum file size of the log file, in megabytes.</span></span> <span data-ttu-id="7eb99-195">La session est fermée lorsque la taille maximale est atteinte, sauf si vous êtes en mode de fichier journal circulaire.</span><span class="sxs-lookup"><span data-stu-id="7eb99-195">The session is closed when the maximum size is reached, unless you are in circular log file mode.</span></span> <span data-ttu-id="7eb99-196">Pour ne spécifier aucune limite, définissez la valeur sur 0.</span><span class="sxs-lookup"><span data-stu-id="7eb99-196">To specify no limit, set value to 0.</span></span> <span data-ttu-id="7eb99-197">La valeur par défaut est 100 Mo, si elle n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="7eb99-197">The default is 100 MB, if not set.</span></span> <span data-ttu-id="7eb99-198">Le comportement qui se produit lorsque la taille de fichier maximale est atteinte dépend de la valeur de <strong>LogFileMode</strong>.</span><span class="sxs-lookup"><span data-stu-id="7eb99-198">The behavior that occurs when the maximum file size is reached depends on the value of <strong>LogFileMode</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb99-199"><strong>MaximumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-199"><strong>MaximumBuffers</strong></span></span></td>
<td><span data-ttu-id="7eb99-200"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-200"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-201">Nombre maximal de mémoires tampons à allouer.</span><span class="sxs-lookup"><span data-stu-id="7eb99-201">The maximum number of buffers to allocate.</span></span> <span data-ttu-id="7eb99-202">En général, cette valeur est le nombre minimal de mémoires tampons plus vingt.</span><span class="sxs-lookup"><span data-stu-id="7eb99-202">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="7eb99-203">ETW utilise la taille de la mémoire tampon et la taille de la mémoire physique pour calculer cette valeur.</span><span class="sxs-lookup"><span data-stu-id="7eb99-203">ETW uses the buffer size and the size of physical memory to calculate this value.</span></span> <span data-ttu-id="7eb99-204">Cette valeur doit être supérieure ou égale à la valeur de <strong>MinimumBuffers</strong>.</span><span class="sxs-lookup"><span data-stu-id="7eb99-204">This value must be greater than or equal to the value for <strong>MinimumBuffers</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb99-205"><strong>MinimumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-205"><strong>MinimumBuffers</strong></span></span></td>
<td><span data-ttu-id="7eb99-206"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-206"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-207">Nombre minimal de mémoires tampons à allouer au démarrage.</span><span class="sxs-lookup"><span data-stu-id="7eb99-207">The minimum number of buffers to allocate at startup.</span></span> <span data-ttu-id="7eb99-208">Le nombre minimal de mémoires tampons que vous pouvez spécifier est deux mémoires tampons par processeur.</span><span class="sxs-lookup"><span data-stu-id="7eb99-208">The minimum number of buffers that you can specify is two buffers per processor.</span></span> <span data-ttu-id="7eb99-209">Par exemple, sur un ordinateur à processeur unique, le nombre minimal de mémoires tampons est de deux.</span><span class="sxs-lookup"><span data-stu-id="7eb99-209">For example, on a single processor computer, the minimum number of buffers is two.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb99-210"><strong>Start</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-210"><strong>Start</strong></span></span></td>
<td><span data-ttu-id="7eb99-211"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-211"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-212">Pour que la session de journalisation automatique démarre lors du prochain redémarrage de l’ordinateur, définissez cette valeur sur 1 ; dans le cas contraire, définissez cette valeur sur 0.</span><span class="sxs-lookup"><span data-stu-id="7eb99-212">To have the AutoLogger session start the next time the computer is restarted, set this value to 1; otherwise, set this value to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb99-213"><strong>État</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-213"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="7eb99-214"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-214"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-215">État de démarrage de l’enregistreur automatique.</span><span class="sxs-lookup"><span data-stu-id="7eb99-215">The startup status of the AutoLogger.</span></span> <span data-ttu-id="7eb99-216">Si le journal automatique n’a pas pu démarrer, la valeur de cette clé est le code d’erreur Win32 approprié.</span><span class="sxs-lookup"><span data-stu-id="7eb99-216">If the AutoLogger failed to start, the value of this key is the appropriate Win32 error code.</span></span> <span data-ttu-id="7eb99-217">Si le journal automatique a démarré, la valeur de cette clé est <strong>ERROR_SUCCESS</strong> (0).</span><span class="sxs-lookup"><span data-stu-id="7eb99-217">If the AutoLogger successfully started, the value of this key is <strong>ERROR_SUCCESS</strong> (0).</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7eb99-218">Le tableau suivant décrit les valeurs que vous pouvez définir pour chaque fournisseur que vous souhaitez activer pour votre session.</span><span class="sxs-lookup"><span data-stu-id="7eb99-218">The following table describes the values that you can define for each provider that you want to enable to your session.</span></span> <span data-ttu-id="7eb99-219">Vous devez disposer de privilèges d’administrateur pour spécifier ces valeurs de registre.</span><span class="sxs-lookup"><span data-stu-id="7eb99-219">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="7eb99-220">Si vous spécifiez une valeur que ETW ne peut pas prendre en charge, ETW remplace la valeur.</span><span class="sxs-lookup"><span data-stu-id="7eb99-220">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7eb99-221">Valeur</span><span class="sxs-lookup"><span data-stu-id="7eb99-221">Value</span></span></th>
<th><span data-ttu-id="7eb99-222">Type</span><span class="sxs-lookup"><span data-stu-id="7eb99-222">Type</span></span></th>
<th><span data-ttu-id="7eb99-223">Description</span><span class="sxs-lookup"><span data-stu-id="7eb99-223">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7eb99-224"><strong>Activé</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-224"><strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="7eb99-225"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-225"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-226">Détermine si le fournisseur est activé.</span><span class="sxs-lookup"><span data-stu-id="7eb99-226">Determines if the provider is enabled.</span></span> <span data-ttu-id="7eb99-227">Pour activer le fournisseur, définissez cette valeur sur 1.</span><span class="sxs-lookup"><span data-stu-id="7eb99-227">To enable the provider, set this value to 1.</span></span> <span data-ttu-id="7eb99-228">Pour désactiver le fournisseur, définissez cette valeur sur 0.</span><span class="sxs-lookup"><span data-stu-id="7eb99-228">To disable the provider, set this value to 0.</span></span> <span data-ttu-id="7eb99-229">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="7eb99-229">The default is 0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb99-230"><strong>EnableFlags</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-230"><strong>EnableFlags</strong></span></span></td>
<td><span data-ttu-id="7eb99-231"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-231"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-232">Valeur définie par le fournisseur qui spécifie la classe des événements pour lesquels le fournisseur génère des événements.</span><span class="sxs-lookup"><span data-stu-id="7eb99-232">Provider-defined value that specifies the class of events for which the provider generates events.</span></span> <span data-ttu-id="7eb99-233">Pour plus d’informations, consultez le paramètre <em>EnableFlags</em> de la fonction <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb99-233">For details, see the <em>EnableFlags</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> function.</span></span> <span data-ttu-id="7eb99-234">Spécifiez ce nom de valeur si le fournisseur ne prend pas en charge <strong>MatchAnyKeyword</strong> ou <strong>MatchAllKeyword</strong>.</span><span class="sxs-lookup"><span data-stu-id="7eb99-234">Specify this value name if the provider does not support <strong>MatchAnyKeyword</strong> or <strong>MatchAllKeyword</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb99-235"><strong>EnableLevel</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-235"><strong>EnableLevel</strong></span></span></td>
<td><span data-ttu-id="7eb99-236"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-236"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-237">Valeur définie par le fournisseur qui spécifie le niveau de détail inclus dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="7eb99-237">Provider-defined value that specifies the level of detail included in the event.</span></span> <span data-ttu-id="7eb99-238">Par exemple, vous pouvez utiliser cette valeur pour indiquer le niveau de gravité des événements générés par le fournisseur (informations, avertissement, erreur).</span><span class="sxs-lookup"><span data-stu-id="7eb99-238">For example, you can use this value to indicate the severity level of the events (informational, warning, error) that the provider generates.</span></span> <span data-ttu-id="7eb99-239">Pour obtenir la liste des niveaux prédéfinis, consultez le paramètre <em>Level</em> de la fonction <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb99-239">For a list of predefined levels, see the <em>level</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb99-240"><strong>EnableProperty</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-240"><strong>EnableProperty</strong></span></span></td>
<td><span data-ttu-id="7eb99-241"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-241"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-242">Utilisez cette valeur pour inclure un ou plusieurs des éléments suivants dans le fichier journal :</span><span class="sxs-lookup"><span data-stu-id="7eb99-242">Use this value to include one or more of the following items in the log file:</span></span>
<ul>
<li><span data-ttu-id="7eb99-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = inclure dans les données étendues l’identificateur de sécurité (SID) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7eb99-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Include in the extended data the security identifier (SID) of the user.</span></span></li>
<li><span data-ttu-id="7eb99-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = include dans les données étendues identificateur de session Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="7eb99-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Include in the extended data the terminal session identifier.</span></span></li>
<li><span data-ttu-id="7eb99-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = inclure dans les données étendues trace de la pile des appels pour les événements écrits à l’aide de <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7eb99-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Include in the extended data a call stack trace for events written using <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span></span></li>
<li><span data-ttu-id="7eb99-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = filtre tous les événements qui n’ont pas de mot clé non nul spécifié.</span><span class="sxs-lookup"><span data-stu-id="7eb99-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filters out all events that do not have a non-zero keyword specified.</span></span></li>
<li><span data-ttu-id="7eb99-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = indique que cet appel à <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> doit activer un <a href="provider-traits.md">groupe de fournisseurs</a> plutôt qu’un fournisseur d’événements individuel.</span><span class="sxs-lookup"><span data-stu-id="7eb99-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Indicates that this call to <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> should enable a <a href="provider-traits.md">Provider Group</a> rather than an individual Event Provider.</span></span></li>
<li><span data-ttu-id="7eb99-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = inclure la clé de début du processus dans les données étendues.</span><span class="sxs-lookup"><span data-stu-id="7eb99-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Include the Process Start Key in the extended data.</span></span></li>
<li><span data-ttu-id="7eb99-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = inclure la clé d’événement dans les données étendues.</span><span class="sxs-lookup"><span data-stu-id="7eb99-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Include the Event Key in the extended data.</span></span></li>
<li><span data-ttu-id="7eb99-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = filtre tous les événements qui sont marqués comme un événement non privé ou qui proviennent d’un processus qui est marqué comme non privé.</span><span class="sxs-lookup"><span data-stu-id="7eb99-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filters out all events that are either marked as an InPrivate event or come from a process that is marked as InPrivate.</span></span></li>
</ul>
<span data-ttu-id="7eb99-251">Pour plus d’informations sur ces éléments, consultez le <strong>EnableProperty</strong> de la structure <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb99-251">For more information about these items, see the <strong>EnableProperty</strong> of the <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7eb99-252"><strong>MatchAnyKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-252"><strong>MatchAnyKeyword</strong></span></span></td>
<td><span data-ttu-id="7eb99-253"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-253"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-254">Masque de réécriture des mots clés qui déterminent la catégorie d’événements que le fournisseur doit écrire.</span><span class="sxs-lookup"><span data-stu-id="7eb99-254">Bitmask of keywords that determine the category of events that you want the provider to write.</span></span> <span data-ttu-id="7eb99-255">Le fournisseur écrit l’événement si l’un des bits de mot clé de l’événement correspond à l’un des bits définis dans ce masque.</span><span class="sxs-lookup"><span data-stu-id="7eb99-255">The provider writes the event if any of the event's keyword bits match any of the bits set in this mask.</span></span> <span data-ttu-id="7eb99-256">Pour spécifier que le fournisseur doit écrire tous les événements, définissez cette valeur sur zéro.</span><span class="sxs-lookup"><span data-stu-id="7eb99-256">To specify that the provider write all events, set this value to zero.</span></span> <span data-ttu-id="7eb99-257">Pour obtenir un exemple, consultez la section Notes de la fonction <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb99-257">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7eb99-258"><strong>MatchAllKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-258"><strong>MatchAllKeyword</strong></span></span></td>
<td><span data-ttu-id="7eb99-259"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="7eb99-259"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="7eb99-260">Ce masque de masque est facultatif.</span><span class="sxs-lookup"><span data-stu-id="7eb99-260">This bitmask is optional.</span></span> <span data-ttu-id="7eb99-261">Ce masque limite davantage la catégorie d’événements que vous souhaitez que le fournisseur écrive.</span><span class="sxs-lookup"><span data-stu-id="7eb99-261">This mask further restricts the category of events that you want the provider to write.</span></span> <span data-ttu-id="7eb99-262">Si le mot clé de l’événement répond à la condition <em>MatchAnyKeyword</em> , le fournisseur écrit l’événement uniquement si tous les bits de ce masque existent dans le mot clé de l’événement.</span><span class="sxs-lookup"><span data-stu-id="7eb99-262">If the event's keyword meets the <em>MatchAnyKeyword</em> condition, the provider will write the event only if all of the bits in this mask exist in the event's keyword.</span></span> <span data-ttu-id="7eb99-263">Ce masque n’est pas utilisé si <em>MatchAnyKeyword</em> est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7eb99-263">This mask is not used if <em>MatchAnyKeyword</em> is zero.</span></span> <span data-ttu-id="7eb99-264">Pour obtenir un exemple, consultez la section Notes de la fonction <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7eb99-264">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7eb99-265">Une fois le registre modifié, la session de journalisation automatique est lancée lors du prochain redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7eb99-265">After the registry has been modified, the AutoLogger session is started the next time the computer is restarted.</span></span> <span data-ttu-id="7eb99-266">La session de journalisation automatique appelle la fonction [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) pour activer les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="7eb99-266">The AutoLogger session calls the [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) function to enable the providers.</span></span>

<span data-ttu-id="7eb99-267">Les sessions de l’enregistreur d’événements automatique augmentent le temps de démarrage du système et doivent être utilisées avec modération.</span><span class="sxs-lookup"><span data-stu-id="7eb99-267">The AutoLogger sessions increase the system boot time and should be used sparingly.</span></span> <span data-ttu-id="7eb99-268">Les services qui souhaitent capturer des informations pendant le processus de démarrage doivent envisager d’ajouter la logique du contrôleur à lui-même au lieu d’utiliser la session de journalisation automatique.</span><span class="sxs-lookup"><span data-stu-id="7eb99-268">Services that want to capture information during the boot process should consider adding controller logic to itself instead of using the AutoLogger session.</span></span>

<span data-ttu-id="7eb99-269">Pour arrêter une session de journalisation automatique, appelez la fonction [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) .</span><span class="sxs-lookup"><span data-stu-id="7eb99-269">To stop an AutoLogger session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function.</span></span> <span data-ttu-id="7eb99-270">Le nom de session que vous transmettez à la fonction est le nom de la clé de registre que vous avez utilisée pour définir la session dans le registre.</span><span class="sxs-lookup"><span data-stu-id="7eb99-270">The session name that you pass to the function is the name of the registry key that you used to define the session in the registry.</span></span>

<span data-ttu-id="7eb99-271">Sur Windows 8.1, Windows Server 2012 R2 et versions ultérieures, la charge utile d’événement, la portée et les filtres de parcours de pile peuvent être utilisés par la fonction [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) et les structures de [**\_ \_ descripteur de filtre d’événement**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) et de [**\_ \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) pour filtrer sur des conditions spécifiques dans une session de journalisation.</span><span class="sxs-lookup"><span data-stu-id="7eb99-271">On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="7eb99-272">Pour plus d’informations sur les filtres de charge utile d’événement, consultez les fonctions [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)et [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , ainsi que les structures de prédicat **activer les \_ \_ paramètres de trace**, **\_ \_ descripteur de filtre d’événement** et de [**\_ filtre \_ de charge utile**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) .</span><span class="sxs-lookup"><span data-stu-id="7eb99-272">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="7eb99-273">Pour plus d’informations sur le démarrage d’une session de suivi d’événements, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="7eb99-273">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="7eb99-274">Pour plus d’informations sur le démarrage d’une session privée de journalisation, consultez [configuration et démarrage d’une session de journalisation privée](configuring-and-starting-a-private-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="7eb99-274">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="7eb99-275">Pour plus d’informations sur le démarrage d’une session de journal de noyau NT, consultez [configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="7eb99-275">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eb99-276">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7eb99-276">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eb99-277">Configuration et démarrage d’une session de journalisation privée</span><span class="sxs-lookup"><span data-stu-id="7eb99-277">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="7eb99-278">Configuration et démarrage d’une session SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="7eb99-278">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="7eb99-279">Configuration et démarrage d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="7eb99-279">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="7eb99-280">Configuration et démarrage de la session de journalisation du noyau NT</span><span class="sxs-lookup"><span data-stu-id="7eb99-280">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="7eb99-281">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="7eb99-281">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="7eb99-282">**ACTIVER \_ les \_ paramètres de trace**</span><span class="sxs-lookup"><span data-stu-id="7eb99-282">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="7eb99-283">**descripteur de filtre d’événements \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7eb99-283">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="7eb99-284">**\_prédicat de filtre de charge utile \_**</span><span class="sxs-lookup"><span data-stu-id="7eb99-284">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="7eb99-285">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="7eb99-285">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="7eb99-286">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="7eb99-286">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="7eb99-287">Mise à jour d’une session de suivi d’événements</span><span class="sxs-lookup"><span data-stu-id="7eb99-287">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>
