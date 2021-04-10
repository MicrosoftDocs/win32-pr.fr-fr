---
title: Copie de données d’un fichier vers un autre
description: Copie de données d’un fichier vers un autre
ms.assetid: 1403c396-46ea-48b1-a535-922ffca31bc2
keywords:
- Windows Media Format SDK, copie de données
- ASF (Advanced Systems Format), copie de données
- ASF (format de systèmes avancés), copie de données
- flux, copie de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b38a1675ac79630371fe4d3fda66d44b4b2990
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940257"
---
# <a name="copying-data-from-one-file-to-another"></a><span data-ttu-id="3b839-107">Copie de données d’un fichier vers un autre</span><span class="sxs-lookup"><span data-stu-id="3b839-107">Copying Data from One File to Another</span></span>

<span data-ttu-id="3b839-108">Au niveau le plus simple, la copie d’un flux d’un fichier ASF vers un autre est relativement simple.</span><span class="sxs-lookup"><span data-stu-id="3b839-108">At the most basic level, copying a stream from one ASF file to another is fairly straightforward.</span></span> <span data-ttu-id="3b839-109">Toutefois, il y a des problèmes à prendre en compte lors de l’utilisation de flux à partir de plusieurs fichiers d’entrée ou lors de la copie de flux que vous décompressez et recodez pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="3b839-109">However, there are issues to consider when working with streams from multiple input files or when copying streams that you first decompress and re-encode.</span></span>

<span data-ttu-id="3b839-110">Les sections suivantes décrivent la copie de flux.</span><span class="sxs-lookup"><span data-stu-id="3b839-110">The following sections describe copying streams.</span></span>



| <span data-ttu-id="3b839-111">Section</span><span class="sxs-lookup"><span data-stu-id="3b839-111">Section</span></span>                                                                                              | <span data-ttu-id="3b839-112">Descripiton</span><span class="sxs-lookup"><span data-stu-id="3b839-112">Descripiton</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b839-113">Copie de flux sans décompression des données</span><span class="sxs-lookup"><span data-stu-id="3b839-113">Copying Streams Without Decompressing the Data</span></span>](copying-streams-without-decompressing-the-data.md) | <span data-ttu-id="3b839-114">Décrit comment copier des flux à l’aide d’échantillons compressés pour préserver la qualité du contenu.</span><span class="sxs-lookup"><span data-stu-id="3b839-114">Describes how to copy streams using compressed samples to preserve the quality of the content.</span></span> |
| [<span data-ttu-id="3b839-115">Copie de flux à l’aide d’exemples décompressés</span><span class="sxs-lookup"><span data-stu-id="3b839-115">Copying Streams Using Decompressed Samples</span></span>](copying-streams-using-decompressed-samples.md)         | <span data-ttu-id="3b839-116">Décrit les difficultés liées à la copie des flux à l’aide d’exemples décompressés.</span><span class="sxs-lookup"><span data-stu-id="3b839-116">Describes the difficulties in copying streams using decompressed samples.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="3b839-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b839-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b839-118">**Gestionnaire de profils, objet**</span><span class="sxs-lookup"><span data-stu-id="3b839-118">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="3b839-119">**Configuration de flux, objet**</span><span class="sxs-lookup"><span data-stu-id="3b839-119">**Stream Configuration Object**</span></span>](stream-configuration-object.md)
</dt> <dt>

[<span data-ttu-id="3b839-120">**Lecteur synchrone, objet**</span><span class="sxs-lookup"><span data-stu-id="3b839-120">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="3b839-121">**Auteur, objet**</span><span class="sxs-lookup"><span data-stu-id="3b839-121">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




