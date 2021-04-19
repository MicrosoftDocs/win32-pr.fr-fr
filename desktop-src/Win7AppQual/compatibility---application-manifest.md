---
description: .
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifeste d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4fd1ae8a9f66dafbe65a3db09dd014dbef31e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535037"
---
# <a name="application-manifest"></a><span data-ttu-id="0e41f-103">Manifeste d’application</span><span class="sxs-lookup"><span data-stu-id="0e41f-103">Application Manifest</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="0e41f-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="0e41f-104">Affected Platforms</span></span>

<span data-ttu-id="0e41f-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e41f-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="0e41f-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0e41f-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="0e41f-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="0e41f-107">Feature Impact</span></span>

 <span data-ttu-id="0e41f-108">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="0e41f-108">**Severity** - Low</span></span>  
<span data-ttu-id="0e41f-109">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="0e41f-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="0e41f-110">Description</span><span class="sxs-lookup"><span data-stu-id="0e41f-110">Description</span></span>

<span data-ttu-id="0e41f-111">Windows 7 introduit une nouvelle section dans le manifeste de l’application appelée « compatibilité ».</span><span class="sxs-lookup"><span data-stu-id="0e41f-111">Windows 7 introduces a new section in the application manifest called "Compatibility."</span></span> <span data-ttu-id="0e41f-112">Cette section aide Windows à déterminer les versions de Windows qu’une application a été conçue pour cibler, et permet à Windows de fournir le comportement attendu par l’application en fonction de la version de Windows ciblée par l’application.</span><span class="sxs-lookup"><span data-stu-id="0e41f-112">This section helps Windows determine the versions of Windows that an application was designed to target, and enables Windows to provide the behavior that the application expects based on the version of Windows that the application targeted.</span></span>

<span data-ttu-id="0e41f-113">La section compatibilité permet à Windows de fournir un nouveau comportement aux nouveaux logiciels créés par des développeurs tout en conservant la compatibilité des logiciels existants.</span><span class="sxs-lookup"><span data-stu-id="0e41f-113">The Compatibility section allows Windows to provide new behavior to new developer-created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="0e41f-114">Cette section aide également Windows à offrir une meilleure compatibilité dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="0e41f-114">This section also helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="0e41f-115">Par exemple, une application qui déclare uniquement la prise en charge de Windows 7 dans la section compatibilité continuera à recevoir le comportement de Windows 7 dans la prochaine version de Windows.</span><span class="sxs-lookup"><span data-stu-id="0e41f-115">For example, an application declaring support only for Windows 7 in the Compatibility section will continue to receive Windows 7 behavior in future version of Windows.</span></span>

## <a name="manifestation-of-change"></a><span data-ttu-id="0e41f-116">Manifeste de modification</span><span class="sxs-lookup"><span data-stu-id="0e41f-116">Manifestation of Change</span></span>

<span data-ttu-id="0e41f-117">Les applications sans section de compatibilité dans leur manifeste recevront le comportement de Windows Vista par défaut sur Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="0e41f-117">Applications without a Compatibility section in their manifest will receive Windows Vista behavior by default on Windows 7 and future Windows versions.</span></span> <span data-ttu-id="0e41f-118">Notez que Windows XP et Windows Vista ignorent cette section du manifeste et qu’il n’a aucun impact sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="0e41f-118">Note that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="0e41f-119">Les composants Windows suivants fournissent un comportement divergent basé sur la section compatibilité dans Windows 7 :</span><span class="sxs-lookup"><span data-stu-id="0e41f-119">The following Windows components provide divergent behavior based on the Compatibility section in Windows 7:</span></span>

<span data-ttu-id="0e41f-120">**Pool de threads par défaut RPC**</span><span class="sxs-lookup"><span data-stu-id="0e41f-120">**RPC Default Thread Pool**</span></span>

-   <span data-ttu-id="0e41f-121">**Windows 7 :** Pour améliorer l’évolutivité et réduire le nombre de threads, RPC bascule vers le pool de threads NT (pool par défaut).</span><span class="sxs-lookup"><span data-stu-id="0e41f-121">**Windows 7:** To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="0e41f-122">Pour Windows Vista, RPC utilisait un pool de threads privés.</span><span class="sxs-lookup"><span data-stu-id="0e41f-122">For Windows Vista, RPC used a private thread pool.</span></span>
    -   <span data-ttu-id="0e41f-123">Pour les fichiers binaires compilés pour Win7, le pool par défaut est utilisé</span><span class="sxs-lookup"><span data-stu-id="0e41f-123">For binaries compiled for Win7 the default pool is used</span></span>
    -   <span data-ttu-id="0e41f-124">Si I \_ RpcMgmtEnableDedicatedThreadPool est appelé avant l’appel d’une API RPC, le pool de threads privés est utilisé (comportement Vista)</span><span class="sxs-lookup"><span data-stu-id="0e41f-124">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior)</span></span>
    -   <span data-ttu-id="0e41f-125">Si j' \_ RpcMgmtEnableDedicatedThreadPool est appelé après un appel RPC, le pool par défaut est utilisé, je \_ RpcMgmtEnableDedicatedThreadPool renvoie l’erreur 1764 et l’opération demandée n’est pas prise en charge</span><span class="sxs-lookup"><span data-stu-id="0e41f-125">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported</span></span>
