---
description: VShadow est un outil de ligne de commande que vous pouvez utiliser pour créer et gérer des clichés instantanés de volume.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Outil et exemple VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485025"
---
# <a name="vshadow-tool-and-sample"></a><span data-ttu-id="3dc90-103">Outil et exemple VShadow</span><span class="sxs-lookup"><span data-stu-id="3dc90-103">VShadow Tool and Sample</span></span>

<span data-ttu-id="3dc90-104">VShadow est un outil de ligne de commande que vous pouvez utiliser pour créer et gérer des clichés instantanés de volume.</span><span class="sxs-lookup"><span data-stu-id="3dc90-104">VShadow is a command-line tool that you can use to create and manage volume shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="3dc90-105">VShadow est inclus dans le kit de développement logiciel (SDK) Microsoft Windows pour Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3dc90-105">VShadow is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="3dc90-106">Le kit de développement logiciel (SDK) VSS 7,2 comprend une version de VShadow qui s’exécute uniquement sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3dc90-106">The VSS 7.2 SDK includes a version of VShadow that runs only on Windows Server 2003.</span></span> <span data-ttu-id="3dc90-107">Pour plus d’informations sur le téléchargement de la SDK Windows et du kit de développement logiciel (SDK) VSS 7,2, consultez [service VSS](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="3dc90-107">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="3dc90-108">L’outil VShadow utilise des options de ligne de commande et des indicateurs facultatifs pour identifier le travail à effectuer.</span><span class="sxs-lookup"><span data-stu-id="3dc90-108">The VShadow tool uses command-line options and optional flags to identify the work to perform.</span></span> <span data-ttu-id="3dc90-109">Lorsqu’elle est utilisée sans aucune option de ligne de commande, la commande VShadow crée un jeu de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="3dc90-109">When used without any command-line options, the VShadow command creates a new shadow copy set.</span></span>

<span data-ttu-id="3dc90-110">Les commandes VShadow effectuent les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3dc90-110">VShadow commands perform the following operations:</span></span>

-   [<span data-ttu-id="3dc90-111">Création d’un jeu de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="3dc90-111">Creating a Shadow Copy Set</span></span>](#creating-a-shadow-copy-set)
-   [<span data-ttu-id="3dc90-112">Importation d’un jeu de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="3dc90-112">Importing a Shadow Copy Set</span></span>](#importing-a-shadow-copy-set)
-   [<span data-ttu-id="3dc90-113">Interrogation des propriétés des clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="3dc90-113">Querying Shadow Copy Properties</span></span>](#querying-shadow-copy-properties)
-   [<span data-ttu-id="3dc90-114">Suppression de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="3dc90-114">Deleting Shadow Copies</span></span>](#deleting-shadow-copies)
-   [<span data-ttu-id="3dc90-115">Rupture d’un jeu de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="3dc90-115">Breaking a Shadow Copy Set</span></span>](#breaking-a-shadow-copy-set)
-   [<span data-ttu-id="3dc90-116">Rupture d’un jeu de clichés instantanés à l’aide de la méthode BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="3dc90-116">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [<span data-ttu-id="3dc90-117">Exposition locale d’un cliché instantané</span><span class="sxs-lookup"><span data-stu-id="3dc90-117">Exposing a Shadow Copy Locally</span></span>](#exposing-a-shadow-copy-locally)
-   [<span data-ttu-id="3dc90-118">Exposition à distance d’un cliché instantané</span><span class="sxs-lookup"><span data-stu-id="3dc90-118">Exposing a Shadow Copy Remotely</span></span>](#exposing-a-shadow-copy-remotely)
-   [<span data-ttu-id="3dc90-119">Affichage de l’État et des métadonnées de l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="3dc90-119">Listing Writer Status and Metadata</span></span>](#listing-writer-status-and-metadata)
-   [<span data-ttu-id="3dc90-120">Exécution d’opérations de restauration</span><span class="sxs-lookup"><span data-stu-id="3dc90-120">Performing Restore Operations</span></span>](#performing-restore-operations)
-   [<span data-ttu-id="3dc90-121">Retour à un cliché instantané précédent</span><span class="sxs-lookup"><span data-stu-id="3dc90-121">Reverting to a Previous Shadow Copy</span></span>](#reverting-to-a-previous-shadow-copy)
-   [<span data-ttu-id="3dc90-122">Resynchronisation des numéros d’unités logiques</span><span class="sxs-lookup"><span data-stu-id="3dc90-122">Resynchronizing LUNs</span></span>](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a><span data-ttu-id="3dc90-123">Création d’un jeu de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="3dc90-123">Creating a Shadow Copy Set</span></span>

<span data-ttu-id="3dc90-124">**vshadow** \[ OptionalFlags \] *VolumeList*</span><span class="sxs-lookup"><span data-stu-id="3dc90-124">**vshadow** \[OptionalFlags\] *VolumeList*</span></span>

<span data-ttu-id="3dc90-125">Cette commande crée un jeu de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="3dc90-125">This command creates a new shadow copy set.</span></span>

<span data-ttu-id="3dc90-126">*VolumeList* est une liste de noms de volumes.</span><span class="sxs-lookup"><span data-stu-id="3dc90-126">*VolumeList* is a list of volume names.</span></span> <span data-ttu-id="3dc90-127">VShadow crée un cliché instantané pour chaque volume de la liste.</span><span class="sxs-lookup"><span data-stu-id="3dc90-127">VShadow creates one shadow copy for each volume in the list.</span></span> <span data-ttu-id="3dc90-128">Un nom de volume peut éventuellement se terminer par une barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="3dc90-128">A volume name can optionally be terminated with a backslash (\\).</span></span> <span data-ttu-id="3dc90-129">Par exemple, C : et C : \\ sont des noms de volume valides.</span><span class="sxs-lookup"><span data-stu-id="3dc90-129">For example, both C: and C:\\ are valid volume names.</span></span> <span data-ttu-id="3dc90-130">Vous pouvez également spécifier des dossiers montés (par exemple, C : \\ DirectoryName) ou des noms de GUID de volume (par exemple \\ \\ ? \\ Volume {edbed95e-7e8d-11D8-9D01-505054503030}).</span><span class="sxs-lookup"><span data-stu-id="3dc90-130">You can also specify mounted folders (for example, C:\\DirectoryName) or volume GUID names (for example, \\\\?\\Volume{edbed95e-7e8d-11d8-9d01-505054503030}).</span></span>

<span data-ttu-id="3dc90-131">*OptionalFlags* est un masque de transparence des valeurs d’indicateur facultatives du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3dc90-131">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3dc90-132">Valeur d’indicateur facultative</span><span class="sxs-lookup"><span data-stu-id="3dc90-132">Optional Flag Value</span></span></th>
<th><span data-ttu-id="3dc90-133">Description</span><span class="sxs-lookup"><span data-stu-id="3dc90-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3dc90-134"><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-134"><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-135">Cet indicateur facultatif spécifie les clichés instantanés matériels différentiels.</span><span class="sxs-lookup"><span data-stu-id="3dc90-135">This optional flag specifies differential hardware shadow copies.</span></span> <span data-ttu-id="3dc90-136">Cet indicateur et l’indicateur <strong>-AP</strong> s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="3dc90-136">This flag and the <strong>-ap</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-137">Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-137">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc90-138"><span id="-ap"></span><span id="-AP"></span><strong>-AP</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-138"><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-139">Cet indicateur facultatif spécifie les clichés instantanés matériels du Plex.</span><span class="sxs-lookup"><span data-stu-id="3dc90-139">This optional flag specifies plex hardware shadow copies.</span></span> <span data-ttu-id="3dc90-140">Cet indicateur et l’indicateur <strong>-ad</strong> s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="3dc90-140">This flag and the <strong>-ad</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-141">Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-141">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dc90-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-BC =</strong><em>file</em><strong>. xml</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span> <strong></strong> <strong>-bc=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-143">Cet indicateur facultatif spécifie les clichés instantanés non transportables et stocke le document des composants de sauvegarde dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="3dc90-143">This optional flag specifies non-transportable shadow copies and stores the Backup Components Document into the specified file.</span></span> <span data-ttu-id="3dc90-144">Ce fichier peut être utilisé dans une opération de restauration ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3dc90-144">This file can be used in a subsequent restore operation.</span></span> <span data-ttu-id="3dc90-145">Cet indicateur et l’indicateur <strong>-t</strong> s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="3dc90-145">This flag and the <strong>-t</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-146">Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-146">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc90-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-Exec =,</strong><em>commande</em></span><span class="sxs-lookup"><span data-stu-id="3dc90-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec=</strong><em>Command</em></span></span><br/></td>
<td><span data-ttu-id="3dc90-148">Cet indicateur facultatif exécute une commande ou un script après la création des clichés instantanés, mais avant la fermeture de l’outil VShadow.</span><span class="sxs-lookup"><span data-stu-id="3dc90-148">This optional flag executes a command or script after the shadow copies are created but before the VShadow tool exits.</span></span> <span data-ttu-id="3dc90-149">La <em>commande</em> peut spécifier une commande d’interpréteur de commandes exécutable ou un fichier cmd.</span><span class="sxs-lookup"><span data-stu-id="3dc90-149"><em>Command</em> can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="3dc90-150">Si elle spécifie une commande d’interpréteur de commandes, aucun paramètre de commande ne peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="3dc90-150">If it specifies a shell command, no command parameters can be specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-151">Pour des raisons de sécurité et pour simplifier l’implémentation, l’indicateur facultatif <strong>-Exec</strong> n’acceptera pas de paramètres à passer à la commande ou au script.</span><span class="sxs-lookup"><span data-stu-id="3dc90-151">For security reasons and to keep the implementation simple, the <strong>-exec</strong> optional flag will not accept parameters to be passed to the command or script.</span></span> <span data-ttu-id="3dc90-152">La chaîne entière transmise à l’indicateur facultatif <strong>-Exec</strong> est traitée comme un fichier cmd ou exe unique.</span><span class="sxs-lookup"><span data-stu-id="3dc90-152">The entire string passed to the <strong>-exec</strong> optional flag is treated as a single CMD or EXE file.</span></span> <span data-ttu-id="3dc90-153">Pour plus d’informations sur cette limitation, consultez le code source VShadow.</span><span class="sxs-lookup"><span data-stu-id="3dc90-153">For more information about this limitation, see the VShadow source code.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dc90-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-155">Cet indicateur facultatif spécifie que l’opération de cliché instantané ne doit être effectuée que si toutes les signatures de disque peuvent être restaurées.</span><span class="sxs-lookup"><span data-stu-id="3dc90-155">This optional flag specifies that the shadow copy operation should be completed only if all disk signatures can be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-156">Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-156">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3dc90-157"><strong>Windows Server 2003 :</strong> Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3dc90-157"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc90-158"><span id="-mask"></span><span id="-MASK"></span><strong>-Mask</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-158"><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-159">Cet indicateur facultatif spécifie que les numéros d’unités logiques des clichés instantanés doivent être masqués sur l’ordinateur lorsque le jeu de clichés instantanés est rompu.</span><span class="sxs-lookup"><span data-stu-id="3dc90-159">This optional flag specifies that the shadow copy LUNs should be masked from the computer when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-160">Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-160">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3dc90-161"><strong>Windows Server 2003 :</strong> Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3dc90-161"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dc90-162"><span id="-nar"></span><span id="-NAR"></span><strong>-NAR</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-162"><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-163">Cet indicateur facultatif spécifie les clichés instantanés sans récupération automatique.</span><span class="sxs-lookup"><span data-stu-id="3dc90-163">This optional flag specifies shadow copies without auto-recovery.</span></span> <span data-ttu-id="3dc90-164">Pour plus d’informations sur cette option, consultez la documentation de l’indicateur VSS_VOLSNAP_ATTR_NO_AUTORECOVERY de l’énumération <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3dc90-164">For more information about this option, see the documentation for the VSS_VOLSNAP_ATTR_NO_AUTORECOVERY flag of the <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> enumeration.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc90-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-Revert</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-166">Cet indicateur facultatif spécifie que les signatures de disque ne doivent pas être restaurées.</span><span class="sxs-lookup"><span data-stu-id="3dc90-166">This optional flag specifies that disk signatures should not be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-167">Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-167">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3dc90-168"><strong>Windows Server 2003 :</strong> Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3dc90-168"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dc90-169"><span id="-nw"></span><span id="-NW"></span><strong>-NW</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-169"><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-170">Cet indicateur facultatif spécifie les clichés instantanés sans impliquer d’enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="3dc90-170">This optional flag specifies shadow copies without involving writers.</span></span> <span data-ttu-id="3dc90-171">Pour plus d’informations sur les clichés instantanés sans participation aux rédacteurs, consultez détails de la création de clichés <a href="shadow-copy-creation-details.md">instantanés</a>.</span><span class="sxs-lookup"><span data-stu-id="3dc90-171">For more information about shadow copies without writer participation, see <a href="shadow-copy-creation-details.md">Shadow Copy Creation Details</a>.</span></span> <span data-ttu-id="3dc90-172">Cet indicateur et les indicateurs <strong>-Wi</strong> et <strong>-WX</strong> s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="3dc90-172">This flag and the <strong>-wi</strong> and <strong>-wx</strong> flags are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc90-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-174">Cet indicateur facultatif spécifie les <a href="vssgloss-p.md"><em>clichés instantanés persistants</em></a>.</span><span class="sxs-lookup"><span data-stu-id="3dc90-174">This optional flag specifies <a href="vssgloss-p.md"><em>persistent shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-175">Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-175">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dc90-176"><span id="-rw"></span><span id="-RW"></span><strong>-RW</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-176"><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-177">Cet indicateur facultatif spécifie que les numéros d’unités logiques des clichés instantanés doivent être en lecture/écriture lorsque le jeu de clichés instantanés est rompu.</span><span class="sxs-lookup"><span data-stu-id="3dc90-177">This optional flag specifies that the shadow copy LUNs should be made read/write when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-178">Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-178">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3dc90-179"><strong>Windows Server 2003 :</strong> Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3dc90-179"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc90-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-181">Cet indicateur facultatif spécifie <a href="vssgloss-c.md"><em>les clichés instantanés accessibles par le client</em></a>.</span><span class="sxs-lookup"><span data-stu-id="3dc90-181">This optional flag specifies <a href="vssgloss-c.md"><em>client-accessible shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-182">Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-182">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dc90-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script =</strong><em>file</em><strong>. cmd</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script=</strong><em>File</em><strong>.cmd</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-184">Cet indicateur facultatif génère un fichier CMD contenant les variables d’environnement associées aux clichés instantanés créés, comme les ID de cliché instantané et les ID de jeu de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="3dc90-184">This optional flag generates a CMD file containing environment variables related to the created shadow copies, such as shadow copy IDs and shadow copy set IDs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc90-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>file</em><strong>. xml</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-186">Cet indicateur facultatif spécifie les clichés instantanés transportables et stocke le document des composants de sauvegarde dans le fichier spécifié par le paramètre <em>File.xml</em> .</span><span class="sxs-lookup"><span data-stu-id="3dc90-186">This optional flag specifies transportable shadow copies and stores the Backup Components Document into the file specified by the <em>File.xml</em> parameter.</span></span> <span data-ttu-id="3dc90-187">Ce fichier peut être utilisé dans une opération d’importation et/ou de restauration ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3dc90-187">This file can be used in a subsequent import and/or restore operation.</span></span> <span data-ttu-id="3dc90-188">Cet indicateur et l’indicateur <strong>-BC</strong> s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="3dc90-188">This flag and the <strong>-bc</strong> flag are mutually exclusive.</span></span><br/> <span data-ttu-id="3dc90-189"><strong>Windows server 2003, Standard Edition et Windows server 2003, Web Edition :</strong> Les clichés instantanés transportables ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3dc90-189"><strong>Windows Server 2003, Standard Edition and Windows Server 2003, Web Edition:</strong> Transportable shadow copies are not supported.</span></span> <span data-ttu-id="3dc90-190">Toutes les éditions de Windows Server 2003 avec Service Pack 1 (SP1) prennent en charge les clichés instantanés transportables.</span><span class="sxs-lookup"><span data-stu-id="3dc90-190">All editions of Windows Server 2003 with Service Pack 1 (SP1) support transportable shadow copies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dc90-191"><span id="-tr"></span><span id="-TR"></span><strong>-TR</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-191"><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-192">Cet indicateur facultatif spécifie que la récupération TxF doit être appliquée lors de la création de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="3dc90-192">This optional flag specifies that TxF recovery should be enforced during shadow copy creation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-193">Cet indicateur est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-193">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc90-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-suivi</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-tracing</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-195">Cet indicateur facultatif génère une sortie détaillée qui peut être utilisée pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="3dc90-195">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dc90-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-Wait</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-197">Cet indicateur facultatif force l’outil VShadow à attendre la confirmation de l’utilisateur avant de quitter.</span><span class="sxs-lookup"><span data-stu-id="3dc90-197">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc90-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-Wi =</strong><em>enregistreur</em></span><span class="sxs-lookup"><span data-stu-id="3dc90-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="3dc90-199">Cet indicateur facultatif vérifie que le composant ou le writer spécifié est inclus dans le cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="3dc90-199">This optional flag verifies that the specified writer or component is included in the shadow copy.</span></span> <span data-ttu-id="3dc90-200">L' <em>enregistreur</em> peut spécifier un chemin d’accès de composant, un nom d’enregistreur, un ID d’enregistreur ou un ID d’instance d’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="3dc90-200"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="3dc90-201">Cet indicateur et l’indicateur <strong>-NW</strong> s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="3dc90-201">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dc90-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-WX =</strong><em>enregistreur</em></span><span class="sxs-lookup"><span data-stu-id="3dc90-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="3dc90-203">Cet indicateur facultatif vérifie que le composant ou le writer spécifié est exclu du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="3dc90-203">This optional flag verifies that the specified writer or component is excluded from the shadow copy.</span></span> <span data-ttu-id="3dc90-204">L' <em>enregistreur</em> peut spécifier un chemin d’accès de composant, un nom d’enregistreur, un ID d’enregistreur ou un ID d’instance d’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="3dc90-204"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="3dc90-205">Cet indicateur et l’indicateur <strong>-NW</strong> s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="3dc90-205">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a><span data-ttu-id="3dc90-206">Importation d’un jeu de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="3dc90-206">Importing a Shadow Copy Set</span></span>

<span data-ttu-id="3dc90-207">**vshadow** \[ OptionalFlags \] **-i =**_file_*_. xml_*</span><span class="sxs-lookup"><span data-stu-id="3dc90-207">**vshadow** \[OptionalFlags\] **-i=**_File_*_.xml_*</span></span>

<span data-ttu-id="3dc90-208">L’option de ligne **de commande-i** importe un jeu de clichés instantanés transportable.</span><span class="sxs-lookup"><span data-stu-id="3dc90-208">The **-i** command-line option imports a transportable shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="3dc90-209">Cette option de ligne de commande est prise en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-209">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="3dc90-210">Le fichier de *File.xml* doit être un fichier de document de composants de sauvegarde pour un jeu de clichés instantanés transportable créé avec l’indicateur facultatif **-t** ou **-BC** .</span><span class="sxs-lookup"><span data-stu-id="3dc90-210">The *File.xml* file must be a Backup Components Document file for a transportable shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="3dc90-211">Un jeu de clichés instantanés est un cliché [*instantané persistant*](vssgloss-p.md) s’il a été créé avec l’indicateur **-p** facultatif.</span><span class="sxs-lookup"><span data-stu-id="3dc90-211">A shadow copy set is a [*persistent shadow copy*](vssgloss-p.md) if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="3dc90-212">Si le jeu de clichés instantanés transportable n’est pas persistant, il apparaît pendant une brève période pendant l’exécution de la commande de création de clichés instantanés, et est automatiquement supprimé lorsque la commande retourne.</span><span class="sxs-lookup"><span data-stu-id="3dc90-212">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="3dc90-213">Vous pouvez importer des clichés instantanés non persistants uniquement lors de la création de clichés instantanés, en créant le jeu de clichés instantanés à l’aide de l’indicateur facultatif **-Exec** pour exécuter un fichier cmd qui appelle VShadow **-i**.</span><span class="sxs-lookup"><span data-stu-id="3dc90-213">You can import nonpersistent shadow copies only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls VShadow **-i**.</span></span>

<span data-ttu-id="3dc90-214">L’option de ligne **de commande-i** ne peut pas être combinée avec d’autres options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3dc90-214">The **-i** command-line option cannot be combined with other command-line options.</span></span>

<span data-ttu-id="3dc90-215">*OptionalFlags* est un masque de transparence des valeurs d’indicateur facultatives du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3dc90-215">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="3dc90-216">Valeur d’indicateur facultative</span><span class="sxs-lookup"><span data-stu-id="3dc90-216">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="3dc90-217">Description</span><span class="sxs-lookup"><span data-stu-id="3dc90-217">Description</span></span>                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc90-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-Exec =,**_commande_</span><span class="sxs-lookup"><span data-stu-id="3dc90-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="3dc90-219">Cet indicateur facultatif exécute une commande ou un script après l’importation des clichés instantanés, mais avant la sortie de l’outil VShadow.</span><span class="sxs-lookup"><span data-stu-id="3dc90-219">This optional flag executes a command or script after the shadow copies are imported but before the VShadow tool exits.</span></span> <span data-ttu-id="3dc90-220">La *commande* peut spécifier une commande d’interpréteur de commandes exécutable ou un fichier cmd.</span><span class="sxs-lookup"><span data-stu-id="3dc90-220">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="3dc90-221">Si elle spécifie une commande d’interpréteur de commandes, aucun paramètre de commande ne peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="3dc90-221">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="3dc90-222"><span id="-tracing"></span><span id="-TRACING"></span>**-suivi**</span><span class="sxs-lookup"><span data-stu-id="3dc90-222"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="3dc90-223">Cet indicateur facultatif génère une sortie détaillée qui peut être utilisée pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="3dc90-223">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="3dc90-224"><span id="-wait"></span><span id="-WAIT"></span>**-Wait**</span><span class="sxs-lookup"><span data-stu-id="3dc90-224"><span id="-wait"></span><span id="-WAIT"></span>**-wait**</span></span><br/>                                                           | <span data-ttu-id="3dc90-225">Cet indicateur facultatif force l’outil VShadow à attendre la confirmation de l’utilisateur avant de quitter.</span><span class="sxs-lookup"><span data-stu-id="3dc90-225">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a><span data-ttu-id="3dc90-226">Interrogation des propriétés des clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="3dc90-226">Querying Shadow Copy Properties</span></span>

<span data-ttu-id="3dc90-227">**vshadow** **-q**</span><span class="sxs-lookup"><span data-stu-id="3dc90-227">**vshadow** **-q**</span></span>

<span data-ttu-id="3dc90-228">**vshadow** **-qx =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="3dc90-228">**vshadow** **-qx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="3dc90-229">**vshadow** **-s =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="3dc90-229">**vshadow** **-s=**_ShadowCopyId_</span></span>

<span data-ttu-id="3dc90-230">L’option de ligne de commande **-q** répertorie les propriétés de tous les clichés instantanés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3dc90-230">The **-q** command-line option lists the properties of all shadow copies on the computer.</span></span>

<span data-ttu-id="3dc90-231">L’option de ligne de commande **-qx** répertorie les propriétés de tous les clichés instantanés dans le jeu de clichés instantanés dont l’ID est spécifié par *ShadowCopySetId*.</span><span class="sxs-lookup"><span data-stu-id="3dc90-231">The **-qx** command-line option lists the properties of all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="3dc90-232">L’option de ligne de commande **-s** répertorie les propriétés du cliché instantané dont l’ID est spécifié par *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="3dc90-232">The **-s** command-line option lists the properties of the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="3dc90-233">Ces options de ligne de commande utilisent une combinaison de [**IVssBackupComponents :: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) et [**IVssBackupComponents :: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) pour obtenir les propriétés du jeu de clichés instantanés donné.</span><span class="sxs-lookup"><span data-stu-id="3dc90-233">These command-line options use a combination of [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) and [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) to get the properties of the given set of shadow copies.</span></span>

<span data-ttu-id="3dc90-234">Les options de ligne de commande **-q**, **-qx** et **-s** s’excluent mutuellement et ne peuvent pas être combinées avec d’autres options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3dc90-234">The **-q**, **-qx**, and **-s** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="deleting-shadow-copies"></a><span data-ttu-id="3dc90-235">Suppression de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="3dc90-235">Deleting Shadow Copies</span></span>

<span data-ttu-id="3dc90-236">**vshadow** **-da**</span><span class="sxs-lookup"><span data-stu-id="3dc90-236">**vshadow** **-da**</span></span>

<span data-ttu-id="3dc90-237">**vshadow** **-do**</span><span class="sxs-lookup"><span data-stu-id="3dc90-237">**vshadow** **-do**</span></span>

<span data-ttu-id="3dc90-238">**vshadow** **-DX =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="3dc90-238">**vshadow** **-dx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="3dc90-239">**vshadow** **-DS =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="3dc90-239">**vshadow** **-ds=**_ShadowCopyId_</span></span>

<span data-ttu-id="3dc90-240">La commande **-da** supprime tous les clichés instantanés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3dc90-240">The **-da** command deletes all shadow copies on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="3dc90-241">L’option de ligne de commande **-da** requiert la confirmation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3dc90-241">The **-da** command-line option requires user confirmation.</span></span>

 

<span data-ttu-id="3dc90-242">L’option **de ligne de commande-do** supprime le cliché instantané le plus ancien sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3dc90-242">The **-do** command-line option deletes the oldest shadow copy on the computer.</span></span>

<span data-ttu-id="3dc90-243">L’option de ligne de commande **-DX** supprime tous les clichés instantanés dans le jeu de clichés instantanés dont l’ID est spécifié par *ShadowCopySetId*.</span><span class="sxs-lookup"><span data-stu-id="3dc90-243">The **-dx** command-line option deletes all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="3dc90-244">L’option de ligne de commande **-DS** supprime le cliché instantané dont l’ID est spécifié par *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="3dc90-244">The **-ds** command-line option deletes the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="3dc90-245">Ces options de ligne de commande sont destinées uniquement aux [*clichés instantanés persistants*](vssgloss-p.md) .</span><span class="sxs-lookup"><span data-stu-id="3dc90-245">These command-line options are for use with [*persistent shadow copies*](vssgloss-p.md) only.</span></span> <span data-ttu-id="3dc90-246">Les clichés instantanés non persistants n’ont pas besoin d’être explicitement supprimés, car ils sont automatiquement supprimés lors de la fermeture de la commande de création de VShadow.</span><span class="sxs-lookup"><span data-stu-id="3dc90-246">Nonpersistent shadow copies do not need to be explicitly deleted, because they are automatically deleted when the VShadow creation command exits.</span></span>

<span data-ttu-id="3dc90-247">Les options de ligne de commande **-da**, **-do**, **-DX** et **-DS** s’excluent mutuellement et ne peuvent pas être combinées avec d’autres options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3dc90-247">The **-da**, **-do**, **-dx**, and **-ds** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set"></a><span data-ttu-id="3dc90-248">Rupture d’un jeu de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="3dc90-248">Breaking a Shadow Copy Set</span></span>

<span data-ttu-id="3dc90-249">**vshadow** **-b =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="3dc90-249">**vshadow** **-b=**_ShadowCopySetId_</span></span>

<span data-ttu-id="3dc90-250">**vshadow** **-BW =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="3dc90-250">**vshadow** **-bw=**_ShadowCopySetId_</span></span>

<span data-ttu-id="3dc90-251">L’option de ligne de commande **-b =**_ShadowCopySetId_ convertit chaque cliché instantané dans le jeu de clichés instantanés en un volume en lecture seule autonome.</span><span class="sxs-lookup"><span data-stu-id="3dc90-251">The **-b=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone read-only volume.</span></span>

<span data-ttu-id="3dc90-252">L’option de ligne de commande **-BW =**_ShadowCopySetId_ convertit chaque cliché instantané dans le jeu de clichés instantanés en un volume inscriptible autonome.</span><span class="sxs-lookup"><span data-stu-id="3dc90-252">The **-bw=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone writable volume.</span></span>

> [!Note]  
> <span data-ttu-id="3dc90-253">Les options de ligne de commande **-b** et **-BW** sont uniquement prises en charge sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-253">The **-b** and **-bw** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="3dc90-254">Pour plus d’informations sur l’arrêt d’un jeu de clichés instantanés, consultez [interruption des clichés instantanés](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="3dc90-254">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

<span data-ttu-id="3dc90-255">Une fois le jeu de clichés instantanés rompu, le jeu de clichés instantanés et les clichés instantanés individuels n’existent plus et ne peuvent pas être gérés à l’aide de commandes VSS.</span><span class="sxs-lookup"><span data-stu-id="3dc90-255">After the shadow copy set is broken, the shadow copy set and the individual shadow copies no longer exist and cannot be managed using VSS commands.</span></span>

<span data-ttu-id="3dc90-256">Un jeu de clichés instantanés est persistant s’il a été créé avec l’indicateur **-p** facultatif.</span><span class="sxs-lookup"><span data-stu-id="3dc90-256">A shadow copy set is persistent if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="3dc90-257">Si le jeu de clichés instantanés transportable n’est pas persistant, il apparaît pendant une brève période pendant l’exécution de la commande de création de clichés instantanés, et est automatiquement supprimé lorsque la commande retourne.</span><span class="sxs-lookup"><span data-stu-id="3dc90-257">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="3dc90-258">Vous pouvez arrêter les jeux de clichés instantanés non persistants uniquement lors de la création de clichés instantanés, en créant le jeu de clichés instantanés à l’aide de l’indicateur facultatif **-Exec** pour exécuter un fichier cmd qui appelle **vshadow** **-b** ou **vshadow** **-BW**.</span><span class="sxs-lookup"><span data-stu-id="3dc90-258">You can break nonpersistent shadow copy sets only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls **vshadow** **-b** or **vshadow** **-bw**.</span></span>

<span data-ttu-id="3dc90-259">Les options de ligne de commande **-b** et **-BW** s’excluent mutuellement et ne peuvent pas être combinées avec d’autres options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3dc90-259">The **-b** and **-bw** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="3dc90-260">Rupture d’un jeu de clichés instantanés à l’aide de la méthode BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="3dc90-260">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="3dc90-261">**vshadow** **-Bex**</span><span class="sxs-lookup"><span data-stu-id="3dc90-261">**vshadow** **-bex**</span></span>

<span data-ttu-id="3dc90-262">L’option de ligne de commande **-Bex** divise un jeu de clichés instantanés selon les options spécifiées par les indicateurs facultatifs **-Mask**, **-RW**, **-forcerevert** et **-Revert** .</span><span class="sxs-lookup"><span data-stu-id="3dc90-262">The **-bex** command-line option breaks a shadow copy set according to the options specified by the optional **-mask**, **-rw**, **-forcerevert**, and **-norevert** flags.</span></span> <span data-ttu-id="3dc90-263">Cette option de ligne de commande est similaire aux options de ligne de commande **-b** et **-BW** .</span><span class="sxs-lookup"><span data-stu-id="3dc90-263">This command-line option is similar to the **-b** and **-bw** command-line options.</span></span> <span data-ttu-id="3dc90-264">L’option de ligne de commande **-Bex** utilise la méthode [**IVssBackupComponentsEx2 :: BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) , tandis que les options de ligne de commande- **b** et **-BW** utilisent la méthode [**IVssBackupComponents :: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .</span><span class="sxs-lookup"><span data-stu-id="3dc90-264">The **-bex** command-line option uses the [**IVssBackupComponentsEx2::BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) method, whereas the **-b** and **-bw** command-line options use the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>

<span data-ttu-id="3dc90-265">Pour plus d’informations sur l’arrêt d’un jeu de clichés instantanés, consultez [interruption des clichés instantanés](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="3dc90-265">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

> [!Note]  
> <span data-ttu-id="3dc90-266">L’option de ligne de commande **-Bex** est prise en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-266">The **-bex** command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="3dc90-267">**vshadow** **-Bex** **-Mask**</span><span class="sxs-lookup"><span data-stu-id="3dc90-267">**vshadow** **-bex** **-mask**</span></span>

<span data-ttu-id="3dc90-268">L’indicateur **-Mask** spécifie que le numéro d’unité logique de cliché instantané sera masqué de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="3dc90-268">The **-mask** flag specifies that the shadow copy LUN will be masked from the host.</span></span> <span data-ttu-id="3dc90-269">Si l’indicateur **-Mask** est spécifié, les indicateurs **-RW**, **-forcerevert** et **-Revert** ne peuvent pas être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="3dc90-269">If the **-mask** flag is specified, the **-rw**, **-forcerevert**, and **-norevert** flags cannot be specified.</span></span>

<span data-ttu-id="3dc90-270">**vshadow** **-Bex** **-RW**</span><span class="sxs-lookup"><span data-stu-id="3dc90-270">**vshadow** **-bex** **-rw**</span></span>

<span data-ttu-id="3dc90-271">L’indicateur **-RW** spécifie que le numéro d’unité logique de cliché instantané sera exposé à l’hôte en tant que volume en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3dc90-271">The **-rw** flag specifies that the shadow copy LUN will be exposed to the host as a read/write volume.</span></span>

<span data-ttu-id="3dc90-272">**vshadow** **-Bex** **-forcerevert**</span><span class="sxs-lookup"><span data-stu-id="3dc90-272">**vshadow** **-bex** **-forcerevert**</span></span>

<span data-ttu-id="3dc90-273">L’indicateur **-forcerevert** spécifie que les identificateurs de disque de tous les numéros d’unités logiques de cliché instantané seront restaurés sur ceux des numéros d’unités logiques d’origine.</span><span class="sxs-lookup"><span data-stu-id="3dc90-273">The **-forcerevert** flag specifies that the disk identifiers of all of the shadow copy LUNs will be reverted to that of the original LUNs.</span></span> <span data-ttu-id="3dc90-274">Toutefois, si l’un des numéros d’unités logiques d’origine est présent sur le système, l’opération échoue et aucun des identificateurs n’est rétabli.</span><span class="sxs-lookup"><span data-stu-id="3dc90-274">However, if any of the original LUNs are present on the system, the operation will fail and none of the identifiers will be reverted.</span></span> <span data-ttu-id="3dc90-275">Cet indicateur et l’indicateur **-Revert** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="3dc90-275">This flag and the **-norevert** flag are mutually exclusive.</span></span>

<span data-ttu-id="3dc90-276">**vshadow** **-Bex** **-Revert**</span><span class="sxs-lookup"><span data-stu-id="3dc90-276">**vshadow** **-bex** **-norevert**</span></span>

<span data-ttu-id="3dc90-277">L’indicateur **-Revert** indique qu’aucun identificateur de disque LUN de cliché instantané ne sera rétabli.</span><span class="sxs-lookup"><span data-stu-id="3dc90-277">The **-norevert** flag specifies that none of the shadow copy LUN disk identifiers will be reverted.</span></span> <span data-ttu-id="3dc90-278">Cet indicateur et l’indicateur **-forcerevert** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="3dc90-278">This flag and the **-forcerevert** flag are mutually exclusive.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="3dc90-279">Exposition locale d’un cliché instantané</span><span class="sxs-lookup"><span data-stu-id="3dc90-279">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="3dc90-280">**vshadow** **-El =**_ShadowCopyId_*_,_*_LocalEmptyDirectory_</span><span class="sxs-lookup"><span data-stu-id="3dc90-280">**vshadow** **-el=**_ShadowCopyId_*_,_*_LocalEmptyDirectory_</span></span>

 <span data-ttu-id="3dc90-281">**vshadow** **-El =**_ShadowCopyId_*_,_*_UnusedDriveLetter_</span><span class="sxs-lookup"><span data-stu-id="3dc90-281">**vshadow** **-el=**_ShadowCopyId_*_,_*_UnusedDriveLetter_</span></span>

<span data-ttu-id="3dc90-282">L’option de ligne de commande **-El** affecte un dossier monté ou une lettre de lecteur à un cliché instantané persistant.</span><span class="sxs-lookup"><span data-stu-id="3dc90-282">The **-el** command-line option assigns a mounted folder or a drive letter to a persistent shadow copy.</span></span> <span data-ttu-id="3dc90-283">Notez que le contenu du volume restera en lecture seule à moins que vous n’appeliez par la suite **vshadow** **-BW** pour rompre le jeu de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="3dc90-283">Note that the volume contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="3dc90-284">Les clichés instantanés non persistants et les [*clichés instantanés accessibles par le client*](vssgloss-c.md) ne peuvent pas être exposés localement.</span><span class="sxs-lookup"><span data-stu-id="3dc90-284">Nonpersistent shadow copies and [*client-accessible shadow copies*](vssgloss-c.md) cannot be exposed locally.</span></span>

 

<span data-ttu-id="3dc90-285">Par exemple, si {edbed95e-7e8d-11D8-9D01-505054503030} est le GUID d’un cliché instantané persistant existant et X : est une lettre de lecteur inutilisée, la commande suivante expose le cliché instantané sous X :</span><span class="sxs-lookup"><span data-stu-id="3dc90-285">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and X: is an unused drive letter, the following command exposes the shadow copy under X:</span></span>

<span data-ttu-id="3dc90-286">**vshadow** **-El = {edbed95e-7e8d-11D8-9D01-505054503030}, x :**</span><span class="sxs-lookup"><span data-stu-id="3dc90-286">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},x:**</span></span>

<span data-ttu-id="3dc90-287">L’exemple suivant montre comment exposer le même cliché instantané sous le dossier monté C : \\ ShadowCopies \\ June23 :</span><span class="sxs-lookup"><span data-stu-id="3dc90-287">The following example shows how to expose the same shadow copy under the mounted folder C:\\ShadowCopies\\June23:</span></span>

<span data-ttu-id="3dc90-288">**mkdir c : \\ ShadowCopies \\ June23**</span><span class="sxs-lookup"><span data-stu-id="3dc90-288">**mkdir c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="3dc90-289">**vshadow** **-El = {edbed95e-7e8d-11D8-9D01-505054503030}, c : \\ ShadowCopies \\ June23**</span><span class="sxs-lookup"><span data-stu-id="3dc90-289">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="3dc90-290">L’option de ligne de commande **-El** ne peut pas être combinée avec d’autres options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3dc90-290">The **-el** command-line option cannot be combined with other command-line options.</span></span>

## <a name="exposing-a-shadow-copy-remotely"></a><span data-ttu-id="3dc90-291">Exposition à distance d’un cliché instantané</span><span class="sxs-lookup"><span data-stu-id="3dc90-291">Exposing a Shadow Copy Remotely</span></span>

<span data-ttu-id="3dc90-292">**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_</span><span class="sxs-lookup"><span data-stu-id="3dc90-292">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_</span></span>

 <span data-ttu-id="3dc90-293">**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_</span><span class="sxs-lookup"><span data-stu-id="3dc90-293">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_</span></span>

<span data-ttu-id="3dc90-294">L’option de ligne de commande **-er** assigne un nom de partage en lecture seule au répertoire racine (ou à un sous-répertoire) à partir du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="3dc90-294">The **-er** command-line option assigns a read-only share name to the root directory (or a subdirectory) from the shadow copy.</span></span> <span data-ttu-id="3dc90-295">Notez que le contenu du partage restera en lecture seule à moins que vous n’appeliez par la suite **vshadow** **-BW** pour rompre le jeu de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="3dc90-295">Note that the share contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="3dc90-296">[*Les clichés instantanés accessibles par le client*](vssgloss-c.md) ne peuvent pas être exposés à distance.</span><span class="sxs-lookup"><span data-stu-id="3dc90-296">[*Client-accessible shadow copies*](vssgloss-c.md) cannot be exposed remotely.</span></span>

 

<span data-ttu-id="3dc90-297">Par exemple, si {edbed95e-7e8d-11D8-9D01-505054503030} est le GUID d’un cliché instantané persistant existant et que \_ le partage 123 est un nom de partage inutilisé, la commande suivante expose le cliché instantané sous le partage \_ 123 :</span><span class="sxs-lookup"><span data-stu-id="3dc90-297">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and share\_123 is an unused share name, the following command exposes the shadow copy under share\_123:</span></span>

<span data-ttu-id="3dc90-298">**vshadow** **-er = {edbed95e-7e8d-11D8-9D01-505054503030}, partage \_ 123**</span><span class="sxs-lookup"><span data-stu-id="3dc90-298">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123**</span></span>

<span data-ttu-id="3dc90-299">L’exemple suivant montre comment exposer uniquement une sous-arborescence (nommée « dossier1 \\ dossier2 ») du même cliché instantané sous le même partage :</span><span class="sxs-lookup"><span data-stu-id="3dc90-299">The following example shows how to expose only a subtree (named "Folder1\\Folder2") of the same shadow copy under the same share:</span></span>

<span data-ttu-id="3dc90-300">**vshadow** **-er = {edbed95e-7e8d-11D8-9D01-505054503030}, partage \_ 123, dossier1 \\ dossier2**</span><span class="sxs-lookup"><span data-stu-id="3dc90-300">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123,Folder1\\Folder2**</span></span>

<span data-ttu-id="3dc90-301">L’option de ligne de commande **-er** ne peut pas être combinée avec d’autres options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3dc90-301">The **-er** command-line option cannot be combined with other command-line options.</span></span>

## <a name="listing-writer-status-and-metadata"></a><span data-ttu-id="3dc90-302">Affichage de l’État et des métadonnées de l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="3dc90-302">Listing Writer Status and Metadata</span></span>

<span data-ttu-id="3dc90-303">**vshadow** **-WS**</span><span class="sxs-lookup"><span data-stu-id="3dc90-303">**vshadow** **-ws**</span></span>

<span data-ttu-id="3dc90-304">**vshadow** **-WM**</span><span class="sxs-lookup"><span data-stu-id="3dc90-304">**vshadow** **-wm**</span></span>

<span data-ttu-id="3dc90-305">**vshadow** **-wm2**</span><span class="sxs-lookup"><span data-stu-id="3dc90-305">**vshadow** **-wm2**</span></span>

<span data-ttu-id="3dc90-306">**vshadow** **-WM3**</span><span class="sxs-lookup"><span data-stu-id="3dc90-306">**vshadow** **-wm3**</span></span>

<span data-ttu-id="3dc90-307">L’option de ligne **de commande-WS** énumère les enregistreurs VSS en cours d’exécution sur l’ordinateur et décrit leur état.</span><span class="sxs-lookup"><span data-stu-id="3dc90-307">The **-ws** command-line option enumerates the VSS writers that are currently running on the computer and describes their state.</span></span> <span data-ttu-id="3dc90-308">Cette commande est l’équivalent de la commande [vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="3dc90-308">This command is the equivalent of the [Vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) command.</span></span> <span data-ttu-id="3dc90-309">Il existe six valeurs d’État possibles : stable, échec, inconnu, en attente de gel, figé et en attente de la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3dc90-309">There are six possible state values: Stable, Failed, Unknown, Waiting for freeze, Frozen, and Waiting for completion.</span></span>

<span data-ttu-id="3dc90-310">L’option de ligne de commande **-WM** répertorie un résumé des métadonnées de l’enregistreur, y compris les volumes affectés.</span><span class="sxs-lookup"><span data-stu-id="3dc90-310">The **-wm** command-line option lists a summary of the writer metadata, including the affected volumes.</span></span>

<span data-ttu-id="3dc90-311">L’option de ligne de commande **-wm2** répertorie toutes les métadonnées de l’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="3dc90-311">The **-wm2** command-line option lists all writer metadata.</span></span>

<span data-ttu-id="3dc90-312">L’option de ligne de commande **-WM3** répertorie toutes les métadonnées de l’enregistreur au format XML brut.</span><span class="sxs-lookup"><span data-stu-id="3dc90-312">The **-wm3** command-line option lists all writer metadata in raw XML format.</span></span>

<span data-ttu-id="3dc90-313">**Windows Vista et Windows Server 2003 :** L’option de ligne de commande **-WM3** n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="3dc90-313">**Windows Vista and Windows Server 2003:** The **-wm3** command-line option is not supported.</span></span>

<span data-ttu-id="3dc90-314">Vous pouvez utiliser ces informations pour déterminer les volumes à inclure dans le jeu de clichés instantanés de volume.</span><span class="sxs-lookup"><span data-stu-id="3dc90-314">You can use this information to determine which volumes to include in the volume shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="3dc90-315">Si l’état du writer est stable ou en attente de la fin de l’exécution, le writer peut être considéré comme étant dans un état stable, prêt pour la sauvegarde suivante.</span><span class="sxs-lookup"><span data-stu-id="3dc90-315">If the writer state is Stable or Waiting for completion, the writer can be considered to be in a stable state, ready for the next backup.</span></span>

 

<span data-ttu-id="3dc90-316">Les options de ligne de commande **-WS**, **-WM**, **-wm2** et **-WM3** s’excluent mutuellement et ne peuvent pas être combinées avec d’autres options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3dc90-316">The **-ws**, **-wm**, **-wm2**, and **-wm3** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="performing-restore-operations"></a><span data-ttu-id="3dc90-317">Exécution d’opérations de restauration</span><span class="sxs-lookup"><span data-stu-id="3dc90-317">Performing Restore Operations</span></span>

<span data-ttu-id="3dc90-318">**vshadow** \[ OptionalFlags \] **-r =**_file_*_. xml_*</span><span class="sxs-lookup"><span data-stu-id="3dc90-318">**vshadow** \[OptionalFlags\] **-r=**_File_*_.xml_*</span></span>

<span data-ttu-id="3dc90-319">**vshadow** \[ OptionalFlags \] **-RS =**_file_*_. xml_*</span><span class="sxs-lookup"><span data-stu-id="3dc90-319">**vshadow** \[OptionalFlags\] **-rs=**_File_*_.xml_*</span></span>

<span data-ttu-id="3dc90-320">L’option de ligne **de commande-r** effectue une opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="3dc90-320">The **-r** command-line option performs a restore operation.</span></span>

<span data-ttu-id="3dc90-321">L’option de ligne **de commande-RS** effectue une opération de restauration simulée.</span><span class="sxs-lookup"><span data-stu-id="3dc90-321">The **-rs** command-line option performs a simulated restore operation.</span></span>

<span data-ttu-id="3dc90-322">Le fichier de *File.xml* doit être un fichier de document de composants de sauvegarde pour un jeu de clichés instantanés qui a été créé avec l’indicateur facultatif **-t** ou **-BC** .</span><span class="sxs-lookup"><span data-stu-id="3dc90-322">The *File.xml* file must be a Backup Components Document file for a shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="3dc90-323">Les options de ligne de commande **-r** et **-RS** s’excluent mutuellement et ne peuvent pas être combinées avec d’autres options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3dc90-323">The **-r** and **-rs** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

<span data-ttu-id="3dc90-324">*OptionalFlags* est un masque de transparence des valeurs d’indicateur facultatives du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3dc90-324">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="3dc90-325">Valeur d’indicateur facultative</span><span class="sxs-lookup"><span data-stu-id="3dc90-325">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="3dc90-326">Description</span><span class="sxs-lookup"><span data-stu-id="3dc90-326">Description</span></span>                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc90-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-Wi =**_enregistreur_</span><span class="sxs-lookup"><span data-stu-id="3dc90-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi=**_Writer_</span></span><br/>             | <span data-ttu-id="3dc90-328">Cet indicateur facultatif vérifie que l’enregistreur ou le composant spécifié est inclus dans la restauration.</span><span class="sxs-lookup"><span data-stu-id="3dc90-328">This optional flag verifies that the specified writer or component is included in the restore.</span></span> <span data-ttu-id="3dc90-329">L' *enregistreur* peut spécifier un chemin d’accès de composant, un nom d’enregistreur, un ID d’enregistreur ou un ID d’instance d’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="3dc90-329">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                    |
| <span data-ttu-id="3dc90-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-WX =**_enregistreur_</span><span class="sxs-lookup"><span data-stu-id="3dc90-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx=**_Writer_</span></span><br/>             | <span data-ttu-id="3dc90-331">Cet indicateur facultatif vérifie que l’enregistreur ou le composant spécifié est exclu de la restauration.</span><span class="sxs-lookup"><span data-stu-id="3dc90-331">This optional flag verifies that the specified writer or component is excluded from the restore.</span></span> <span data-ttu-id="3dc90-332">L' *enregistreur* peut spécifier un chemin d’accès de composant, un nom d’enregistreur, un ID d’enregistreur ou un ID d’instance d’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="3dc90-332">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="3dc90-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-Exec =,**_commande_</span><span class="sxs-lookup"><span data-stu-id="3dc90-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="3dc90-334">Cet indicateur facultatif exécute une commande ou un script entre les événements antérieurs et postérieurs à la restauration qui sont envoyés aux enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="3dc90-334">This optional flag executes a command or script between the pre-restore and post-restore events that are sent to the writers.</span></span> <span data-ttu-id="3dc90-335">La *commande* peut spécifier une commande d’interpréteur de commandes exécutable ou un fichier cmd.</span><span class="sxs-lookup"><span data-stu-id="3dc90-335">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="3dc90-336">Si elle spécifie une commande d’interpréteur de commandes, aucun paramètre de commande ne peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="3dc90-336">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="3dc90-337"><span id="-tracing"></span><span id="-TRACING"></span>**-suivi**</span><span class="sxs-lookup"><span data-stu-id="3dc90-337"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="3dc90-338">Cet indicateur facultatif génère une sortie détaillée qui peut être utilisée pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="3dc90-338">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a><span data-ttu-id="3dc90-339">Retour à un cliché instantané précédent</span><span class="sxs-lookup"><span data-stu-id="3dc90-339">Reverting to a Previous Shadow Copy</span></span>

<span data-ttu-id="3dc90-340">**vshadow** **-Revert =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="3dc90-340">**vshadow** **-revert=**_ShadowCopyId_</span></span>

> [!Note]  
> <span data-ttu-id="3dc90-341">Cette option de ligne de commande est prise en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-341">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="3dc90-342">**Windows server 2008 et Windows server 2003 :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3dc90-342">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="3dc90-343">L’option de ligne de commande **-Revert** retourne un volume au cliché instantané précédent dont l’ID est spécifié par *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="3dc90-343">The **-revert** command-line option reverts a volume to the previous shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="3dc90-344">L’option de ligne de commande **-Revert** ne peut pas être combinée avec d’autres options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3dc90-344">The **-revert** command-line option cannot be combined with other command-line options.</span></span>

## <a name="resynchronizing-luns"></a><span data-ttu-id="3dc90-345">Resynchronisation des numéros d’unités logiques</span><span class="sxs-lookup"><span data-stu-id="3dc90-345">Resynchronizing LUNs</span></span>

<span data-ttu-id="3dc90-346">**vshadow** **-addresync =**_ShadowCopyId_ **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]</span><span class="sxs-lookup"><span data-stu-id="3dc90-346">**vshadow** **-addresync=**_ShadowCopyId_ **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="3dc90-347">**vshadow** **-addresync =**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]</span><span class="sxs-lookup"><span data-stu-id="3dc90-347">**vshadow** **-addresync=**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="3dc90-348">L’option de ligne de commande **-addresync** spécifie les volumes à inclure dans une opération de resynchronisation des numéros d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="3dc90-348">The **-addresync** command-line option specifies the volumes to be included in a LUN resynchronization operation.</span></span> <span data-ttu-id="3dc90-349">Le paramètre *ShadowCopyId* spécifie l’identificateur du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="3dc90-349">The *ShadowCopyId* parameter specifies the identifier of the shadow copy.</span></span> <span data-ttu-id="3dc90-350">Le paramètre facultatif *TargetVolumeDriveLetter* spécifie le volume de destination dans lequel le contenu du volume de clichés instantanés doit être copié.</span><span class="sxs-lookup"><span data-stu-id="3dc90-350">The optional *TargetVolumeDriveLetter* parameter specifies the destination volume where the contents of the shadow copy volume are to be copied.</span></span>

<span data-ttu-id="3dc90-351">L’option de ligne de commande **-Resync** lance une opération de resynchronisation des numéros d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="3dc90-351">The **-resync** command-line option initiates a LUN resynchronization operation.</span></span> <span data-ttu-id="3dc90-352">Une fois l’opération terminée, la signature de chaque LUN cible doit être identique à celle du numéro d’unité logique du volume cible.</span><span class="sxs-lookup"><span data-stu-id="3dc90-352">After the operation is complete, the signature of each target LUN should be identical to that of the target volume LUN.</span></span> <span data-ttu-id="3dc90-353">Le paramètre *BCDFileName* spécifie le nom du fichier XML qui contient le document du composant de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="3dc90-353">The *BCDFileName* parameter specifies the name of the XML file that contains the Backup Component Document.</span></span>

> [!Note]  
> <span data-ttu-id="3dc90-354">Les options de ligne de commande **-addresync** et **-Resync** sont uniquement prises en charge sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-354">The **-addresync** and **-resync** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="3dc90-355">**Windows server 2008 et Windows server 2003 :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3dc90-355">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="3dc90-356">*OptionalResyncFlags* est un masque de transparence des valeurs d’indicateur facultatives du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3dc90-356">*OptionalResyncFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3dc90-357">Valeur d’indicateur facultative</span><span class="sxs-lookup"><span data-stu-id="3dc90-357">Optional flag value</span></span></th>
<th><span data-ttu-id="3dc90-358">Description</span><span class="sxs-lookup"><span data-stu-id="3dc90-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3dc90-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-360">Cet indicateur facultatif spécifie qu’une fois l’opération terminée, la signature de chaque LUN cible doit être identique à celle du numéro d’unité logique d’origine qui a été utilisé pour créer le cliché instantané, et non le numéro d’unité logique du volume cible.</span><span class="sxs-lookup"><span data-stu-id="3dc90-360">This optional flag specifies that after the operation is complete, the signature of each target LUN should be identical to that of the original LUN that was used to create the shadow copy, not the target volume LUN.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-361">L’indicateur <strong>-revertsig</strong> est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-361">The <strong>-revertsig</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3dc90-362"><strong>Windows server 2008 et Windows server 2003 :</strong> Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3dc90-362"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc90-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span><span class="sxs-lookup"><span data-stu-id="3dc90-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span></span><br/></td>
<td><span data-ttu-id="3dc90-364">Cet indicateur facultatif spécifie que le service VSS ne doit pas vérifier les volumes non sélectionnés qui seraient remplacés par l’opération de resynchronisation des LUN.</span><span class="sxs-lookup"><span data-stu-id="3dc90-364">This optional flag specifies that the VSS service should not check for unselected volumes that would be overwritten by the LUN resynchronization operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3dc90-365">L’indicateur <strong>-novolcheck</strong> est pris en charge uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3dc90-365">The <strong>-novolcheck</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="3dc90-366"><strong>Windows server 2008 et Windows server 2003 :</strong> Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3dc90-366"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 
