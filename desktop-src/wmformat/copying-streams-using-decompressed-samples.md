---
title: Copie de flux à l’aide d’exemples décompressés
description: Copie de flux à l’aide d’exemples décompressés
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows Media Format SDK, copie de flux
- ASF (Advanced Systems Format), copie de flux
- ASF (format de systèmes avancés), copie de flux
- flux, copie à l’aide de données décompressées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106544144"
---
# <a name="copying-streams-using-decompressed-samples"></a><span data-ttu-id="a19b2-107">Copie de flux à l’aide d’exemples décompressés</span><span class="sxs-lookup"><span data-stu-id="a19b2-107">Copying Streams Using Decompressed Samples</span></span>

<span data-ttu-id="a19b2-108">Il est fortement recommandé de ne pas copier les flux d’un fichier vers un autre à l’aide d’exemples décompressés.</span><span class="sxs-lookup"><span data-stu-id="a19b2-108">It is strongly recommended that you not copy streams from one file to another using decompressed samples.</span></span> <span data-ttu-id="a19b2-109">Le processus de décompression et de recompression des exemples entraîne une dégradation de la qualité de la sortie.</span><span class="sxs-lookup"><span data-stu-id="a19b2-109">The process of decompressing and recompressing samples will degrade the quality of the output.</span></span> <span data-ttu-id="a19b2-110">Si vous avez besoin de décompresser vos exemples, puis de les copier dans un autre flux, vous risquez de rencontrer des difficultés avec les flux codés en fonction de la vitesse de transmission variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="a19b2-110">If you do need to decompress your samples and then copy them to another stream, you may encounter some difficulty with quality-based variable bit rate (VBR) encoded streams.</span></span>

<span data-ttu-id="a19b2-111">Lorsque le codec finit de compresser un flux VBR basé sur la qualité, il enregistre la vitesse de transmission et la fenêtre de mémoire tampon du contenu résultant.</span><span class="sxs-lookup"><span data-stu-id="a19b2-111">When the codec finishes compressing a quality-based VBR stream, it records the bit rate and buffer window of the resulting content.</span></span> <span data-ttu-id="a19b2-112">Quand vous lisez un fichier contenant un flux encodé à l’aide de la fonction VBR basée sur la qualité, le profil obtenu à partir du lecteur indique la vitesse de transmission et la fenêtre de mémoire tampon, ainsi que la vitesse de transmission maximale et la fenêtre de mémoire tampon maximale.</span><span class="sxs-lookup"><span data-stu-id="a19b2-112">When you read a file containing a stream encoded with quality-based VBR, the profile obtained from the reader will note the bit rate and buffer window as well as the maximum bit rate and maximum buffer window.</span></span> <span data-ttu-id="a19b2-113">Cette configuration dans le profil signifie normalement un flux de vitesse de transmission variable à vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="a19b2-113">This configuration in the profile normally signifies a bit-rate constrained variable bit rate stream.</span></span> <span data-ttu-id="a19b2-114">Par conséquent, lorsque vous définissez le profil sur le writer, il s’attend à obtenir une passe de prétraitement pour le flux, car les flux VBR à vitesse de transmission requièrent un encodage en deux passes.</span><span class="sxs-lookup"><span data-stu-id="a19b2-114">As a result, when you set the profile on the writer, it will expect a preprocessing pass for the stream, because bit-rate constrained VBR streams require two-pass encoding.</span></span> <span data-ttu-id="a19b2-115">Vous devez traiter le flux comme s’il s’agissait d’un flux VBR à vitesse de transmission restreinte et remettre les exemples pour le prétraitement.</span><span class="sxs-lookup"><span data-stu-id="a19b2-115">You should treat the stream as if it were a bit-rate constrained VBR stream and deliver the samples for preprocessing.</span></span> <span data-ttu-id="a19b2-116">Étant donné que vous utilisez les valeurs retournées après l’encodage du contenu à un niveau de qualité particulier, ces valeurs représentent le niveau de qualité souhaité.</span><span class="sxs-lookup"><span data-stu-id="a19b2-116">Because you are using the values returned after encoding the content at a particular quality level, those values represent the desired quality level.</span></span> <span data-ttu-id="a19b2-117">Bien entendu, la qualité de la sortie ré-encodée sera tout de même dégradée, en raison de la nouvelle encodage.</span><span class="sxs-lookup"><span data-stu-id="a19b2-117">Of course, the quality of the re-encoded output will be somewhat degraded anyway, as a result of the re-encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a19b2-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a19b2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a19b2-119">**Copie de données d’un fichier vers un autre**</span><span class="sxs-lookup"><span data-stu-id="a19b2-119">**Copying Data from One File to Another**</span></span>](copying-data-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="a19b2-120">**Copie de flux sans décompression des données**</span><span class="sxs-lookup"><span data-stu-id="a19b2-120">**Copying Streams Without Decompressing the Data**</span></span>](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




