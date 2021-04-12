---
title: Manifeste de l’application (exécutable)
description: Manifeste de l’application (exécutable)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104031985"
---
# <a name="app-executable-manifest"></a><span data-ttu-id="6a144-103">Manifeste de l’application (exécutable)</span><span class="sxs-lookup"><span data-stu-id="6a144-103">App (executable) manifest</span></span>

## <a name="platforms"></a><span data-ttu-id="6a144-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="6a144-104">Platforms</span></span>

<span data-ttu-id="6a144-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a144-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="6a144-106">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a144-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="6a144-107">Description</span><span class="sxs-lookup"><span data-stu-id="6a144-107">Description</span></span>

<span data-ttu-id="6a144-108">La section compatibilité du manifeste de l’application (exécutable) introduite dans Windows permet au système d’exploitation de déterminer les versions de Windows qu’une application a été conçue pour cibler.</span><span class="sxs-lookup"><span data-stu-id="6a144-108">The compatibility section of the app (executable) manifest introduced in Windows helps the operating system determine the versions of Windows an app was designed to target.</span></span> <span data-ttu-id="6a144-109">En outre, le manifeste de l’application permet à Windows de fournir le comportement attendu par l’application en fonction de la version de Windows ciblée par l’application.</span><span class="sxs-lookup"><span data-stu-id="6a144-109">Additionally, the app manifest enables Windows to provide the behavior that the app expects based on the version of Windows that the app targeted.</span></span>

<span data-ttu-id="6a144-110">La section compatibilité du manifeste permet à Windows de fournir un nouveau comportement aux nouveaux logiciels tout en conservant la compatibilité des logiciels existants.</span><span class="sxs-lookup"><span data-stu-id="6a144-110">The compatibility section of the manifest allows Windows to provide new behavior to newly created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="6a144-111">Cette section permet également à Windows d’offrir une meilleure compatibilité dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="6a144-111">This section helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="6a144-112">Par exemple, une application qui déclare la prise en charge de Windows 8 uniquement dans la section compatibilité continuera à recevoir le comportement de Windows 8 dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="6a144-112">For example, an app declaring support for only Windows 8 in the compatibility section will continue to receive Windows 8 behavior in future versions of Windows.</span></span>

## <a name="manifestation"></a><span data-ttu-id="6a144-113">Manifestation</span><span class="sxs-lookup"><span data-stu-id="6a144-113">Manifestation</span></span>

<span data-ttu-id="6a144-114">Les applications sans section de compatibilité dans leur manifeste présentent le comportement de Windows Vista par défaut sur Windows 7 et Windows 8, ainsi que les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="6a144-114">Apps without a compatibility section in their manifest will have Windows Vista behavior by default on Windows 7 and Windows 8 and future Windows versions.</span></span> <span data-ttu-id="6a144-115">N’oubliez pas que Windows XP et Windows Vista ignorent cette section du manifeste et qu’il n’a aucun impact sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="6a144-115">Be aware that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="6a144-116">Ces composants Windows fournissent un comportement divergent en fonction de la section compatibilité :</span><span class="sxs-lookup"><span data-stu-id="6a144-116">These Windows components provide divergent behavior based on the compatibility section:</span></span>

<span data-ttu-id="6a144-117">**Pool de threads par défaut de l’appel de procédure distante (RPC)**</span><span class="sxs-lookup"><span data-stu-id="6a144-117">**Remote procedure call (RPC) default thread pool**</span></span>

-   <span data-ttu-id="6a144-118">Windows 8 et Windows 7 : pour améliorer l’évolutivité et réduire le nombre de threads, RPC bascule vers le pool de threads NT (pool par défaut).</span><span class="sxs-lookup"><span data-stu-id="6a144-118">Windows 8 and Windows 7: To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="6a144-119">Pour Windows Vista, RPC utilisait un pool de threads privés :</span><span class="sxs-lookup"><span data-stu-id="6a144-119">For Windows Vista, RPC used a private thread pool:</span></span>

    -   <span data-ttu-id="6a144-120">Pour les fichiers binaires compilés pour Windows 7 et les versions ultérieures de Windows, le pool par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6a144-120">For binaries compiled for Windows 7 and later versions of Windows, the default pool is used.</span></span>
    -   <span data-ttu-id="6a144-121">Si I \_ RpcMgmtEnableDedicatedThreadPool est appelé avant l’appel d’une API RPC, le pool de threads privés est utilisé (comportement Vista).</span><span class="sxs-lookup"><span data-stu-id="6a144-121">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior).</span></span>
    -   <span data-ttu-id="6a144-122">Si j' \_ RpcMgmtEnableDedicatedThreadPool est appelé après un appel RPC, le pool par défaut est utilisé, je \_ RpcMgmtEnableDedicatedThreadPool renvoie l’erreur 1764 et l’opération demandée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6a144-122">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported.</span></span>