-   <span data-ttu-id="0e41f-126">**Windows Vista (par défaut) :** Pour les fichiers binaires compilés pour Windows Vista et les versions antérieures, le pool privé est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0e41f-126">**Windows Vista (default):** For binaries compiled for Windows Vista and below, the private pool is used.</span></span>

<span data-ttu-id="0e41f-127">**Verrouillage DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="0e41f-127">**DirectDraw Lock**</span></span>

-   <span data-ttu-id="0e41f-128">**Windows 7 :** Les applications manifestées pour Windows 7 ne peuvent pas appeler l’API Lock dans DDRAW pour verrouiller la mémoire tampon de la vidéo de bureau principale.</span><span class="sxs-lookup"><span data-stu-id="0e41f-128">**Windows 7:** Applications manifested for Windows 7 cannot call Lock API in DDRAW to lock the primary Desktop video buffer.</span></span> <span data-ttu-id="0e41f-129">Cela génère une erreur et le renvoi du pointeur **null** pour le réplica principal est retourné.</span><span class="sxs-lookup"><span data-stu-id="0e41f-129">Doing so will result in error, and **NULL** pointer for the primary will be returned.</span></span> <span data-ttu-id="0e41f-130">Ce comportement est appliqué même si Gestionnaire de fenêtrage composition n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="0e41f-130">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="0e41f-131">Les applications compatibles Windows 7 ne doivent pas verrouiller la mémoire tampon vidéo principale pour effectuer le rendu.</span><span class="sxs-lookup"><span data-stu-id="0e41f-131">Windows 7 compatible applications must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="0e41f-132">**Windows Vista (par défaut) :** Les applications seront en mesure d’acquérir un verrou sur la mémoire tampon vidéo principale, car les applications héritées dépendent de ce comportement.</span><span class="sxs-lookup"><span data-stu-id="0e41f-132">**Windows Vista (default):** Applications will be able to acquire a lock on the primary video buffer as legacy applications depend on this behavior.</span></span> <span data-ttu-id="0e41f-133">L’exécution de l’application désactive Gestionnaire de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="0e41f-133">Running the application turns off Desktop Window Manager.</span></span>

<span data-ttu-id="0e41f-134">**Transfert de bloc binaire (BLT) DirectDraw vers le réplica principal sans fenêtre de détourage**</span><span class="sxs-lookup"><span data-stu-id="0e41f-134">**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**</span></span>

-   <span data-ttu-id="0e41f-135">**Windows 7 :** Les applications manifestes pour Windows 7 ne sont pas en mesure d’effectuer des BLT sur la mémoire tampon vidéo principale du bureau sans fenêtre de détourage.</span><span class="sxs-lookup"><span data-stu-id="0e41f-135">**Windows 7:** Applications manifested for Windows 7 are prevented from performing Blt's to the primary Desktop video buffer without a clipping window.</span></span> <span data-ttu-id="0e41f-136">Cela génère une erreur et la zone BLT ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="0e41f-136">Doing so will result in error and the Blt area will not be rendered.</span></span> <span data-ttu-id="0e41f-137">Windows applique ce comportement même si vous n’activez pas la composition Gestionnaire de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="0e41f-137">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="0e41f-138">Les applications compatibles Windows 7 doivent être BLT dans une fenêtre de détourage.</span><span class="sxs-lookup"><span data-stu-id="0e41f-138">Windows 7 compatible applications must Blt to a clipping window.</span></span>
-   <span data-ttu-id="0e41f-139">**Windows Vista (par défaut) :** Les applications doivent pouvoir accéder au BLT sur le réplica principal sans fenêtre de découpage, car les applications héritées dépendent de ce comportement.</span><span class="sxs-lookup"><span data-stu-id="0e41f-139">**Windows Vista (default):** Applications must be able to Blt to the primary without a clipping window as legacy applications depend on this behavior.</span></span> <span data-ttu-id="0e41f-140">L’exécution de cette application désactive l’Gestionnaire de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="0e41f-140">Running this application turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="0e41f-141">**API GetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="0e41f-141">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="0e41f-142">**Windows 7 :** Résout une condition de concurrence où une application multithread utilisant GetOverlappedResult peut retourner sans réinitialiser l’événement dans la structure OVERLAPPED, provoquant le retour prématuré de l’appel suivant à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="0e41f-142">**Windows 7:** Resolves a race condition where a multithreaded app using GetOverlappedResult can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="0e41f-143">**Windows Vista (par défaut) :** Fournit le comportement avec la condition de concurrence sur laquelle les applications peuvent avoir une dépendance.</span><span class="sxs-lookup"><span data-stu-id="0e41f-143">**Windows Vista (default):** Provides the behavior with the race condition that applications may have a dependency on.</span></span> <span data-ttu-id="0e41f-144">Les applications qui souhaitent éviter cette course avant le comportement de Windows 7 doivent attendre l’événement Overlapped et, lorsqu’elles sont signalées, appeler GetOverlappedResult avec bWait = = **false**.</span><span class="sxs-lookup"><span data-stu-id="0e41f-144">Applications wishing to avoid this race prior to the Windows 7 behavior should wait on the overlapped event and when signaled, call GetOverlappedResult with bWait == **FALSE**.</span></span>

