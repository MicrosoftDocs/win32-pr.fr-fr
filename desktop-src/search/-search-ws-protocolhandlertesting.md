---
description: L’intégralité du test et du débogage de vos implémentations de gestionnaires de protocole consiste à comprendre comment les gestionnaires de protocole sont lancés.
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Débogage de gestionnaires de protocole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112399"
---
# <a name="debugging-protocol-handlers"></a><span data-ttu-id="6a536-103">Débogage de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="6a536-103">Debugging Protocol Handlers</span></span>

<span data-ttu-id="6a536-104">L’intégralité du test et du débogage de vos implémentations de gestionnaires de protocole consiste à comprendre comment les gestionnaires de protocole sont lancés.</span><span class="sxs-lookup"><span data-stu-id="6a536-104">Integral to testing and debugging your protocol handler implementations is understanding how protocol handlers are launched.</span></span>

<span data-ttu-id="6a536-105">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="6a536-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="6a536-106">À propos du débogage des gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="6a536-106">About Debugging Protocol Handlers</span></span>](#about-debugging-protocol-handlers)
-   [<span data-ttu-id="6a536-107">Configuration du débogage</span><span class="sxs-lookup"><span data-stu-id="6a536-107">Setting Up Debugging</span></span>](#setting-up-debugging)
-   [<span data-ttu-id="6a536-108">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6a536-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="6a536-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a536-109">Related topics</span></span>](#related-topics)

## <a name="about-debugging-protocol-handlers"></a><span data-ttu-id="6a536-110">À propos du débogage des gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="6a536-110">About Debugging Protocol Handlers</span></span>

<span data-ttu-id="6a536-111">Le processus SearchIndexer (searchindexer.exe) lance une copie du processus SearchProtocolHost (SearchProtocolHost.exe) dans le contexte système et une autre copie dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a536-111">The SearchIndexer process (searchindexer.exe) launches one copy of the SearchProtocolHost process (SearchProtocolHost.exe) in the system context and another copy in the user context.</span></span> <span data-ttu-id="6a536-112">Ensuite, les gestionnaires de protocole sont chargés dans le processus SearchProtocolHost en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="6a536-112">Then, the protocol handlers are loaded in the SearchProtocolHost process as needed.</span></span> <span data-ttu-id="6a536-113">Ils ne sont pas déchargés tant que le service de recherche n’est pas arrêté.</span><span class="sxs-lookup"><span data-stu-id="6a536-113">They are not unloaded until the search service is stopped.</span></span> <span data-ttu-id="6a536-114">La même instance d’un gestionnaire de protocole est réutilisée autant de fois que le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6a536-114">The same instance of a protocol handler is reused any number of times while the service is running.</span></span>

<span data-ttu-id="6a536-115">Les processus SearchIndexer et SearchProtocolHost communiquent fréquemment pendant l’indexation.</span><span class="sxs-lookup"><span data-stu-id="6a536-115">The SearchIndexer and SearchProtocolHost processes communicate frequently during indexing.</span></span> <span data-ttu-id="6a536-116">Si vous suspendez ou arrêtez le processus SearchProtocolHost à déboguer, le SearchIndexer lance un nouveau processus SearchProtocolHost, invalidant la session de débogage.</span><span class="sxs-lookup"><span data-stu-id="6a536-116">If you pause or stop the SearchProtocolHost process to debug, the SearchIndexer will launch a new SearchProtocolHost process, invalidating your debugging session.</span></span> <span data-ttu-id="6a536-117">En outre, si vous attachez directement votre débogueur au processus SearchProtocolHost, vous pouvez rompre l’héritage handle-héritage à partir de searchindexer.exe à searchprotocolhost.exe, et les deux processus ne pourront pas communiquer.</span><span class="sxs-lookup"><span data-stu-id="6a536-117">Also, if you attach your debugger directly to the SearchProtocolHost process, you can break handle-inheritance from searchindexer.exe to searchprotocolhost.exe, and the two processes will be unable to communicate.</span></span>

<span data-ttu-id="6a536-118">Pour éviter ces problèmes, vous devez notifier le service de recherche que vous déboguez, et vous devez attacher le débogueur au processus SearchIndexer avec des instructions pour déboguer les processus enfants, comme décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6a536-118">To avoid these problems, you need to notify the search service that you are debugging, and you need to attach the debugger to the SearchIndexer process with instructions to debug child processes, as described next.</span></span>

## <a name="setting-up-debugging"></a><span data-ttu-id="6a536-119">Configuration du débogage</span><span class="sxs-lookup"><span data-stu-id="6a536-119">Setting Up Debugging</span></span>

<span data-ttu-id="6a536-120">Procédez comme suit pour configurer le débogage de votre gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="6a536-120">Follow these steps to set up debugging for your protocol handler.</span></span>

1.  <span data-ttu-id="6a536-121">Informez le service de recherche que vous déboguez en affectant la valeur 1 à la valeur DebugFilters dans le registre :</span><span class="sxs-lookup"><span data-stu-id="6a536-121">Notify the search service that you are debugging by setting the DebugFilters value to 1 in the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  <span data-ttu-id="6a536-122">Attachez un débogueur à l’aide de la clé de registre des options d’exécution du fichier image :</span><span class="sxs-lookup"><span data-stu-id="6a536-122">Attach a debugger using the Image File Execution Options registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    <span data-ttu-id="6a536-123">Les options d’un débogueur d’exemple sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6a536-123">The options for a sample debugger are described in the following table.</span></span>

    

    <span data-ttu-id="6a536-124">**Exemple utilisant le** débogueur ntsd Debugger *= C : \\ débogueurs \\ntsd.exe-odGx-C : "sXe LD mydll.dll ; g"*   </span><span class="sxs-lookup"><span data-stu-id="6a536-124">**Example using the ntsd debugger**   *Debugger = C:\\debuggers\\ntsd.exe -odGx -c: "sxe ld mydll.dll;g"*</span></span><br/>

3.  <span data-ttu-id="6a536-125">Redémarrez searchindexer.exe sous le débogueur en utilisant compmgmt. msc, services. msc ou une fenêtre de commande avec des commandes semblables à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="6a536-125">Restart searchindexer.exe under the debugger using compmgmt.msc, services.msc, or a command window with commands similar to the following:</span></span>
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

<span data-ttu-id="6a536-126">Pour faire la distinction entre un processus SearchProtocolHost en cours d’exécution dans le contexte système et un processus en cours d’exécution dans le contexte de l’utilisateur, vous pouvez passer en revue les chaînes d’environnement.</span><span class="sxs-lookup"><span data-stu-id="6a536-126">To distinguish between a SearchProtocolHost process running in the system context and one running in the user context, you can review the environment strings.</span></span> <span data-ttu-id="6a536-127">Par exemple, avec ntsd.exe, vous pouvez utiliser la commande d’extension **! PEB** pour afficher une vue mise en forme des informations contenues dans le bloc Process Environment (PEB).</span><span class="sxs-lookup"><span data-stu-id="6a536-127">With ntsd.exe, for example, you can use extension command **!peb** to display a formatted view of the information in the process environment block (PEB).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a536-128">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6a536-128">Additional Resources</span></span>

-   <span data-ttu-id="6a536-129">Pour plus d’informations sur la création de gestionnaires, consultez [inscription d’extensions de Shell](../shell/reg-shell-exts.md).</span><span class="sxs-lookup"><span data-stu-id="6a536-129">For information on creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a536-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a536-130">Related topics</span></span>

<dl> <span data-ttu-id="6a536-131">Développement <dt>**conceptuel**</dt> de <dt><a href="-search-3x-wds-phaddins.md">gestionnaires de protocoles</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Présentation des gestionnaires de protocole</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">notification de l’index des modifications</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Ajout d’icônes et de menus contextuels</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">exemple de code : extensions de Shell pour les gestionnaires de protocole</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">création d’un connecteur de recherche pour un gestionnaire de protocole</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">installation et inscription de gestionnaires de protocole</a></dt> </span><span class="sxs-lookup"><span data-stu-id="6a536-131"><dt>**Conceptual**</dt> <dt><a href="-search-3x-wds-phaddins.md">Developing Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Understanding Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">Notifying the Index of Changes</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Adding Icons and Context Menus</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">Code Sample: Shell Extensions for Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">Creating a Search Connector for a Protocol Handler</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">Installing and Registering Protocol Handlers</a></dt> </span></span></dl>

 

 