-   <span data-ttu-id="6a144-123">Windows Vista (par défaut) : pour les fichiers binaires compilés pour Windows Vista et les versions antérieures de Windows, le pool privé est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6a144-123">Windows Vista (default): For binaries compiled for Windows Vista and earlier versions of Windows, the private pool is used.</span></span>

<span data-ttu-id="6a144-124">**Verrouillage DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="6a144-124">**DirectDraw lock**</span></span>

-   <span data-ttu-id="6a144-125">Windows 8 et Windows 7 : les applications manifestées pour Windows 7 et les versions ultérieures du système d’exploitation ne peuvent pas appeler l’API Lock dans DDRAW pour verrouiller la mémoire tampon de la vidéo principale du bureau. Cela entraînera une erreur et un pointeur NULL pour le réplica principal est retourné.</span><span class="sxs-lookup"><span data-stu-id="6a144-125">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of the operating system cannot call Lock API in DDRAW to lock the primary desktop video buffer; doing so will result in an error, and a NULL pointer for the primary is returned.</span></span> <span data-ttu-id="6a144-126">Ce comportement est appliqué même si Gestionnaire de fenêtrage composition n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="6a144-126">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="6a144-127">Les applications dont la compatibilité est déclarée pour Windows 7 et les versions ultérieures ne doivent pas verrouiller la mémoire tampon vidéo principale à restituer.</span><span class="sxs-lookup"><span data-stu-id="6a144-127">Apps with compatibility declared for Windows 7 and later must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="6a144-128">Windows Vista (par défaut) : les applications peuvent acquérir un verrou sur la mémoire tampon vidéo principale, car les applications héritées dépendent de ce comportement. l’exécution de l’application désactive Gestionnaire de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="6a144-128">Windows Vista (default): Apps can acquire a lock on the primary video buffer, as legacy apps depend on this behavior; running the app turns off Desktop Window Manager.</span></span>

<span data-ttu-id="6a144-129">**Transfert de bloc de bits (BitBlt) DirectDraw vers le réplica principal sans fenêtre de découpage**</span><span class="sxs-lookup"><span data-stu-id="6a144-129">**DirectDraw bit-block transfer (bitblt) to primary without clipping window**</span></span>

-   <span data-ttu-id="6a144-130">Windows 8 et Windows 7 : les applications manifestes pour Windows 7 et les versions ultérieures de Windows ne sont pas en mesure d’effectuer un BitBlt dans la mémoire tampon vidéo principale du bureau sans fenêtre de découpage ; Cela génère une erreur et la zone BitBlt ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="6a144-130">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of Windows are prevented from performing a bitblt to the primary Desktop video buffer without a clipping window; doing so results in an error and the bitblt area will not be rendered.</span></span> <span data-ttu-id="6a144-131">Windows applique ce comportement même si vous n’activez pas la composition Gestionnaire de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="6a144-131">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="6a144-132">Les applications dont la compatibilité est déclarée pour Windows 7 et les versions ultérieures doivent effectuer un BitBlt dans une fenêtre de découpage.</span><span class="sxs-lookup"><span data-stu-id="6a144-132">Apps with compatibility declared for Windows 7 and later must perform a bitblt to a clipping window.</span></span>
-   <span data-ttu-id="6a144-133">Windows Vista (par défaut) : les applications doivent être en mesure d’effectuer un BitBlt sur le serveur principal sans fenêtre de découpage, car les applications héritées dépendent de ce comportement. l’exécution de cette application désactive l’Gestionnaire de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="6a144-133">Windows Vista (default): Apps must be able to perform a bitblt to the primary without a clipping window, as legacy apps depend on this behavior; running this app turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="6a144-134">**API GetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="6a144-134">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="6a144-135">Windows 8 et Windows 7 : résout une condition de concurrence dans laquelle une application multithread utilisant **GetOverlappedResult** peut retourner sans réinitialiser l’événement dans la structure OVERLAPPED, provoquant le retour prématuré de l’appel suivant à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="6a144-135">Windows 8 and Windows 7: Resolves a race condition where a multithreaded app using **GetOverlappedResult** can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="6a144-136">Windows Vista (par défaut) : fournit le comportement avec la condition de concurrence sur laquelle les applications peuvent avoir une dépendance.</span><span class="sxs-lookup"><span data-stu-id="6a144-136">Windows Vista (default): Provides the behavior with the race condition that apps might have a dependency on.</span></span> <span data-ttu-id="6a144-137">Les applications qui doivent éviter cette concurrence avant le comportement de Windows 7 doivent attendre l’événement Overlapped et, lorsqu’elles sont signalées, appeler GetOverlappedResult avec bWait = = FALSe.</span><span class="sxs-lookup"><span data-stu-id="6a144-137">Apps that must avoid this race prior to the Windows 7 behavior should wait on the overlapped event and, when signaled, call GetOverlappedResult with bWait == FALSE.</span></span>