<span data-ttu-id="0e41f-145">**Assistant Compatibilité des programmes (PCA)**</span><span class="sxs-lookup"><span data-stu-id="0e41f-145">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="0e41f-146">**Windows 7 :** La section applications avec compatibilité n’obtiendra pas l’atténuation de l’APC.</span><span class="sxs-lookup"><span data-stu-id="0e41f-146">**Windows 7:** Applications with Compatibility section will not get the PCA mitigation.</span></span>
-   <span data-ttu-id="0e41f-147">**Windows Vista (par défaut) :** Les applications qui ne parviennent pas à s’installer correctement ou se bloquer lors de l’exécution dans certaines circonstances spécifiques obtiennent l’atténuation de l’APC.</span><span class="sxs-lookup"><span data-stu-id="0e41f-147">**Windows Vista (default):** Applications that fail to install properly or crash during runtime under some specific circumstances will get the PCA mitigation.</span></span> <span data-ttu-id="0e41f-148">Pour plus d’informations, consultez la section référence.</span><span class="sxs-lookup"><span data-stu-id="0e41f-148">For more details, see the reference section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="0e41f-149">Exploitation des fonctionnalités de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="0e41f-149">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="0e41f-150">Mettez à jour le manifeste d’application avec les dernières informations de compatibilité pour la prise en charge du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0e41f-150">Update the application manifest with the latest Compatibility information for operating system support.</span></span> <span data-ttu-id="0e41f-151">La section décrit les ajouts au manifeste :</span><span class="sxs-lookup"><span data-stu-id="0e41f-151">The section describes the additions to the manifest:</span></span>

-   <span data-ttu-id="0e41f-152">**Espace de noms :** Compatibility. v1 (xmlns = "urn : schemas-microsoft-com : Compatibility. v1" >)</span><span class="sxs-lookup"><span data-stu-id="0e41f-152">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

-   <span data-ttu-id="0e41f-153">**Nom de la section :** Compatibilité (nouvelle section)</span><span class="sxs-lookup"><span data-stu-id="0e41f-153">**Section Name:** Compatibility (new section)</span></span>

-   <span data-ttu-id="0e41f-154">**Pris en charge :** GUID du système d’exploitation pris en charge : les GUID mappés aux systèmes d’exploitation pris en charge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="0e41f-154">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

    -   <span data-ttu-id="0e41f-155">{e2011457-1546-43C5-a5fe-008deee3d3f0} pour Windows Vista : il s’agit de la valeur par défaut pour le contexte Switchback.</span><span class="sxs-lookup"><span data-stu-id="0e41f-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} for Windows Vista: This is the default value for the switchback context.</span></span>
    -   <span data-ttu-id="0e41f-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} pour Windows 7 : les applications qui définissent cette valeur dans le manifeste de l’application obtiennent le comportement de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0e41f-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} for Windows 7: Applications that set this value in the application manifest get the Windows 7 behavior.</span></span>

    > [!Note]  
    > <span data-ttu-id="0e41f-157">Microsoft génère et publie des GUID pour les futures versions de Windows, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0e41f-157">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

     

<span data-ttu-id="0e41f-158">Voici un exemple de manifeste mis à jour.</span><span class="sxs-lookup"><span data-stu-id="0e41f-158">The following is an example of an updated manifest.</span></span>

> [!Note]  
> <span data-ttu-id="0e41f-159">L’attribut et les noms de balise dans le manifeste de l’application respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="0e41f-159">The attribute and tag names in the application manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



