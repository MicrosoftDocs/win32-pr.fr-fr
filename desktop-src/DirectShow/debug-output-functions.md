---
description: Fonctions de sortie de débogage
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Fonctions de sortie de débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87470b44717bb76c1a029bd885bb9149a4636b5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544562"
---
# <a name="debug-output-functions"></a><span data-ttu-id="35e12-103">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="35e12-103">Debug Output Functions</span></span>

<span data-ttu-id="35e12-104">Les [classes de base DirectShow](directshow-base-classes.md) fournissent plusieurs macros pour l’affichage des informations de débogage.</span><span class="sxs-lookup"><span data-stu-id="35e12-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros for displaying debugging information.</span></span>



| <span data-ttu-id="35e12-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="35e12-105">Function</span></span>                                               | <span data-ttu-id="35e12-106">Description</span><span class="sxs-lookup"><span data-stu-id="35e12-106">Description</span></span>                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35e12-107">**DbgCheckModuleLevel**</span><span class="sxs-lookup"><span data-stu-id="35e12-107">**DbgCheckModuleLevel**</span></span>](dbgcheckmodulelevel.md)     | <span data-ttu-id="35e12-108">Vérifie si la journalisation est activée pour les types de messages et le niveau donnés.</span><span class="sxs-lookup"><span data-stu-id="35e12-108">Checks whether logging is enabled for the given message types and level.</span></span>                             |
| [<span data-ttu-id="35e12-109">**DbgDumpObjectRegister**</span><span class="sxs-lookup"><span data-stu-id="35e12-109">**DbgDumpObjectRegister**</span></span>](dbgdumpobjectregister.md) | <span data-ttu-id="35e12-110">Affiche des informations sur les objets actifs.</span><span class="sxs-lookup"><span data-stu-id="35e12-110">Displays information about active objects.</span></span>                                                           |
| [<span data-ttu-id="35e12-111">**DbgInitialise**</span><span class="sxs-lookup"><span data-stu-id="35e12-111">**DbgInitialise**</span></span>](dbginitialise.md)                 | <span data-ttu-id="35e12-112">Initialise la bibliothèque de débogage.</span><span class="sxs-lookup"><span data-stu-id="35e12-112">Initializes the debug library.</span></span>                                                                       |
| [<span data-ttu-id="35e12-113">**DbgLog**</span><span class="sxs-lookup"><span data-stu-id="35e12-113">**DbgLog**</span></span>](dbglog.md)                               | <span data-ttu-id="35e12-114">Envoie une chaîne à l’emplacement de sortie de débogage, si la journalisation est activée pour le type et le niveau spécifiés.</span><span class="sxs-lookup"><span data-stu-id="35e12-114">Sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> |
| [<span data-ttu-id="35e12-115">**DbgOutString**</span><span class="sxs-lookup"><span data-stu-id="35e12-115">**DbgOutString**</span></span>](dbgoutstring.md)                   | <span data-ttu-id="35e12-116">Envoie une chaîne à l’emplacement de sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="35e12-116">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="35e12-117">**DbgSetModuleLevel**</span><span class="sxs-lookup"><span data-stu-id="35e12-117">**DbgSetModuleLevel**</span></span>](dbgsetmodulelevel.md)         | <span data-ttu-id="35e12-118">Définit le niveau de journalisation pour un ou plusieurs types de messages.</span><span class="sxs-lookup"><span data-stu-id="35e12-118">Sets the logging level for one or more message types.</span></span>                                                |
| [<span data-ttu-id="35e12-119">**DbgTerminate**</span><span class="sxs-lookup"><span data-stu-id="35e12-119">**DbgTerminate**</span></span>](dbgterminate.md)                   | <span data-ttu-id="35e12-120">Nettoie la bibliothèque de débogage.</span><span class="sxs-lookup"><span data-stu-id="35e12-120">Cleans up the debug library.</span></span>                                                                         |
| [<span data-ttu-id="35e12-121">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="35e12-121">**DisplayType**</span></span>](displaytype.md)                     | <span data-ttu-id="35e12-122">Envoie des informations sur un type de média à l’emplacement de sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="35e12-122">Sends information about a media type to the debug output location.</span></span>                                   |
| [<span data-ttu-id="35e12-123">**DumpGraph**</span><span class="sxs-lookup"><span data-stu-id="35e12-123">**DumpGraph**</span></span>](dumpgraph.md)                         | <span data-ttu-id="35e12-124">Envoie des informations sur un graphique de filtre à l’emplacement de sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="35e12-124">Sends information about a filter graph to the debug output location.</span></span>                                 |
| [<span data-ttu-id="35e12-125">**GuidNames**</span><span class="sxs-lookup"><span data-stu-id="35e12-125">**GuidNames**</span></span>](guidnames.md)                         | <span data-ttu-id="35e12-126">Tableau global qui contient des chaînes représentant les GUID définis dans UUID. h.</span><span class="sxs-lookup"><span data-stu-id="35e12-126">Global array that contains strings representing the GUIDs defined in Uuids.h.</span></span>                        |
| [<span data-ttu-id="35e12-127">**NOMME**</span><span class="sxs-lookup"><span data-stu-id="35e12-127">**NAME**</span></span>](name.md)                                   | <span data-ttu-id="35e12-128">Génère une chaîne de débogage uniquement.</span><span class="sxs-lookup"><span data-stu-id="35e12-128">Generates a debug-only string.</span></span>                                                                       |
| [<span data-ttu-id="35e12-129">**OBSERVE**</span><span class="sxs-lookup"><span data-stu-id="35e12-129">**NOTE**</span></span>](note.md)                                   | <span data-ttu-id="35e12-130">Envoie une chaîne à l’emplacement de sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="35e12-130">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="35e12-131">**AVERTI**</span><span class="sxs-lookup"><span data-stu-id="35e12-131">**REMIND**</span></span>](remind.md)                               | <span data-ttu-id="35e12-132">Génère un rappel au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="35e12-132">Generates a reminder at compile time.</span></span>                                                                |



 