<span data-ttu-id="6a144-138">**État des thèmes de Shell en mode de contraste élevé**</span><span class="sxs-lookup"><span data-stu-id="6a144-138">**Shell themes status in high contrast mode**</span></span>

-   <span data-ttu-id="6a144-139">Windows 8 : retourne l’état des thèmes réels pour lorsqu’il est en mode de contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="6a144-139">Windows 8: Returns the real theming status for when in high contrast mode.</span></span>
-   <span data-ttu-id="6a144-140">Windows 7 : retourne un thème non disponible en mode de contraste élevé, car DWM est toujours activé.</span><span class="sxs-lookup"><span data-stu-id="6a144-140">Windows 7: Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>
-   <span data-ttu-id="6a144-141">Windows Vista (par défaut) : retourne comme non disponible en mode de contraste élevé, car DWM est toujours activé.</span><span class="sxs-lookup"><span data-stu-id="6a144-141">Windows Vista (default): Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>

<span data-ttu-id="6a144-142">**Shell iPersistFile :: Save, méthode**</span><span class="sxs-lookup"><span data-stu-id="6a144-142">**Shell iPersistFile::Save method**</span></span>

-   <span data-ttu-id="6a144-143">Windows 8 : CShellLink :: Save détermine maintenant si le gestionnaire IPersistFile est appelé avec un argument de chemin d’accès relatif et fait échouer l’appel si c’est le cas.</span><span class="sxs-lookup"><span data-stu-id="6a144-143">Windows 8: CShellLink::Save now determines if the IPersistFile handler is called with a relative path argument and fails the call if it is.</span></span>

    <span data-ttu-id="6a144-144">La [documentation publique](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) qui décrit ce comportement indique que l’argument de chemin d’accès doit être un chemin d’accès absolu :</span><span class="sxs-lookup"><span data-stu-id="6a144-144">The [public documentation](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) describing this behavior indicates that path argument has to be an absolute path:</span></span>

-   <span data-ttu-id="6a144-145">Windows 7 et versions antérieures (par défaut) : CShellLink :: Save ne détermine pas si le gestionnaire iPersistFile envoie un contrôle de chemin d’accès relatif et permet aux applications de continuer à travailler avec des chemins d’accès absolus ou relatifs.</span><span class="sxs-lookup"><span data-stu-id="6a144-145">Windows 7 and earlier (default): CShellLink::Save does not determine if the iPersistFile handler sends a relative path check and allows apps to continue working with absolute or relative paths.</span></span>

