---
description: Lorsqu’une opération de sauvegarde VSS est effectuée sans implication d’un enregistreur, la création de clichés instantanés peut encore se produire.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Sauvegardes sans participation au rédacteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a782fbcb9afe532f2f123151dc7998307157b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526966"
---
# <a name="backups-without-writer-participation"></a><span data-ttu-id="f3863-103">Sauvegardes sans participation au rédacteur</span><span class="sxs-lookup"><span data-stu-id="f3863-103">Backups without Writer Participation</span></span>

<span data-ttu-id="f3863-104">Lorsqu’une opération de sauvegarde VSS est effectuée sans implication d’un enregistreur, la création de clichés instantanés peut encore se produire.</span><span class="sxs-lookup"><span data-stu-id="f3863-104">When a VSS backup operation is conducted without the involvement of a writer, the shadow copy creation can still occur.</span></span>

<span data-ttu-id="f3863-105">Comme indiqué ailleurs (voir [État de cliché instantané par défaut](shadow-copies-and-shadow-copy-sets.md)), le résultat de ce type de cliché instantané est un volume qui reflète l’état d’un disque au moment du cliché instantané : les données sur le volume copié par cliché instantané peuvent refléter des opérations d’e/s incomplètes ou partielles et sont décrites comme étant dans un [*État de cohérence*](vssgloss-c.md)en cas d’incident.</span><span class="sxs-lookup"><span data-stu-id="f3863-105">As noted elsewhere (see [Default Shadow Copy State](shadow-copies-and-shadow-copy-sets.md)), the result of this type of shadow copy is a volume reflecting the state of a disk at the time of the shadow copy: data on the shadow-copied volume may reflect incomplete or partial I/O operations and is described as being in a [*crash-consistent state*](vssgloss-c.md).</span></span>

<span data-ttu-id="f3863-106">Il existe plusieurs situations qui nécessitent une application de sauvegarde pour fonctionner avec des données de clichés instantanés cohérentes en cas d’incident :</span><span class="sxs-lookup"><span data-stu-id="f3863-106">There are several situations that will require a backup application to work with crash consistent shadow copied data:</span></span>

-   <span data-ttu-id="f3863-107">**Les données sont gérées par des applications qui ne prennent pas en charge VSS**</span><span class="sxs-lookup"><span data-stu-id="f3863-107">**Data is managed by VSS-unaware applications**</span></span>

    <span data-ttu-id="f3863-108">Presque tous les systèmes disposent de certaines applications, telles que les éditeurs de texte, les lecteurs de messagerie, les traitements de texte, etc., qui ne sont pas compatibles avec VSS. il est donc toujours probable que certaines des données d’un cliché instantané devront être considérées comme étant dans un état de cohérence d’incident.</span><span class="sxs-lookup"><span data-stu-id="f3863-108">Almost every system will have some applications—text editors, mail readers, word processors, and so forth—that are VSS unaware, so it is always likely that some of the data on a shadow copy will need to be thought of as being in a crash consistent state.</span></span>

    <span data-ttu-id="f3863-109">Ce type de données n’étant généralement pas critique dans le système ou le service, la sauvegarde ne doit pas être problématique, ou au moins plus problématiques que lors d’une sauvegarde conventionnelle.</span><span class="sxs-lookup"><span data-stu-id="f3863-109">This sort of data is not typically system- or service-critical, so backing it up should not be problematic, or at least no more problematic than during a conventional backup.</span></span>

    <span data-ttu-id="f3863-110">Comme avec les préparations pour les sauvegardes conventionnelles, si possible, les opérateurs de sauvegarde doivent tenter d’interrompre ou de mettre fin à ces applications avant de démarrer un travail de sauvegarde VSS.</span><span class="sxs-lookup"><span data-stu-id="f3863-110">As with preparations for conventional backups, if possible, backup operators should attempt to suspend or terminate such applications prior to starting a VSS backup job.</span></span>

-   <span data-ttu-id="f3863-111">**Système sans Writers compatibles VSS**</span><span class="sxs-lookup"><span data-stu-id="f3863-111">**System with no VSS-compatible writers**</span></span>

    <span data-ttu-id="f3863-112">Cette situation peut être relativement rare, car la plupart des systèmes qui peuvent être sauvegardés par une application de sauvegarde VSS auront une version de Windows compatible avec VSS, qui doit contenir des enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="f3863-112">This situation may be relatively rare because most systems that can be backed up by a VSS backup application will have a VSS-enabled version of Windows, which should contain writers.</span></span>

    <span data-ttu-id="f3863-113">Toutefois, dans certains cas, ce problème peut survenir : par exemple, si vous sauvegardez un système sans la prise en charge de VSS, mais que le système utilise une appliance en réseau compatible VSS pour son stockage.</span><span class="sxs-lookup"><span data-stu-id="f3863-113">However, there are certain circumstances where this problem could arise—for instance, if you are backing up a system without VSS support but the system uses a VSS-enabled networked appliance for its storage.</span></span>

    <span data-ttu-id="f3863-114">Bien que la sauvegarde de l’état d’un système à partir d’une image cohérente en cas d’incident ne soit pas optimale, il peut suffire qu’un ordinateur redémarre à un état opérationnel.</span><span class="sxs-lookup"><span data-stu-id="f3863-114">Although backing up a system's state from a crash-consistent image is not optimal, it may be sufficient for a computer to reboot to an operational status.</span></span> <span data-ttu-id="f3863-115">Dans de nombreux cas, l’ordinateur récupère les opérations d’e/s incomplètes dans les systèmes de fichiers et fonctionne normalement.</span><span class="sxs-lookup"><span data-stu-id="f3863-115">In many cases, the computer will recover from any incomplete I/O operations to the file systems and will operate normally.</span></span>

-   <span data-ttu-id="f3863-116">**Un demandeur choisit de ne pas travailler avec les enregistreurs système**</span><span class="sxs-lookup"><span data-stu-id="f3863-116">**A requester choosing not to work with the system writers**</span></span>

    <span data-ttu-id="f3863-117">Cette situation se produit si un demandeur a choisi d’ajouter des composants d’écriture ou de désactiver tous les enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="f3863-117">This circumstance would occur if a requester chose to add no writer components, or disabling all writers.</span></span>

    <span data-ttu-id="f3863-118">L’exécution de sauvegardes de cette manière est généralement déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f3863-118">Performing backups in this way is generally discouraged.</span></span> <span data-ttu-id="f3863-119">Bien que le volume cliché instantané à sauvegarder puisse être suffisant pour restaurer un système en cours d’exécution, il n’est pas souhaitable.</span><span class="sxs-lookup"><span data-stu-id="f3863-119">Although the shadow-copied volume to back up might be sufficient to restore a system to running, it is not desirable.</span></span> <span data-ttu-id="f3863-120">En fait, étant donné que les writers qui s’exécutent sur le système sont conçus avec des fonctionnalités permettant de coopérer avec VSS et les clichés instantanés, la sauvegarde de leurs données de cette manière peut entraîner une instabilité.</span><span class="sxs-lookup"><span data-stu-id="f3863-120">In fact, given that the writers running on the system are designed with functionality to cooperate with VSS and shadow copies, backing up their data in this way might result in instability.</span></span>

 

 