<span data-ttu-id="35e12-133">**Clés de Registre**</span><span class="sxs-lookup"><span data-stu-id="35e12-133">**Registry Keys**</span></span>

<span data-ttu-id="35e12-134">La fonction de sortie de débogage dans DirectShow utilise un ensemble de clés de registre.</span><span class="sxs-lookup"><span data-stu-id="35e12-134">The debug output function in DirectShow use a set of registry keys.</span></span> <span data-ttu-id="35e12-135">L’emplacement de ces clés de Registre dépend de la version de Windows.</span><span class="sxs-lookup"><span data-stu-id="35e12-135">The location of these registry keys depends on the version of Windows.</span></span>

<span data-ttu-id="35e12-136">*Avant Windows Vista*, les clés de débogage se trouvent sous le chemin d’accès suivant :</span><span class="sxs-lookup"><span data-stu-id="35e12-136">*Prior to Windows Vista*, the debugging keys are located under the following path:</span></span>

<span data-ttu-id="35e12-137">**HKEY \_ \_** Débogage \\ **logiciel** \\  de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="35e12-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Debug**</span></span>

<span data-ttu-id="35e12-138">Dans Windows Vista ou version ultérieure, ils se trouvent sous le chemin d’accès suivant :</span><span class="sxs-lookup"><span data-stu-id="35e12-138">In Windows Vista or later, they are located under the following path:</span></span>

<span data-ttu-id="35e12-139">**HKEY \_ \_** Débogage \\  \\ **Microsoft** \\ **DirectShow** \\  du logiciel de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="35e12-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**DirectShow**\\**Debug**</span></span>

<span data-ttu-id="35e12-140">Pour les filtres tiers, l’emplacement dépend de la version des classes de [base DirectShow](directshow-base-classes.md) qui a été utilisée pour générer le filtre.</span><span class="sxs-lookup"><span data-stu-id="35e12-140">For third-party filters, the location depends on which version of the [DirectShow Base Classes](directshow-base-classes.md) was used to build the filter.</span></span> <span data-ttu-id="35e12-141">La version incluse dans le SDK Windows pour Windows Vista utilise le chemin d’accès le plus récent.</span><span class="sxs-lookup"><span data-stu-id="35e12-141">The version included in the Windows SDK for Windows Vista uses the newer path.</span></span> <span data-ttu-id="35e12-142">Les versions précédentes utilisaient l’ancien chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="35e12-142">Previous versions used the older path.</span></span>

<span data-ttu-id="35e12-143">Dans les notes qui suivent, l’étiquette *<DebugRoot>* est utilisée pour indiquer ces deux chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="35e12-143">In the remarks that follow, the label *<DebugRoot>* is used to indicate these two paths.</span></span> <span data-ttu-id="35e12-144">Remplacez le chemin d’accès correct, selon la version de Windows ou la version des classes de base.</span><span class="sxs-lookup"><span data-stu-id="35e12-144">Substitute the correct path, depending on the version of Windows or the version of the base classes.</span></span>

<span data-ttu-id="35e12-145">**Journalisation du débogage**</span><span class="sxs-lookup"><span data-stu-id="35e12-145">**Debug Logging**</span></span>

<span data-ttu-id="35e12-146">DirectShow définit plusieurs types de messages, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="35e12-146">DirectShow defines several message types, shown in the following table.</span></span>



