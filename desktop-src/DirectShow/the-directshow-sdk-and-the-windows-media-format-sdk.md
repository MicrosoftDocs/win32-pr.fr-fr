---
description: Le SDK DirectShow et le kit de développement logiciel (SDK) Windows Media format
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: Le SDK DirectShow et le kit de développement logiciel (SDK) Windows Media format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321641"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a><span data-ttu-id="73e23-103">Le SDK DirectShow et le kit de développement logiciel (SDK) Windows Media format</span><span class="sxs-lookup"><span data-stu-id="73e23-103">The DirectShow SDK and the Windows Media Format SDK</span></span>

<span data-ttu-id="73e23-104">DirectShow et le kit de développement logiciel (SDK) du format Windows Media offrent des solutions complémentaires pour écrire des applications qui créent et lisent des flux de format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="73e23-104">DirectShow and the Windows Media Format SDK offer complementary solutions for writing applications that create and play back Windows Media Format streams.</span></span> <span data-ttu-id="73e23-105">Pour plus d’informations, consultez la section «[audio et vidéo](../audio-and-video.md)» de la bibliothèque MSDN.</span><span class="sxs-lookup"><span data-stu-id="73e23-105">For more information, see the "[Audio and Video](../audio-and-video.md)" section of the MSDN Library.</span></span>

<span data-ttu-id="73e23-106">Le filtre d’écriture ASF accepte un nombre quelconque de flux d’entrée et crée un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="73e23-106">The ASF Writer filter accepts any number of input streams and creates an ASF file.</span></span> <span data-ttu-id="73e23-107">Le filtre utilise le kit de développement logiciel (SDK) Windows Media format pour convertir des fichiers audio ou vidéo non compressés en contenu Windows Media.</span><span class="sxs-lookup"><span data-stu-id="73e23-107">The filter uses the Windows Media Format SDK to convert uncompressed audio or video files to Windows Media-based content.</span></span> <span data-ttu-id="73e23-108">Le contenu compressé est ensuite stocké dans le format de conteneur ASF.</span><span class="sxs-lookup"><span data-stu-id="73e23-108">The compressed content is then stored in the ASF container format.</span></span> <span data-ttu-id="73e23-109">Si le contenu est uniquement audio, le fichier reçoit une extension. WMA et est appelé fichier Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="73e23-109">If the content is audio only, then the file is given a .wma extension and is referred to as a Windows Media Audio file.</span></span> <span data-ttu-id="73e23-110">Si le contenu est vidéo uniquement ou vidéo et audio, le fichier reçoit une extension. wmv et est appelé fichier Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="73e23-110">If the content is video only or video and audio, then the file is given a .wmv extension and is referred to as a Windows Media Video file.</span></span> <span data-ttu-id="73e23-111">Chaque type de fichier peut également inclure des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="73e23-111">Either type of file may also include metadata.</span></span>

<span data-ttu-id="73e23-112">Vous pouvez utiliser l’enregistreur ASF WM dans différents scénarios, y compris la capture vidéo numérique (DV), la recompression audio et la conversion de fichiers multimédias Audio-Video entrelacés (AVI) ou MPEG pour la diffusion réseau.</span><span class="sxs-lookup"><span data-stu-id="73e23-112">You can use the WM ASF Writer in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG multimedia files for network streaming.</span></span> <span data-ttu-id="73e23-113">Ce filtre offre la seule façon de créer des fichiers Microsoft® Windows Media™ audio (WMA) et Windows Media Video (WMV) dans DirectShow®.</span><span class="sxs-lookup"><span data-stu-id="73e23-113">This filter provides the only way to create Microsoft® Windows Media™ Audio (WMA) and Windows Media Video (WMV) files in DirectShow®.</span></span> <span data-ttu-id="73e23-114">Le filtre peut également créer des fichiers qui sont sécurisés par des Rights Management numériques (DRM) et peut également créer du contenu MPEG-4 à l’aide de l’encodeur Microsoft MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="73e23-114">The filter can also create files that are secured by Digital Rights Management (DRM), and can also create MPEG-4 content using the Microsoft MPEG-4 Encoder.</span></span> <span data-ttu-id="73e23-115">Ce contenu est stocké dans le format de conteneur ASF.</span><span class="sxs-lookup"><span data-stu-id="73e23-115">This content is stored in the ASF container format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73e23-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73e23-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73e23-117">Création de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="73e23-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
