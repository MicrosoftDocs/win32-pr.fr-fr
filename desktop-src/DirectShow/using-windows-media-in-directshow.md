---
description: Utilisation de Windows Media dans DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Utilisation de Windows Media dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104393859"
---
# <a name="using-windows-media-in-directshow"></a><span data-ttu-id="8694e-103">Utilisation de Windows Media dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="8694e-103">Using Windows Media in DirectShow</span></span>

<span data-ttu-id="8694e-104">Cette section décrit comment utiliser DirectShow pour lire et écrire des fichiers ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="8694e-104">This section describes how to use DirectShow to play and write Advanced Systems Format (ASF) files.</span></span> <span data-ttu-id="8694e-105">Les fichiers ASF contiennent généralement du contenu audio et vidéo encodé à l’aide des codecs Windows Media Audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="8694e-105">ASF files commonly contain audio and video content encoded using the Windows Media Audio and Video codecs.</span></span> <span data-ttu-id="8694e-106">Toutefois, ASF peut contenir n’importe quel type de données.</span><span class="sxs-lookup"><span data-stu-id="8694e-106">However, ASF can contain any type of data.</span></span>

<span data-ttu-id="8694e-107">Les filtres DirectShow suivants prennent en charge la lecture et l’écriture de fichiers ASF :</span><span class="sxs-lookup"><span data-stu-id="8694e-107">The following DirectShow filters support reading and writing ASF files:</span></span>

