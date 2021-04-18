---
title: Écriture d’exemples compressés
description: Écriture d’exemples compressés
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- ASF (Advanced Systems Format), écrire des exemples compressés
- ASF (format avancé des systèmes), écriture d’exemples compressés
- ASF (Advanced Systems Format), passer des exemples compressés
- ASF (format de systèmes avancés), passer des exemples compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104462711"
---
# <a name="writing-compressed-samples"></a><span data-ttu-id="27753-107">Écriture d’exemples compressés</span><span class="sxs-lookup"><span data-stu-id="27753-107">Writing Compressed Samples</span></span>

<span data-ttu-id="27753-108">Pour certains flux audio ou vidéo, vous souhaiterez peut-être passer des exemples qui sont déjà compressés au lieu de transmettre des données brutes.</span><span class="sxs-lookup"><span data-stu-id="27753-108">For some audio or video streams, you may want to pass samples that are already compressed instead of passing raw data.</span></span> <span data-ttu-id="27753-109">Cette fonctionnalité permet de copier un flux existant ou d’écrire des exemples compressés à l’aide d’un codec tiers.</span><span class="sxs-lookup"><span data-stu-id="27753-109">This feature is used to copy an existing stream or to write samples compressed with a third-party codec.</span></span> <span data-ttu-id="27753-110">Le processus d’écriture d’un exemple compressé est identique à l’écriture d’un exemple non compressé, sauf que vous utilisez [**IWMWriterAdvanced :: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) au lieu de [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span><span class="sxs-lookup"><span data-stu-id="27753-110">The process of writing a compressed sample is identical to writing an uncompressed sample, except that you use [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) instead of [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span> <span data-ttu-id="27753-111">Pour plus d’informations sur l’écriture d’exemples non compressés, consultez [pour écrire des exemples](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="27753-111">For more information about writing uncompressed samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="27753-112">Lorsque vous écrivez des exemples compressés, pour les profils CBR, le writer supprime certains exemples, si nécessaire, pour conserver le contenu dans les valeurs de la vitesse de transmission et de la fenêtre tampon spécifiées.</span><span class="sxs-lookup"><span data-stu-id="27753-112">When you write compressed samples, for CBR profiles, the writer will drop some samples, if necessary, to keep the content within the specified bit rate and buffer window values.</span></span> <span data-ttu-id="27753-113">Pour VBR, l’enregistreur ne supprimera pas les exemples, mais il n’existe aucun moyen de s’assurer que les valeurs de la vitesse de transmission et de la fenêtre de mémoire tampon seront correctes.</span><span class="sxs-lookup"><span data-stu-id="27753-113">For VBR, the writer will not drop samples, but there is no way to be sure that the bit rate and buffer window values will be correct.</span></span>

<span data-ttu-id="27753-114">Si vous copiez un flux d’un fichier vers un autre, vous devez toujours copier l’objet de configuration de flux à partir du profil du fichier d’origine vers le profil du nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="27753-114">If you are copying a stream from one file to another, you should always copy the stream configuration object from the profile of the original file to the profile of the new file.</span></span> <span data-ttu-id="27753-115">Cela garantit que vous disposez des informations de vitesse de transmission et de fenêtre de mémoire tampon appropriées.</span><span class="sxs-lookup"><span data-stu-id="27753-115">This ensures that you have the correct bit rate and buffer window information.</span></span> <span data-ttu-id="27753-116">Si vous copiez un flux compressé dans un flux qui a une fenêtre de mémoire tampon inférieure définie, des exemples seront supprimés lors de l’écriture du fichier.</span><span class="sxs-lookup"><span data-stu-id="27753-116">If you copy a compressed stream to a stream that has a lower buffer window set, samples will be dropped during file writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27753-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27753-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27753-118">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="27753-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




