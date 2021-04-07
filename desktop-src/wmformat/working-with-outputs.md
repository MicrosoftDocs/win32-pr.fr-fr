---
title: Utilisation des sorties
description: Utilisation des sorties
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows Media Format SDK, utilisation des sorties
- ASF (Advanced Systems Format), utilisation des sorties
- ASF (format avancé des systèmes), utilisation des sorties
- ASF (Advanced Systems Format), nombres et formats de sortie
- ASF (format des systèmes avancés), nombres et formats de sortie
- nombres et formats de sortie, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723458"
---
# <a name="working-with-outputs"></a><span data-ttu-id="aff11-109">Utilisation des sorties</span><span class="sxs-lookup"><span data-stu-id="aff11-109">Working with Outputs</span></span>

<span data-ttu-id="aff11-110">Par défaut, chaque exemple que vous recevez de l’un des deux objets de lecteur est associé à un numéro de sortie.</span><span class="sxs-lookup"><span data-stu-id="aff11-110">As a default, every sample you receive from either reader object is associated with an output number.</span></span> <span data-ttu-id="aff11-111">Chaque numéro de sortie correspond à un flux du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="aff11-111">Each output number corresponds to a stream in the ASF file.</span></span> <span data-ttu-id="aff11-112">Le lecteur attribue des numéros de sortie aux flux du fichier lorsque le fichier est ouvert.</span><span class="sxs-lookup"><span data-stu-id="aff11-112">The reader assigns output numbers to the streams in the file when the file is opened.</span></span> <span data-ttu-id="aff11-113">Normalement, il y a une sortie pour chaque flux dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="aff11-113">Normally there is one output for each stream in a file.</span></span> <span data-ttu-id="aff11-114">Toutefois, si le fichier utilise l’exclusion mutuelle, un seul numéro de sortie est attribué à chaque groupe de flux mutuellement exclusifs.</span><span class="sxs-lookup"><span data-stu-id="aff11-114">If the file uses mutual exclusion, however, each group of mutually exclusive streams is assigned a single output number.</span></span> <span data-ttu-id="aff11-115">Le flux qui correspond au numéro de sortie des flux s’excluant mutuellement est déterminé par le lecteur, dans le cas de fichiers à débit binaire multiple (MBR) ou par votre application, si vous utilisez la sélection manuelle de flux.</span><span class="sxs-lookup"><span data-stu-id="aff11-115">The stream that corresponds to the output number of the mutually exclusive streams is determined either by the reader, in the case of multiple bit rate (MBR) files, or by your application, if you are using manual stream selection.</span></span>

<span data-ttu-id="aff11-116">Étant donné que le nom de connexion défini dans le profil n’est pas conservé dans le fichier, le lecteur crée un nom de connexion par défaut pour chaque sortie qui est simplement une représentation sous forme de chaîne du numéro de sortie, par exemple « 1 », « 2 », « 3 », etc.</span><span class="sxs-lookup"><span data-stu-id="aff11-116">Because the connection name set in the profile is not persisted in the file, the reader creates a default connection name for each output that is simply a string representation of the output number, for example "1", "2", "3" and so on.</span></span> <span data-ttu-id="aff11-117">Les noms de connexion permettent aux applications et au lecteur lui-même de mettre en corrélation les sorties avec les flux.</span><span class="sxs-lookup"><span data-stu-id="aff11-117">The connection names enable applications, and the reader itself, to correlate outputs to streams.</span></span> <span data-ttu-id="aff11-118">Dans un fichier à plusieurs vitesses de transmission, plusieurs flux partagent un nom de connexion.</span><span class="sxs-lookup"><span data-stu-id="aff11-118">In a multiple bit rate file, several streams share a connection name.</span></span> <span data-ttu-id="aff11-119">Cela n’a pas d’importance pour le lecteur, car les propriétés de sortie de chaque flux MBR sont identiques.</span><span class="sxs-lookup"><span data-stu-id="aff11-119">This does not matter to the reader, because the output properties for each MBR stream are identical.</span></span>

<span data-ttu-id="aff11-120">Chaque sortie a un ou plusieurs formats de sortie pris en charge.</span><span class="sxs-lookup"><span data-stu-id="aff11-120">Each output has one or more supported output formats.</span></span> <span data-ttu-id="aff11-121">Un format de sortie est le format que les exemples non compressés fournis par le lecteur utilisent.</span><span class="sxs-lookup"><span data-stu-id="aff11-121">An output format is the format that the uncompressed samples delivered by the reader use.</span></span> <span data-ttu-id="aff11-122">Lorsque le lecteur ouvre un fichier, il définit le format de chaque sortie sur la valeur par défaut pour le sous-type de média.</span><span class="sxs-lookup"><span data-stu-id="aff11-122">When the reader opens a file, it sets the format of each output to the default for the media subtype.</span></span> <span data-ttu-id="aff11-123">Le nombre et le type des formats de sortie pris en charge sont déterminés par le codec qui décompresse les données multimédias.</span><span class="sxs-lookup"><span data-stu-id="aff11-123">The number and type of output formats supported is determined by the codec that decompresses the media data.</span></span>

<span data-ttu-id="aff11-124">Les rubriques suivantes expliquent comment utiliser les sorties :</span><span class="sxs-lookup"><span data-stu-id="aff11-124">The following topics explain how to work with outputs:</span></span>

-   [<span data-ttu-id="aff11-125">Pour identifier les numéros de sortie</span><span class="sxs-lookup"><span data-stu-id="aff11-125">To Identify Output Numbers</span></span>](to-identify-output-numbers.md)
-   [<span data-ttu-id="aff11-126">Assigner des formats de sortie</span><span class="sxs-lookup"><span data-stu-id="aff11-126">Assigning Output Formats</span></span>](assigning-output-formats.md)

## <a name="related-topics"></a><span data-ttu-id="aff11-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aff11-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aff11-128">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="aff11-128">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="aff11-129">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="aff11-129">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="aff11-130">**Lecture des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="aff11-130">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




