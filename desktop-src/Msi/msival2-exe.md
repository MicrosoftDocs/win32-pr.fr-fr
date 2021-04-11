---
description: Msival2.exe est un utilitaire de ligne de commande qui peut exécuter une suite d’évaluateurs de cohérence internes (ICEs).
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210779"
---
# <a name="msival2exe"></a><span data-ttu-id="ea745-103">Msival2.exe</span><span class="sxs-lookup"><span data-stu-id="ea745-103">Msival2.exe</span></span>

<span data-ttu-id="ea745-104">Msival2.exe est un utilitaire de ligne de commande qui peut exécuter une suite d' [évaluateurs de cohérence internes (ICEs)](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="ea745-104">Msival2.exe is a command line utility that can run a suite of [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="ea745-105">Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="ea745-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="ea745-106">Pour plus d’informations sur le fichier ICEs et le fichier CUB, consultez [utilisation des évaluateurs de cohérence internes](using-internal-consistency-evaluators.md).</span><span class="sxs-lookup"><span data-stu-id="ea745-106">For more information about ICEs and the CUB file, see [Using Internal Consistency Evaluators](using-internal-consistency-evaluators.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ea745-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea745-107">Syntax</span></span>

<span data-ttu-id="ea745-108">**MSIVal2** *{Database} {fichier CUB} \[ -f \] \[ -l {logfile} \] \[ -i {Ice ID} \[ : {Ice ID}... \] \]*</span><span class="sxs-lookup"><span data-stu-id="ea745-108">**Msival2** *{database}{CUB file}\[-f\]\[-l {logfile}\]\[-i {ICE Id}\[:{ICE Id}...\]\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="ea745-109">Options de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="ea745-109">Command Line Options</span></span>

<span data-ttu-id="ea745-110">Msival2.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="ea745-110">Msival2.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="ea745-111">Un séparateur de barre oblique peut également être utilisé à la place d’un tiret.</span><span class="sxs-lookup"><span data-stu-id="ea745-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="ea745-112">Option</span><span class="sxs-lookup"><span data-stu-id="ea745-112">Option</span></span> | <span data-ttu-id="ea745-113">Description</span><span class="sxs-lookup"><span data-stu-id="ea745-113">Description</span></span>                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea745-114">-f</span><span class="sxs-lookup"><span data-stu-id="ea745-114">-f</span></span>     | <span data-ttu-id="ea745-115">Filtrez tous les messages d’information à partir des résultats affichés.</span><span class="sxs-lookup"><span data-stu-id="ea745-115">Filter out all informational messages from the displayed results.</span></span> <span data-ttu-id="ea745-116">Tous les autres types de messages s’affichent.</span><span class="sxs-lookup"><span data-stu-id="ea745-116">All other types of messages are displayed.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="ea745-117">-i</span><span class="sxs-lookup"><span data-stu-id="ea745-117">-i</span></span>     | <span data-ttu-id="ea745-118">Exécutez uniquement le CIEM indiqué sur la ligne de commande dans l’ordre spécifié.</span><span class="sxs-lookup"><span data-stu-id="ea745-118">Run only the ICEs listed on the command line in the order specified.</span></span> <span data-ttu-id="ea745-119">Chaque action personnalisée ICE doit être indiquée telle qu’elle apparaît dans la [table CustomAction](customaction-table.md) du fichier CUB.</span><span class="sxs-lookup"><span data-stu-id="ea745-119">Each ICE custom action should be listed as it appears in the [CustomAction table](customaction-table.md) of the CUB file.</span></span> <span data-ttu-id="ea745-120">Si cette option est omise, l’outil exécute l’ensemble par défaut du CIEM spécifié par l’auteur du fichier CUB.</span><span class="sxs-lookup"><span data-stu-id="ea745-120">If this option is omitted, the tool runs the default set of ICEs specified by the author of the CUB file.</span></span> |
| <span data-ttu-id="ea745-121">-l</span><span class="sxs-lookup"><span data-stu-id="ea745-121">-l</span></span>     | <span data-ttu-id="ea745-122">Écrit les résultats dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="ea745-122">Write results to the specified file.</span></span> <span data-ttu-id="ea745-123">Le fichier ne doit pas déjà exister.</span><span class="sxs-lookup"><span data-stu-id="ea745-123">The file must not already exist.</span></span> <span data-ttu-id="ea745-124">Si le fichier existe, il n’est pas remplacé.</span><span class="sxs-lookup"><span data-stu-id="ea745-124">If the file exists, it is not overwritten.</span></span>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="ea745-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea745-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea745-126">Outils de développement Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ea745-126">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="ea745-127">Évaluateurs de cohérence internes-CIEM</span><span class="sxs-lookup"><span data-stu-id="ea745-127">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
</dt> <dt>

[<span data-ttu-id="ea745-128">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="ea745-128">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



