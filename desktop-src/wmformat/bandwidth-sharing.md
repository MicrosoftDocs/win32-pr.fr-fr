---
title: Partage de bande passante
description: Partage de bande passante
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows Media Format SDK, partage de bande passante
- ASF (Advanced Systems Format), partage de bande passante
- ASF (format de systèmes avancés), partage de bande passante
- Windows Media Format SDK, flux
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- partage de bande passante, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2221d2fbc44654af7f12acf6e45fb85ca32b7d2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030824"
---
# <a name="bandwidth-sharing"></a><span data-ttu-id="28711-110">Partage de bande passante</span><span class="sxs-lookup"><span data-stu-id="28711-110">Bandwidth Sharing</span></span>

<span data-ttu-id="28711-111">Vous pouvez spécifier des flux dans un fichier qui, lorsqu’ils sont utilisés ensemble, utilisent moins de bande passante que la somme des vitesses de transmission indiquées.</span><span class="sxs-lookup"><span data-stu-id="28711-111">You can specify streams in a file that, when taken together, use less bandwidth than the sum of their stated bit rates combined.</span></span> <span data-ttu-id="28711-112">En spécifiant le partage de bande passante dans le profil, vous précisez que vous devez lire les applications dont la bande passante disponible pour diffuser le fichier n’est pas celle qui pourrait autrement paraître.</span><span class="sxs-lookup"><span data-stu-id="28711-112">By specifying bandwidth sharing in the profile, you clarify to reading applications that the available bandwidth needed to stream the file is not what it might otherwise seem.</span></span>

<span data-ttu-id="28711-113">Aucun des objets du kit de développement logiciel (SDK) de format Windows Media ne modifie leur comportement en réponse aux informations de partage de bande passante, qui sont fournies uniquement afin que la lecture des applications puisse prendre en compte lorsque vous déterminez si un fichier peut être lu avec une remise de bande passante limitée.</span><span class="sxs-lookup"><span data-stu-id="28711-113">None of the objects of the Windows Media Format SDK change their behavior in response to bandwidth sharing information, which is provided solely so that reading applications can take it into account when determining whether a file can be played with restricted bandwidth delivery.</span></span>

<span data-ttu-id="28711-114">Le partage de bande passante est configuré avec un objet de partage de bande passante et est ajouté à un profil avant de commencer à écrire un fichier.</span><span class="sxs-lookup"><span data-stu-id="28711-114">Bandwidth sharing is configured with a bandwidth sharing object and is added to a profile before beginning to write a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28711-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28711-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28711-116">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="28711-116">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="28711-117">**Objet de partage de bande passante**</span><span class="sxs-lookup"><span data-stu-id="28711-117">**Bandwidth Sharing Object**</span></span>](bandwidth-sharing-object.md)
</dt> <dt>

[<span data-ttu-id="28711-118">**Interface IWMBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="28711-118">**IWMBandwidthSharing Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="28711-119">**Interface IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="28711-119">**IWMProfile3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[<span data-ttu-id="28711-120">**Utilisation du partage de bande passante**</span><span class="sxs-lookup"><span data-stu-id="28711-120">**Using Bandwidth Sharing**</span></span>](using-bandwidth-sharing.md)
</dt> </dl>

 

 