| <span data-ttu-id="35e12-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="35e12-147">Value</span></span>                   | <span data-ttu-id="35e12-148">Description</span><span class="sxs-lookup"><span data-stu-id="35e12-148">Description</span></span>                                             |
|-------------------------|---------------------------------------------------------|
| <span data-ttu-id="35e12-149">erreur de journal \_</span><span class="sxs-lookup"><span data-stu-id="35e12-149">LOG\_ERROR</span></span>              | <span data-ttu-id="35e12-150">Notification d’erreur.</span><span class="sxs-lookup"><span data-stu-id="35e12-150">Error notification.</span></span>                                     |
| <span data-ttu-id="35e12-151">verrouillage du journal \_</span><span class="sxs-lookup"><span data-stu-id="35e12-151">LOG\_LOCKING</span></span>            | <span data-ttu-id="35e12-152">Verrouillage et déverrouillage des sections critiques.</span><span class="sxs-lookup"><span data-stu-id="35e12-152">Locking and unlocking of critical sections.</span></span>             |
| <span data-ttu-id="35e12-153">mémoire de JOURNALisation \_</span><span class="sxs-lookup"><span data-stu-id="35e12-153">LOG\_MEMORY</span></span>             | <span data-ttu-id="35e12-154">Allocation de mémoire, et création et destruction d’objets.</span><span class="sxs-lookup"><span data-stu-id="35e12-154">Memory allocation, and object creation and destruction.</span></span> |
| <span data-ttu-id="35e12-155">synchronisation du journal \_</span><span class="sxs-lookup"><span data-stu-id="35e12-155">LOG\_TIMING</span></span>             | <span data-ttu-id="35e12-156">Mesures de minutage et de performances.</span><span class="sxs-lookup"><span data-stu-id="35e12-156">Timing and performance measurements.</span></span>                    |
| <span data-ttu-id="35e12-157">suivi du journal \_</span><span class="sxs-lookup"><span data-stu-id="35e12-157">LOG\_TRACE</span></span>              | <span data-ttu-id="35e12-158">Suivi des appels généraux.</span><span class="sxs-lookup"><span data-stu-id="35e12-158">General call tracing.</span></span>                                   |
| <span data-ttu-id="35e12-159">CUSTOM1 à CUSTOM5</span><span class="sxs-lookup"><span data-stu-id="35e12-159">CUSTOM1 through CUSTOM5</span></span> | <span data-ttu-id="35e12-160">Disponible pour les messages de débogage personnalisés</span><span class="sxs-lookup"><span data-stu-id="35e12-160">Available for custom debug messages</span></span>                     |



 

<span data-ttu-id="35e12-161">Chacune des fonctions de journalisation de débogage DirectShow spécifie un type de message et un niveau de journal.</span><span class="sxs-lookup"><span data-stu-id="35e12-161">Each of the DirectShow debug logging functions specifies a message type and a log level.</span></span> <span data-ttu-id="35e12-162">Le message de débogage s’affiche uniquement lorsque le niveau de débogage actuel de ce type de message est supérieur ou égal au niveau spécifié dans la fonction de journalisation.</span><span class="sxs-lookup"><span data-stu-id="35e12-162">The debug message is displayed only when the current debugging level for that message type is equal to or greater than the level specified in the logging function.</span></span> <span data-ttu-id="35e12-163">Dans le cas contraire, le message est ignoré.</span><span class="sxs-lookup"><span data-stu-id="35e12-163">Otherwise, the message is ignored.</span></span>

<span data-ttu-id="35e12-164">Par exemple, le code suivant génère la chaîne « This is a Debug message » si le niveau de trace du journal \_ est supérieur ou égal à 3 :</span><span class="sxs-lookup"><span data-stu-id="35e12-164">For example, the following code outputs the string "This is a debug message" if the LOG\_TRACE level is 3 or higher:</span></span>

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

<span data-ttu-id="35e12-165">Chaque module peut définir son propre niveau de débogage pour chaque type de message.</span><span class="sxs-lookup"><span data-stu-id="35e12-165">Every module can set its own debugging level for each message type.</span></span> <span data-ttu-id="35e12-166">(Un *module* est une dll ou un fichier exécutable qui peut être chargé à l’aide de la fonction **LoadLibrary** .) Les niveaux de débogage d’un module s’affichent dans le Registre sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="35e12-166">(A *module* is a DLL or executable that can be loaded using the **LoadLibrary** function.) A module's debugging levels appear in the registry under the following key:</span></span>

<span data-ttu-id="35e12-167">**HKEY \_ local \_ machine**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span><span class="sxs-lookup"><span data-stu-id="35e12-167">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span></span>