-   <span data-ttu-id="8694e-108">[Filtre de lecteur ASF WM](wm-asf-reader-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8694e-108">[WM ASF Reader Filter](wm-asf-reader-filter.md).</span></span> <span data-ttu-id="8694e-109">Lit les fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="8694e-109">Reads ASF files.</span></span>
-   <span data-ttu-id="8694e-110">[Filtre d’enregistreur ASF WM](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8694e-110">[WM ASF Writer Filter](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="8694e-111">Fichiers ASF Wrties.</span><span class="sxs-lookup"><span data-stu-id="8694e-111">Wrties ASF files.</span></span>
-   <span data-ttu-id="8694e-112">[Filtre de wrapper DMO](dmo-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8694e-112">[DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="8694e-113">Encapsule le codeur et le décodeur Windows Media DMOs.</span><span class="sxs-lookup"><span data-stu-id="8694e-113">Wraps the Windows Media encoder and decoder DMOs.</span></span>

### <a name="versions"></a><span data-ttu-id="8694e-114">Versions</span><span class="sxs-lookup"><span data-stu-id="8694e-114">Versions</span></span>

<span data-ttu-id="8694e-115">Le lecteur ASF WM et les filtres du writer WM ASF sont empaquetés dans la DLL nommée qasf.dll, et les filtres sont appelés « composants QASF ».</span><span class="sxs-lookup"><span data-stu-id="8694e-115">The WM ASF Reader and WM ASF Writer filters are packaged in the DLL named qasf.dll, and the filters are collectively named "QASF components."</span></span> <span data-ttu-id="8694e-116">Ces filtres sont des wrappers pour le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8694e-116">These filters are wrappers for the Windows Media Format SDK.</span></span> <span data-ttu-id="8694e-117">La DLL (qasf.dll) a été publiée pour la première fois dans le SDK DirectX, mais elle a été mise à jour ultérieurement dans le kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="8694e-117">The DLL (qasf.dll) was first published in the DirectX SDK but was later updated in the Windows Media Format SDK.</span></span> <span data-ttu-id="8694e-118">Voici l’historique des versions des filtres QASF :</span><span class="sxs-lookup"><span data-stu-id="8694e-118">Here is the version history of the QASF filters:</span></span>

-   <span data-ttu-id="8694e-119">DirectShow 8,1 prend en charge le kit de développement logiciel (SDK) Windows Media format version 7,0.</span><span class="sxs-lookup"><span data-stu-id="8694e-119">DirectShow 8.1 supports Windows Media Format SDK version 7.0.</span></span>
-   <span data-ttu-id="8694e-120">DirectShow 9,0 prend en charge le kit de développement logiciel (SDK) Windows Media format version 7,1.</span><span class="sxs-lookup"><span data-stu-id="8694e-120">DirectShow 9.0 supports Windows Media Format SDK version 7.1.</span></span>
-   <span data-ttu-id="8694e-121">Windows XP Service Pack 2 prend en charge le kit de développement logiciel (SDK) Windows Media Format 9.</span><span class="sxs-lookup"><span data-stu-id="8694e-121">Windows XP Service Pack 2 supports Windows Media Format 9 SDK.</span></span>
-   <span data-ttu-id="8694e-122">Windows Vista prend en charge le kit de développement logiciel (SDK) Windows Media format 11.</span><span class="sxs-lookup"><span data-stu-id="8694e-122">Windows Vista supports Windows Media Format 11 SDK.</span></span>
-   <span data-ttu-id="8694e-123">Le kit de développement logiciel (SDK) Windows Media Format 9 et versions ultérieures contiennent les versions correspondantes de QASF.</span><span class="sxs-lookup"><span data-stu-id="8694e-123">Windows Media Format 9 SDK and later contain corresponding versions of QASF.</span></span>

<span data-ttu-id="8694e-124">Pour accéder à la dernière version de QASF, téléchargez toujours le kit de développement logiciel (SDK) de format Windows Media le plus récent.</span><span class="sxs-lookup"><span data-stu-id="8694e-124">To get the latest version of QASF, always download the latest Windows Media Format SDK.</span></span>

### <a name="legacy-windows-media-source-filter"></a><span data-ttu-id="8694e-125">Filtre de source Windows Media hérité</span><span class="sxs-lookup"><span data-stu-id="8694e-125">Legacy Windows Media Source Filter</span></span>

<span data-ttu-id="8694e-126">Dans Windows XP Service Pack 1 et versions antérieures, le filtre source par défaut pour les fichiers ASF (extensions de fichier. ASF,. wmv et. WMA) est le [filtre de source Windows Media](windows-media-source-filter.md)obsolète.</span><span class="sxs-lookup"><span data-stu-id="8694e-126">In Windows XP Service Pack 1 and earlier, the default source filter for ASF files (.asf, .wmv, and .wma file extensions) is the obsolete [Windows Media Source Filter](windows-media-source-filter.md).</span></span> <span data-ttu-id="8694e-127">Ce comportement a été maintenu pour garantir la compatibilité descendante avec les applications qui utilisaient le lecteur Windows Media 6,4.</span><span class="sxs-lookup"><span data-stu-id="8694e-127">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="8694e-128">Les nouvelles applications doivent utiliser les versions plus récentes de QASF, qui font du filtre du lecteur ASF WM le filtre par défaut pour la lecture des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="8694e-128">New applications should use the newer versions of QASF, which make the WM ASF Reader filter the default filter for playing ASF files.</span></span>

<span data-ttu-id="8694e-129">Pour plus d’informations sur la suite Windows Media des kits de développement logiciel, consultez la section [audio et vidéo](../audio-and-video.md) de la bibliothèque MSDN.</span><span class="sxs-lookup"><span data-stu-id="8694e-129">For more information on the Windows Media suite of software development kits, see the [Audio and Video](../audio-and-video.md) section of the MDSN Library.</span></span>

<span data-ttu-id="8694e-130">Cet article contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8694e-130">This article contains the following topics:</span></span>

-   [<span data-ttu-id="8694e-131">Lecture de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="8694e-131">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
-   [<span data-ttu-id="8694e-132">Création de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="8694e-132">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="8694e-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8694e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8694e-134">Utilisation de DirectShow</span><span class="sxs-lookup"><span data-stu-id="8694e-134">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 
