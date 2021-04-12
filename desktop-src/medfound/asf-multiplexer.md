---
description: Multiplexeur ASF
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: Multiplexeur ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033823"
---
# <a name="asf-multiplexer"></a><span data-ttu-id="b0260-103">Multiplexeur ASF</span><span class="sxs-lookup"><span data-stu-id="b0260-103">ASF Multiplexer</span></span>

<span data-ttu-id="b0260-104">Le *multiplexeur* ASF est un objet de couche WMContainer qui fonctionne avec l' [objet de données ASF](asf-file-structure.md) et donne à une application la possibilité de générer des paquets de données pour un conteneur ASF.</span><span class="sxs-lookup"><span data-stu-id="b0260-104">The ASF *multiplexer* is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate data packets for an ASF container.</span></span> <span data-ttu-id="b0260-105">Le multiplexeur accepte les données multimédias sous la forme d' [exemples](media-samples.md) de média et génère des exemples de média basés sur les paramètres de paquets de streaming et ASF définis dans l' [objet d’en-tête ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="b0260-105">The multiplexer accepts media data in the form of [Media Samples](media-samples.md) and outputs media samples based on streaming and ASF packet parameters defined in the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="b0260-106">Les exemples de supports de sortie contiennent des références à un ou plusieurs tampons de média qui contiennent des données multimédias numériques paquets. Vous pouvez utiliser cet objet dans un scénario d’encodage de fichier dans lequel il reçoit des exemples de flux encodés à partir de l’encodeur ou pour le transcodage ASF-ASF (remuxing).</span><span class="sxs-lookup"><span data-stu-id="b0260-106">The output media samples hold references to one or more media buffers that contain packetized digital media data.You can use this object in a file encoding scenario where it receives encoded stream samples from the encoder or for ASF-ASF transcoding (remuxing).</span></span>

<span data-ttu-id="b0260-107">Le diagramme suivant illustre la génération de paquets de données ASF pour un fichier ASF à l’aide du multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="b0260-107">The following diagram illustrates ASF data packet generation for an ASF file using the multiplexer.</span></span>

![Diagramme montrant la génération de paquets de données ASF](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

<span data-ttu-id="b0260-109">Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="b0260-109">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="b0260-110">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0260-110">This section contains the following topics:</span></span>



| <span data-ttu-id="b0260-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b0260-111">Topic</span></span>                                                                  | <span data-ttu-id="b0260-112">Description</span><span class="sxs-lookup"><span data-stu-id="b0260-112">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="b0260-113">Création de l’objet multiplexeur</span><span class="sxs-lookup"><span data-stu-id="b0260-113">Creating the Multiplexer Object</span></span>](creating-the-multiplexer-object.md) | <span data-ttu-id="b0260-114">Comment créer et initialiser le multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="b0260-114">How to create and initialize the multiplexer.</span></span>                     |
| [<span data-ttu-id="b0260-115">Génération de nouveaux paquets de données ASF</span><span class="sxs-lookup"><span data-stu-id="b0260-115">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md) | <span data-ttu-id="b0260-116">Comment générer des paquets de données pour constituer un nouvel objet de données ASF.</span><span class="sxs-lookup"><span data-stu-id="b0260-116">How to generate data packets to constitute a new ASF Data Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b0260-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0260-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0260-118">Composants WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="b0260-118">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="b0260-119">Didacticiel : copie de flux de fichiers ASF d’un fichier à un autre</span><span class="sxs-lookup"><span data-stu-id="b0260-119">Tutorial: Copying ASF Streams from One File to Another</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="b0260-120">Didacticiel : écriture d’un fichier WMA à l’aide de l’encodage CBR</span><span class="sxs-lookup"><span data-stu-id="b0260-120">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



