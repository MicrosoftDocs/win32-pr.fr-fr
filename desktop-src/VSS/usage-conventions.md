---
description: Lorsque vous développez votre propre application VSS, vous devez respecter les instructions et restrictions suivantes.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Compatibilité des applications VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318409"
---
# <a name="vss-application-compatibility"></a><span data-ttu-id="f8821-103">Compatibilité des applications VSS</span><span class="sxs-lookup"><span data-stu-id="f8821-103">VSS Application Compatibility</span></span>

<span data-ttu-id="f8821-104">Lorsque vous développez votre propre application VSS, vous devez respecter les instructions et restrictions suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8821-104">When developing your own VSS application, you should observe the following guidelines and restrictions.</span></span> <span data-ttu-id="f8821-105">Il peut s’avérer utile de faire référence à l’exemple de code pour les demandeurs VSS, les fournisseurs et les rédacteurs fournis dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f8821-105">You may find it helpful to refer to the sample code for VSS requesters, providers, and writers that is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="f8821-106">Le SDK Windows peut être utilisé pour développer des applications VSS uniquement pour Windows Vista et les versions ultérieures du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="f8821-106">The Windows SDK can be used to develop VSS applications only for Windows Vista and later Windows operating system versions.</span></span> <span data-ttu-id="f8821-107">Elle ne peut pas être utilisée pour développer des demandeurs VSS, des fournisseurs ou des enregistreurs pour Windows Server 2003 R2, Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f8821-107">It cannot be used to develop VSS requesters, providers, or writers for Windows Server 2003 R2, Windows Server 2003, or Windows XP.</span></span>

 

<span data-ttu-id="f8821-108">**Windows server 2003 R2, Windows server 2003 et Windows XP :** VSS est disponible dans le kit de développement logiciel (SDK) Service VSS 7,2, que vous pouvez télécharger à partir de [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) .</span><span class="sxs-lookup"><span data-stu-id="f8821-108">**Windows Server 2003 R2, Windows Server 2003 and Windows XP:** VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="f8821-109">Notez que les fichiers vssapi. lib 64 bits dans les répertoires du répertoire Win2003 \\ obj peuvent être utilisés pour les versions 64 bits de Windows server 2003 R2, Windows server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f8821-109">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 R2, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="f8821-110">Ce kit de développement logiciel (SDK) fournit également un exemple de code pour les demandeurs VSS, les fournisseurs et les writers.</span><span class="sxs-lookup"><span data-stu-id="f8821-110">This SDK also provides sample code for VSS requesters, providers, and writers.</span></span>

## <a name="compiling-vss-applications"></a><span data-ttu-id="f8821-111">Compilation d’applications VSS</span><span class="sxs-lookup"><span data-stu-id="f8821-111">Compiling VSS Applications</span></span>

<span data-ttu-id="f8821-112">Lors du développement d’un demandeur, par exemple une application de sauvegarde :</span><span class="sxs-lookup"><span data-stu-id="f8821-112">When developing a requester, such as a backup application:</span></span>

-   <span data-ttu-id="f8821-113">Incluez les en-têtes suivants :</span><span class="sxs-lookup"><span data-stu-id="f8821-113">Include the following headers:</span></span> <dl> <span data-ttu-id="f8821-114">VSS. h</span><span class="sxs-lookup"><span data-stu-id="f8821-114">Vss.h</span></span>  
    <span data-ttu-id="f8821-115">VsWriter. h</span><span class="sxs-lookup"><span data-stu-id="f8821-115">VsWriter.h</span></span>  
    <span data-ttu-id="f8821-116">VsBackup. h</span><span class="sxs-lookup"><span data-stu-id="f8821-116">VsBackup.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="f8821-117">VssApi. lib</span><span class="sxs-lookup"><span data-stu-id="f8821-117">VssApi.Lib</span></span>  
    </dl>

<span data-ttu-id="f8821-118">Lors du développement d’un enregistreur :</span><span class="sxs-lookup"><span data-stu-id="f8821-118">When developing a writer:</span></span>

-   <span data-ttu-id="f8821-119">Incluez les en-têtes suivants :</span><span class="sxs-lookup"><span data-stu-id="f8821-119">Include the following headers:</span></span> <dl> <span data-ttu-id="f8821-120">VSS. h</span><span class="sxs-lookup"><span data-stu-id="f8821-120">Vss.h</span></span>  
    <span data-ttu-id="f8821-121">VsWriter. h</span><span class="sxs-lookup"><span data-stu-id="f8821-121">VsWriter.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="f8821-122">VssApi. lib</span><span class="sxs-lookup"><span data-stu-id="f8821-122">VssApi.lib</span></span>  
    </dl>