<span data-ttu-id="0e41f-160">La valeur de l’ajout de GUID pour les deux systèmes d’exploitation dans l’exemple ci-dessus consiste à fournir une prise en charge de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="0e41f-160">The value of adding GUIDs for both operating systems in the above example is to provide down-level support.</span></span> <span data-ttu-id="0e41f-161">Les applications qui prennent en charge les deux plateformes n’ont pas besoin de manifestes séparés pour chaque plateforme.</span><span class="sxs-lookup"><span data-stu-id="0e41f-161">Applications that support both platforms would not need separate manifests for each platform.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="0e41f-162">Compatibilité, performances, fiabilité et test d’utilisabilité</span><span class="sxs-lookup"><span data-stu-id="0e41f-162">Compatibility, Performance, Reliability, and Usability Testing</span></span>

1.  <span data-ttu-id="0e41f-163">Testez l’application avec la nouvelle section de compatibilité et `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` Assurez-vous que l’application fonctionne correctement à l’aide du comportement Windows 7 le plus récent</span><span class="sxs-lookup"><span data-stu-id="0e41f-163">Test the application with the new compatibility section and `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` to ensure that the application works properly using the latest Windows 7 behavior</span></span>
2.  <span data-ttu-id="0e41f-164">Testez l’application avec la nouvelle section de compatibilité et `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (ou sans cette section entièrement) pour vous assurer que l’application fonctionne correctement à l’aide des comportements Windows Vista sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e41f-164">Test the application with the new compatibility section and `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (or without this section entirely) to ensure that the application works properly using the Windows Vista behaviors on Windows 7</span></span>

## <a name="known-issues"></a><span data-ttu-id="0e41f-165">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="0e41f-165">Known Issues</span></span>

<span data-ttu-id="0e41f-166">**Incompatibilité de contexte** Une application s’exécute dans un contexte Windows Vista plutôt que dans un contexte Windows 7 sur un ordinateur qui exécute une édition x64 de Windows 7 ou Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="0e41f-166">**Context Mismatch** An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of either Windows 7 or Windows Server 2008 R2.</span></span>

<span data-ttu-id="0e41f-167">**Solution** Des mises à jour sont disponibles pour corriger cette erreur pour toutes les versions x64 prises en charge de Windows 7 et Windows Server 2008 R2, ainsi que pour toutes les versions Itanium prises en charge de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="0e41f-167">**Solution** Updates are available to correct this for all supported x64-based versions of Windows 7 and Windows Server 2008 R2, as well as for all supported Itanium-based versions of Windows Server 2008 R2.</span></span> <span data-ttu-id="0e41f-168">Accédez à la page de Support Microsoft pour [KB 978637 : une application s’exécute dans un contexte Windows Vista plutôt que dans un contexte Windows 7 sur un ordinateur qui exécute une édition x64 de Windows 7 ou de Windows Server 2008 R2](https://support.microsoft.com/kb/978637) pour obtenir des détails supplémentaires et télécharger la version appropriée pour votre système.</span><span class="sxs-lookup"><span data-stu-id="0e41f-168">Go to the Microsoft Support page for [KB 978637: An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of Windows 7 or of Windows Server 2008 R2](https://support.microsoft.com/kb/978637) for additional details and to download the correct version for your system.</span></span>

<span data-ttu-id="0e41f-169">**Diagnostic de vidage sur incident bloqué**</span><span class="sxs-lookup"><span data-stu-id="0e41f-169">**Crash dump diagnosis blocked**</span></span>

<span data-ttu-id="0e41f-170">**Solution** Accédez à la page de Support Microsoft de la [base de connaissances KB 976038 : les exceptions levées à partir d’une application qui s’exécute dans une version 64 bits de Windows sont ignorées](https://support.microsoft.com/kb/976038) pour obtenir des détails supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0e41f-170">**Solution** Go to the Microsoft Support page for [KB 976038: Exceptions that are thrown from an application that runs in a 64-bit version of Windows are ignored](https://support.microsoft.com/kb/976038) for additional details.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="0e41f-171">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="0e41f-171">Links to Other Resources</span></span>

-   [<span data-ttu-id="0e41f-172">**QueryActCtxW fonction)**</span><span class="sxs-lookup"><span data-stu-id="0e41f-172">**QueryActCtxW Function**</span></span>](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   <span data-ttu-id="0e41f-173">[Manifeste de contrôle de compte d’utilisateur](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="0e41f-173">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="0e41f-174">Manifestes d’application pour les applications Windows</span><span class="sxs-lookup"><span data-stu-id="0e41f-174">Application manifests for Windows applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="0e41f-175">Gestionnaire de fenêtrage (DWM)</span><span class="sxs-lookup"><span data-stu-id="0e41f-175">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="0e41f-176">Mise à jour des incompatibilités de contexte</span><span class="sxs-lookup"><span data-stu-id="0e41f-176">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)

 

 