<span data-ttu-id="6a144-146">**Assistant Compatibilité des programmes (PCA)**</span><span class="sxs-lookup"><span data-stu-id="6a144-146">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="6a144-147">Windows 8 : les applications avec la section compatibilité n’obtiennent pas l’atténuation de l’APC.</span><span class="sxs-lookup"><span data-stu-id="6a144-147">Windows 8: Apps with the compatibility section do not get the PCA mitigation.</span></span>
-   <span data-ttu-id="6a144-148">Windows 7 : les applications avec la section compatibilité sont suivies pour détecter les problèmes de compatibilité potentiels pour les modifications apportées à Windows 8 (décrits dans ce document).</span><span class="sxs-lookup"><span data-stu-id="6a144-148">Windows 7: Apps with the compatibility section are tracked for potential compatibility issues for Windows 8 changes (described in this document).</span></span>
-   <span data-ttu-id="6a144-149">Windows Vista (par défaut) : les applications qui ne parviennent pas à s’installer correctement ou se bloquer pendant l’exécution dans certaines circonstances spécifiques obtiennent l’atténuation de l’APC.</span><span class="sxs-lookup"><span data-stu-id="6a144-149">Windows Vista (default): Apps that fail to install properly or crash during runtime under some specific circumstances get the PCA mitigation.</span></span> <span data-ttu-id="6a144-150">Pour plus d’informations, consultez la section ressources.</span><span class="sxs-lookup"><span data-stu-id="6a144-150">For more info, see the Resources section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="6a144-151">Exploitation des fonctionnalités de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="6a144-151">Leveraging feature capabilities</span></span>

<span data-ttu-id="6a144-152">Mettez à jour le manifeste d’application avec les dernières informations de compatibilité pour la prise en charge du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6a144-152">Update the app manifest with the latest compatibility info for operating system support.</span></span> <span data-ttu-id="6a144-153">Cette section décrit les ajouts apportés au manifeste :</span><span class="sxs-lookup"><span data-stu-id="6a144-153">This section describes the additions to the manifest:</span></span>

<span data-ttu-id="6a144-154">**Espace de noms :** Compatibility. v1 (xmlns = "urn : schemas-microsoft-com : Compatibility. v1" >)</span><span class="sxs-lookup"><span data-stu-id="6a144-154">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

<span data-ttu-id="6a144-155">**Nom de la section :** Compatibilité (nouvelle section)</span><span class="sxs-lookup"><span data-stu-id="6a144-155">**Section name:** Compatibility (new section)</span></span>

<span data-ttu-id="6a144-156">**Pris en charge :** GUID du système d’exploitation pris en charge : les GUID mappés aux systèmes d’exploitation pris en charge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="6a144-156">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

-   <span data-ttu-id="6a144-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="6a144-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span>

    <span data-ttu-id="6a144-158">pour **Windows Vista**: il s’agit de la valeur par défaut pour le contexte Switchback</span><span class="sxs-lookup"><span data-stu-id="6a144-158">for **Windows Vista**: This is the default value for the switchback context</span></span>

-   <span data-ttu-id="6a144-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="6a144-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span>

    <span data-ttu-id="6a144-160">pour **Windows 7**: les applications qui définissent cette valeur dans le manifeste de l’application obtiennent le comportement de Windows 7</span><span class="sxs-lookup"><span data-stu-id="6a144-160">for **Windows 7**: Apps that set this value in the app manifest get the Windows 7 behavior</span></span>

-   <span data-ttu-id="6a144-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="6a144-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span>

    <span data-ttu-id="6a144-162">pour **Windows 8**: les applications qui définissent cette valeur dans le manifeste de l’application obtiennent le comportement de Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a144-162">for **Windows 8**: Apps that set this value in the application manifest get the Windows 8 behavior</span></span>

<span data-ttu-id="6a144-163">Microsoft génère et publie des GUID pour les futures versions de Windows, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6a144-163">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

<span data-ttu-id="6a144-164">Exemple XML d’un manifeste mis à jour :</span><span class="sxs-lookup"><span data-stu-id="6a144-164">An XML example of an updated manifest:</span></span>

> [!Note]  
> <span data-ttu-id="6a144-165">L’attribut et les noms de balise dans le manifeste de l’application respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="6a144-165">The attribute and tag names in the app manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



<span data-ttu-id="6a144-166">Les GUID pour tous les systèmes d’exploitation de l’exemple précédent offrent une prise en charge de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="6a144-166">The GUIDs for all the operating systems in the previous example provide down-level support.</span></span> <span data-ttu-id="6a144-167">Les applications qui prennent en charge plusieurs plateformes n’ont pas besoin de manifestes séparés pour chaque plateforme.</span><span class="sxs-lookup"><span data-stu-id="6a144-167">Apps that support multiple platforms do not need separate manifests for each platform.</span></span>

