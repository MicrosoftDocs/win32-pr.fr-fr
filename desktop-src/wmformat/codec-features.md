---
title: Fonctionnalités du codec
description: Fonctionnalités du codec
ms.assetid: e0bbdf75-2369-4080-ae8e-aabaa8401dcf
keywords:
- SDK Windows Media format, fonctionnalités de codec
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalités
- codecs, fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3623bcb6f338fe11bef3089705801dc3ea047
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196766"
---
# <a name="codec-features"></a><span data-ttu-id="2df9e-106">Fonctionnalités du codec</span><span class="sxs-lookup"><span data-stu-id="2df9e-106">Codec Features</span></span>

<span data-ttu-id="2df9e-107">Le kit de développement logiciel (SDK) Windows Media format est fourni avec plusieurs codecs audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="2df9e-107">The Windows Media Format SDK is delivered with several audio and video codecs.</span></span> <span data-ttu-id="2df9e-108">Vous pouvez utiliser les codecs fournis pour compresser et décompresser du contenu pour répondre à différents besoins.</span><span class="sxs-lookup"><span data-stu-id="2df9e-108">You can use the codecs provided to compress and decompress content to suit a variety of needs.</span></span> <span data-ttu-id="2df9e-109">Le codec utilisé par le writer pour compresser les données est spécifié par les informations de configuration de flux dans le profil.</span><span class="sxs-lookup"><span data-stu-id="2df9e-109">The codec that is used by the writer to compress data is specified by stream configuration information in the profile.</span></span> <span data-ttu-id="2df9e-110">Les informations du profil sont ensuite stockées dans l’en-tête du fichier créé par le writer.</span><span class="sxs-lookup"><span data-stu-id="2df9e-110">Information from the profile is then stored in the header of the file created by the writer.</span></span> <span data-ttu-id="2df9e-111">Ensuite, lorsque le fichier est ouvert par le lecteur ou le lecteur synchrone, les informations de profil dans l’en-tête identifient le codec nécessaire pour décompresser les données.</span><span class="sxs-lookup"><span data-stu-id="2df9e-111">Then, when the file is opened by the reader or synchronous reader, the profile information in the header identifies the codec needed to decompress the data.</span></span>

<span data-ttu-id="2df9e-112">Les fonctionnalités suivantes sont présentées dans cette section.</span><span class="sxs-lookup"><span data-stu-id="2df9e-112">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="2df9e-113">Codecs pris en charge</span><span class="sxs-lookup"><span data-stu-id="2df9e-113">Supported Codecs</span></span>](supported-codecs.md)
-   [<span data-ttu-id="2df9e-114">Encodage à débit binaire constant (CBR)</span><span class="sxs-lookup"><span data-stu-id="2df9e-114">Constant Bit Rate (CBR) Encoding</span></span>](constant-bit-rate--cbr--encoding.md)
-   [<span data-ttu-id="2df9e-115">Encodage à vitesse de transmission variable (VBR)</span><span class="sxs-lookup"><span data-stu-id="2df9e-115">Variable Bit Rate (VBR) Encoding</span></span>](variable-bit-rate--vbr--encoding.md)
-   [<span data-ttu-id="2df9e-116">Encodage en deux passes</span><span class="sxs-lookup"><span data-stu-id="2df9e-116">Two-Pass Encoding</span></span>](two-pass-encoding.md)
-   [<span data-ttu-id="2df9e-117">Prise en charge audio haute résolution</span><span class="sxs-lookup"><span data-stu-id="2df9e-117">High-Resolution Audio Support</span></span>](high-resolution-audio-support.md)
-   [<span data-ttu-id="2df9e-118">Audio à faible retards</span><span class="sxs-lookup"><span data-stu-id="2df9e-118">Low-Delay Audio</span></span>](low-delay-audio.md)
-   [<span data-ttu-id="2df9e-119">Sortie audio S/PDIF</span><span class="sxs-lookup"><span data-stu-id="2df9e-119">S/PDIF Audio Output</span></span>](s-pdif-audio-output.md)
-   [<span data-ttu-id="2df9e-120">Image vidéo</span><span class="sxs-lookup"><span data-stu-id="2df9e-120">Video Image</span></span>](video-image.md)
-   [<span data-ttu-id="2df9e-121">Modèles de conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="2df9e-121">Device Conformance Templates</span></span>](device-conformance-templates.md)
-   [<span data-ttu-id="2df9e-122">Paramètres de complexité de la vidéo</span><span class="sxs-lookup"><span data-stu-id="2df9e-122">Video Complexity Settings</span></span>](video-complexity-settings.md)
-   [<span data-ttu-id="2df9e-123">Interpolation de frame</span><span class="sxs-lookup"><span data-stu-id="2df9e-123">Frame Interpolation</span></span>](frame-interpolation.md)

## <a name="related-topics"></a><span data-ttu-id="2df9e-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2df9e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2df9e-125">**Fonctionnalités**</span><span class="sxs-lookup"><span data-stu-id="2df9e-125">**Features**</span></span>](features.md)
</dt> </dl>

 

 