<span data-ttu-id="35e12-168">où *<Message Type>* est le type de message moins le « journal \_ » initial, par exemple, le **verrouillage** des messages de verrouillage des journaux \_ .</span><span class="sxs-lookup"><span data-stu-id="35e12-168">where *<Message Type>* is the message type minus the initial "LOG\_"; for example, **LOCKING** for LOG\_LOCKING messages.</span></span> <span data-ttu-id="35e12-169">Quand un module est chargé, la bibliothèque de débogage recherche les niveaux de journalisation du module dans le registre.</span><span class="sxs-lookup"><span data-stu-id="35e12-169">When a module is loaded, the debug library finds the module's logging levels in the registry.</span></span> <span data-ttu-id="35e12-170">Si les clés de Registre n’existent pas, la bibliothèque de débogage les crée.</span><span class="sxs-lookup"><span data-stu-id="35e12-170">If the registry keys do not exist, the debug library creates them.</span></span>

<span data-ttu-id="35e12-171">Un module peut également définir ses propres niveaux au moment de l’exécution, à l’aide de la fonction [**DbgSetModuleLevel**](dbgsetmodulelevel.md) .</span><span class="sxs-lookup"><span data-stu-id="35e12-171">A module can also set its own levels at run time, using the [**DbgSetModuleLevel**](dbgsetmodulelevel.md) function.</span></span> <span data-ttu-id="35e12-172">Pour envoyer un message à la sortie de débogage, appelez la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="35e12-172">To send a message to the debug output, call the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="35e12-173">L’exemple suivant crée un message de niveau 3 de type \_ trace du journal :</span><span class="sxs-lookup"><span data-stu-id="35e12-173">The following example creates a level 3 message of type LOG\_TRACE:</span></span>

<span data-ttu-id="35e12-174">Vous pouvez également spécifier des niveaux de journalisation globale, avec la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="35e12-174">You can also specify global logging levels, with the following registry key:</span></span>


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



<span data-ttu-id="35e12-175">La bibliothèque de débogage utilise le niveau le plus élevé, le niveau global ou le niveau du module.</span><span class="sxs-lookup"><span data-stu-id="35e12-175">The debug library uses whichever level is greater, the global level or the module level.</span></span>

<span data-ttu-id="35e12-176">**Emplacement de sortie de débogage**</span><span class="sxs-lookup"><span data-stu-id="35e12-176">**Debug Output Location**</span></span>

<span data-ttu-id="35e12-177">L’emplacement de sortie de débogage est déterminé par une autre clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="35e12-177">The debug output location is determined by another registry key:</span></span>

<span data-ttu-id="35e12-178">**HKEY \_ \_** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **LogToFile** de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="35e12-178">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<Modile Name>**\\**LogToFile**</span></span>

<span data-ttu-id="35e12-179">Si la valeur de cette clé est `Console` , la sortie est envoyée à la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="35e12-179">If the value of this key is `Console`, the output goes to the console window.</span></span> <span data-ttu-id="35e12-180">Si la valeur est `Deb` , `Debug` , `Debugger` ou une chaîne vide, la sortie est envoyée à la fenêtre du débogueur.</span><span class="sxs-lookup"><span data-stu-id="35e12-180">If the value is `Deb`, `Debug`, `Debugger`, or an empty string, the output goes to the debugger window.</span></span> <span data-ttu-id="35e12-181">Dans le cas contraire, la sortie est écrite dans un fichier spécifié par la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="35e12-181">Otherwise, the output is written to a file specified by the registry key.</span></span>

<span data-ttu-id="35e12-182">Avant qu’un fichier exécutable n’utilise la bibliothèque de débogage DirectShow, il doit appeler la fonction [**DbgInitialise**](dbginitialise.md) .</span><span class="sxs-lookup"><span data-stu-id="35e12-182">Before an executable uses the DirectShow debug library, it must call the [**DbgInitialise**](dbginitialise.md) function.</span></span> <span data-ttu-id="35e12-183">Ensuite, il doit appeler la fonction [**DbgTerminate**](dbgterminate.md) .</span><span class="sxs-lookup"><span data-stu-id="35e12-183">Afterward, it must call the [**DbgTerminate**](dbgterminate.md) function.</span></span> <span data-ttu-id="35e12-184">Les dll n’ont pas besoin d’appeler ces fonctions, car le point d’entrée de la DLL (défini dans la bibliothèque de classes de base) les appelle automatiquement.</span><span class="sxs-lookup"><span data-stu-id="35e12-184">DLLs do not need to call these functions, because the DLL entry point (defined in the base class library) calls them automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35e12-185">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35e12-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35e12-186">Utilitaires de débogage</span><span class="sxs-lookup"><span data-stu-id="35e12-186">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