## <a name="tests"></a><span data-ttu-id="6a144-168">Tests</span><span class="sxs-lookup"><span data-stu-id="6a144-168">Tests</span></span>

<span data-ttu-id="6a144-169">Une application peut spécifier plusieurs ID de système d’exploitation pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6a144-169">An app can specify multiple supported operating system IDs.</span></span> <span data-ttu-id="6a144-170">Vous devez ajouter un ID de système d’exploitation pris en charge si vous avez testé ou si vous êtes en train de tester l’application sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6a144-170">You should add a supported operating system ID if you have tested, or are in the process of testing, the app on that operating system.</span></span> <span data-ttu-id="6a144-171">Windows Vista et les versions antérieures du système d’exploitation ne prêtent pas attention à ces entrées.</span><span class="sxs-lookup"><span data-stu-id="6a144-171">Windows Vista and prior operating system versions do not pay attention to these entries.</span></span> <span data-ttu-id="6a144-172">À compter de Windows 7, Windows choisit le GUID de la version la plus élevée dans le manifeste jusqu’à la version Windows en cours d’exécution et donne à ce niveau la prise en charge de l’application.</span><span class="sxs-lookup"><span data-stu-id="6a144-172">Starting with Windows 7, Windows will choose the highest version GUID in the manifest up to the running Windows version, and give the app support at that level.</span></span> <span data-ttu-id="6a144-173">Pour vérifier que l’application fonctionne avec la nouvelle section de compatibilité du manifeste de l’application :</span><span class="sxs-lookup"><span data-stu-id="6a144-173">To verify that the app works with the new app manifest compatibility section:</span></span>

1.  <span data-ttu-id="6a144-174">Testez l’application avec la nouvelle section de compatibilité et la prise en charge d’ID = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} pour vous assurer que l’application fonctionne correctement à l’aide du comportement Windows 8 le plus récent.</span><span class="sxs-lookup"><span data-stu-id="6a144-174">Test the app with the new compatibility section and SupportedOS ID = { 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} to ensure that the app works properly using the latest Windows 8 behavior.</span></span>
2.  <span data-ttu-id="6a144-175">Testez l’application avec la nouvelle section de compatibilité et l’ID d’ID pris en charge = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} pour vous assurer que l’application fonctionne correctement à l’aide du comportement de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6a144-175">Test the app with the new compatibility section and SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} to ensure that the app works properly using the Windows 7 behavior.</span></span>
3.  <span data-ttu-id="6a144-176">Testez l’application avec la nouvelle section de compatibilité et l’ID d’ID pris en charge = {e2011457-1546-43C5-a5fe-008deee3d3f0} pour vous assurer que l’application fonctionne correctement à l’aide du comportement de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a144-176">Test the app with the new compatibility section and SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0} to ensure that the app works properly using the Windows Vista behavior.</span></span>

## <a name="resources"></a><span data-ttu-id="6a144-177">Ressources</span><span class="sxs-lookup"><span data-stu-id="6a144-177">Resources</span></span>

-   [<span data-ttu-id="6a144-178">QueryActCtxW fonction)</span><span class="sxs-lookup"><span data-stu-id="6a144-178">QueryActCtxW Function</span></span>](../sbscs/application-manifests.md)
-   <span data-ttu-id="6a144-179">[Manifeste de contrôle de compte d’utilisateur](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6a144-179">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="6a144-180">Manifestes d’application pour les applications Windows</span><span class="sxs-lookup"><span data-stu-id="6a144-180">Application Manifests for Windows Applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="6a144-181">Gestionnaire de fenêtrage (DWM)</span><span class="sxs-lookup"><span data-stu-id="6a144-181">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="6a144-182">Mise à jour des incompatibilités de contexte</span><span class="sxs-lookup"><span data-stu-id="6a144-182">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)
-   <span data-ttu-id="6a144-183">[Assistant Compatibilité des programmes](/previous-versions/bb756937(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6a144-183">[Program Compatibility Assistant](/previous-versions/bb756937(v=msdn.10))</span></span>

 

 