## <a name="supported-configurations-and-restrictions"></a><span data-ttu-id="f8821-123">Configurations et restrictions prises en charge</span><span class="sxs-lookup"><span data-stu-id="f8821-123">Supported Configurations and Restrictions</span></span>

<span data-ttu-id="f8821-124">La liste suivante décrit les configurations et restrictions prises en charge :</span><span class="sxs-lookup"><span data-stu-id="f8821-124">The following list describes supported configurations and restrictions:</span></span>

-   <span data-ttu-id="f8821-125">VSS est fourni et pris en charge sur les versions du système d’exploitation Windows à compter de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f8821-125">VSS is provided and supported on versions of the Windows operating system beginning with Windows XP.</span></span>
-   <span data-ttu-id="f8821-126">Le tableau suivant récapitule les informations de compatibilité entre les différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="f8821-126">The following table summarizes compatibility information across Windows versions.</span></span> <span data-ttu-id="f8821-127">Notez que si une application VSS est « compilée pour » une version de Windows spécifiée, cela signifie que l’application a été compilée à l’aide des fichiers d’en-tête et des bibliothèques qui sont spécifiques à cette version.</span><span class="sxs-lookup"><span data-stu-id="f8821-127">Note that if a VSS application is "compiled for" a specified Windows version, this means that the application was compiled using the header files and libraries that are specific to that version.</span></span>

    > [!Note]  
    > <span data-ttu-id="f8821-128">Les fournisseurs de matériel s’exécutent uniquement sur les versions de système d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f8821-128">Hardware providers will run only on Windows server operating system versions.</span></span> <span data-ttu-id="f8821-129">Ils ne s’exécuteront pas sur les versions des systèmes d’exploitation clients Windows.</span><span class="sxs-lookup"><span data-stu-id="f8821-129">They will not run on Windows client operating system versions.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="f8821-130">Dans les tableaux suivants, Windows Server 2008 avec Service Pack 2 (SP2) doit être considéré comme le même que Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f8821-130">In the following tables, Windows Server 2008 with Service Pack 2 (SP2) should be considered the same as Windows Server 2008.</span></span> <span data-ttu-id="f8821-131">Pour plus d’informations sur Windows Server 2008 avec SP2, consultez <https://go.microsoft.com/fwlink/p/?linkid=178730> .</span><span class="sxs-lookup"><span data-stu-id="f8821-131">For more information about Windows Server 2008 with SP2, see <https://go.microsoft.com/fwlink/p/?linkid=178730>.</span></span> <span data-ttu-id="f8821-132">Windows Server 2003 R2 doit être considéré comme Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f8821-132">Windows Server 2003 R2 should be considered the same as Windows Server 2003.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="f8821-133">Si une application VSS est compilée pour Windows Server 2003 ou une version ultérieure, elle s’exécutera également sur les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="f8821-133">If a VSS application is compiled for Windows Server 2003 or later, it will also run on later versions of Windows.</span></span>

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f8821-134">Redemandeurs VSS, enregistreurs et fournisseurs compilés pour</span><span class="sxs-lookup"><span data-stu-id="f8821-134">VSS requesters, writers, and providers compiled for</span></span></th>
    <th><span data-ttu-id="f8821-135">S’exécutera sur</span><span class="sxs-lookup"><span data-stu-id="f8821-135">Will run on</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="f8821-136">Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) et Windows Vista (64 bits)</span><span class="sxs-lookup"><span data-stu-id="f8821-136">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    <td><span data-ttu-id="f8821-137">Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) et Windows Vista (64 bits)</span><span class="sxs-lookup"><span data-stu-id="f8821-137">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f8821-138">Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) et Windows Vista (32 bits)</span><span class="sxs-lookup"><span data-stu-id="f8821-138">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    <td><span data-ttu-id="f8821-139">Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) et Windows Vista (32 bits)</span><span class="sxs-lookup"><span data-stu-id="f8821-139">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="f8821-140">Windows Server 2003 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="f8821-140">Windows Server 2003 (64-bit)</span></span></td>
    <td><span data-ttu-id="f8821-141">Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits), Windows Vista (64 bits) et Windows Server 2003 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="f8821-141">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit), Windows Vista (64-bit), and Windows Server 2003 (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f8821-142">Windows Server 2003 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="f8821-142">Windows Server 2003 (32-bit)</span></span></td>
    <td><span data-ttu-id="f8821-143">Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits), Windows Vista (32 bits) et Windows Server 2003 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="f8821-143">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit), Windows Vista (32-bit), and Windows Server 2003 (32-bit)</span></span> <blockquote>
    [!Note]<br />
<span data-ttu-id="f8821-144">Les demandeurs s’exécuteront également sur Windows Server 2003 (64 bits).</span><span class="sxs-lookup"><span data-stu-id="f8821-144">Requesters will also run on Windows Server 2003 (64-bit).</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="f8821-145">Windows XP Édition 64 bits</span><span class="sxs-lookup"><span data-stu-id="f8821-145">Windows XP 64-Bit Edition</span></span></td>
    <td><span data-ttu-id="f8821-146">Windows Server 2003 (64 bits) et Windows XP 64 bits Edition</span><span class="sxs-lookup"><span data-stu-id="f8821-146">Windows Server 2003 (64-bit) and Windows XP 64-Bit Edition</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f8821-147">Windows XP (32 bits)</span><span class="sxs-lookup"><span data-stu-id="f8821-147">Windows XP (32-bit)</span></span></td>
    <td><span data-ttu-id="f8821-148">Windows XP (32 bits)</span><span class="sxs-lookup"><span data-stu-id="f8821-148">Windows XP (32-bit)</span></span></td>
    </tr>
    </tbody>
    </table>

    

     

    

    | <span data-ttu-id="f8821-149">Pour compiler un demandeur, un enregistreur ou un fournisseur VSS pour</span><span class="sxs-lookup"><span data-stu-id="f8821-149">To compile a VSS requester, writer, or provider for</span></span>        | <span data-ttu-id="f8821-150">Utilisation</span><span class="sxs-lookup"><span data-stu-id="f8821-150">Use</span></span>                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f8821-151">Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="f8821-151">Windows Server 2008 R2 or Windows 7</span></span>                        | <span data-ttu-id="f8821-152">SDK Windows pour Windows 7 (disponible à partir du [Centre de téléchargement Windows](https://www.microsoft.com/download/details.aspx?id=8279)).</span><span class="sxs-lookup"><span data-stu-id="f8821-152">Windows SDK for Windows 7 (Available from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).)</span></span>                |
    | <span data-ttu-id="f8821-153">Windows Server 2008 ou Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8821-153">Windows Server 2008 or Windows Vista</span></span>                       | <span data-ttu-id="f8821-154">SDK Windows pour Windows Server 2008 (disponible dans le [Centre de développement SDK Windows](https://msdn.microsoft.com/windows/bb980924.aspx).)</span><span class="sxs-lookup"><span data-stu-id="f8821-154">Windows SDK for Windows Server 2008 (Available from the [Windows SDK Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx).)</span></span> |
    | <span data-ttu-id="f8821-155">Windows Server 2003 R2, Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="f8821-155">Windows Server 2003 R2, Windows Server 2003, or Windows XP</span></span> | [<span data-ttu-id="f8821-156">Kit de développement logiciel (SDK) Service VSS 7,2</span><span class="sxs-lookup"><span data-stu-id="f8821-156">Volume Shadow Copy Service 7.2 SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   <span data-ttu-id="f8821-157">Toutes les applications VSS 32 bits (demandeurs, fournisseurs et enregistreurs) doivent s’exécuter en tant qu’applications natives 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f8821-157">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="f8821-158">Leur exécution sous WOW64 n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f8821-158">Running them under WOW64 is not supported.</span></span>

    <span data-ttu-id="f8821-159">**Windows Server 2003 et Windows XP :** L’exécution de demandeurs VSS 32 bits sous WOW64 est prise en charge, mais pas pour les sauvegardes de l’état du système.</span><span class="sxs-lookup"><span data-stu-id="f8821-159">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="f8821-160">L’exécution des fournisseurs et des enregistreurs VSS 32 bits sous WOW64 n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f8821-160">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="f8821-161">La prise en charge de l’exécution de demandeurs 32 bits sous WOW64 a été supprimée dans Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f8821-161">Support for running 32- bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

-   <span data-ttu-id="f8821-162">Un cliché instantané créé sur Windows Server 2003 R2 ou Windows Server 2003 ne peut pas être utilisé sur un ordinateur qui exécute Windows Server 2008 R2 ou Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f8821-162">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="f8821-163">Un cliché instantané créé sur Windows Server 2008 R2 ou Windows Server 2008 ne peut pas être utilisé sur un ordinateur qui exécute Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f8821-163">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="f8821-164">Toutefois, un cliché instantané créé sur Windows Server 2008 peut être utilisé sur un ordinateur qui exécute Windows Server 2008 R2, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="f8821-164">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>
-   <span data-ttu-id="f8821-165">Pour prendre en charge les clichés instantanés, un système exécutant VSS doit avoir au moins un système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="f8821-165">To support shadow copies, a system running VSS must have at least one NTFS file system.</span></span> <span data-ttu-id="f8821-166">Ce système de fichiers hébergera la « zone diff » du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="f8821-166">This file system will host the shadow copy's "diff area."</span></span> <span data-ttu-id="f8821-167">Pour plus d’informations, consultez [fournisseur système](providers.md).</span><span class="sxs-lookup"><span data-stu-id="f8821-167">For more information, see [System Provider](providers.md).</span></span>
-   <span data-ttu-id="f8821-168">Compte tenu de la présence d’un système de fichiers NTFS et du choix approprié du contexte (consultez [configurations du contexte](shadow-copy-context-configurations.md)de cliché instantané), tous les systèmes de fichiers locaux pris en charge peuvent être des clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="f8821-168">Given the presence of one NTFS file system, and given the appropriate choice of context (see [Shadow Copy Context Configurations](shadow-copy-context-configurations.md)), any supported local file system can be shadow copied.</span></span>
-   <span data-ttu-id="f8821-169">Vous pouvez créer des clichés instantanés uniquement pour les systèmes de fichiers montés localement.</span><span class="sxs-lookup"><span data-stu-id="f8821-169">You can make shadow copies only for locally mounted file systems.</span></span> <span data-ttu-id="f8821-170">Les partages distants et autres systèmes de fichiers montés sur plusieurs systèmes de fichiers ne peuvent pas être des clichés instantanés par le système qui les monte.</span><span class="sxs-lookup"><span data-stu-id="f8821-170">Remote shares and other cross-mounted file systems cannot be shadow copied by the system that mounts them.</span></span> <span data-ttu-id="f8821-171">Ces systèmes de fichiers peuvent être des clichés instantanés uniquement par les systèmes qui traitent les systèmes de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f8821-171">These file systems can be shadow copied only by the systems that serve out the file systems.</span></span>
-   <span data-ttu-id="f8821-172">Les rédacteurs et les demandeurs doivent spécifier uniquement des ressources locales.</span><span class="sxs-lookup"><span data-stu-id="f8821-172">Writers and requesters should specify only local resources.</span></span> <span data-ttu-id="f8821-173">Les ressources locales sont des ensembles de fichiers dont le chemin d’accès absolu commence par une lettre de lecteur, et la lettre de lecteur ne peut pas être associée à un dossier monté sur un partage distant.</span><span class="sxs-lookup"><span data-stu-id="f8821-173">Local resources are sets of files whose absolute path starts with a drive letter, and the drive letter cannot be associated with a mounted folder on a remote share.</span></span>
-   <span data-ttu-id="f8821-174">Le nombre maximal de clichés instantanés logiciels pour chaque volume est de 512.</span><span class="sxs-lookup"><span data-stu-id="f8821-174">The maximum number is of software shadow copies for each volume is 512.</span></span> <span data-ttu-id="f8821-175">Toutefois, par défaut, vous ne pouvez conserver que 64 clichés instantanés utilisés par la fonctionnalité Clichés instantanés de dossiers partagés.</span><span class="sxs-lookup"><span data-stu-id="f8821-175">However, by default you can only maintain 64 shadow copies that are used by the Shadow Copies of Shared Folders feature.</span></span> <span data-ttu-id="f8821-176">Pour modifier la limite de la fonctionnalité clichés instantanés de dossiers partagés, utilisez la clé de Registre [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="f8821-176">To change the limit for the Shadow Copies of Shared Folders feature, use the [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) registry key.</span></span>
-   <span data-ttu-id="f8821-177">L’infrastructure des composants de sauvegarde ne prend pas en charge la sauvegarde des ressources de cluster en tant que composants d’écriture.</span><span class="sxs-lookup"><span data-stu-id="f8821-177">The Backup Components infrastructure does not support backing up cluster resources as writer components.</span></span> <span data-ttu-id="f8821-178">Pour sauvegarder des ressources de cluster, les applications doivent supposer que le chemin d’accès est local à un nœud de cluster particulier spécifié.</span><span class="sxs-lookup"><span data-stu-id="f8821-178">To back up cluster resources, applications should assume that the path is local to a specified particular cluster node.</span></span>
-   [!Note]  
    > <span data-ttu-id="f8821-179">Microsoft ne fournit pas de support technique pour les développeurs ou les professionnels de l’informatique pour l’implémentation de restaurations en ligne sur l’état du système sur Windows (toutes les versions).</span><span class="sxs-lookup"><span data-stu-id="f8821-179">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

     

    <span data-ttu-id="f8821-180">Lors de la sauvegarde et de la récupération de l’état du système, la stratégie recommandée consiste à sauvegarder et à récupérer les volumes système et de démarrage en plus des fichiers énumérés par les Writers d’État du système.</span><span class="sxs-lookup"><span data-stu-id="f8821-180">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span>

    > [!Note]  
    > <span data-ttu-id="f8821-181">Les Writers d’État du système sont des enregistreurs dont l’attribut de [**\_ \_ type d’utilisation VSS**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) est défini sur VSS \_ ut \_ BOOTABLESYSTEMSTATE ou VSS \_ ut \_ SYSTEMSERVICE.</span><span class="sxs-lookup"><span data-stu-id="f8821-181">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

     

 

 
