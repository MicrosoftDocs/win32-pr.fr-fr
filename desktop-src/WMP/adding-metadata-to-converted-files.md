---
title: Ajout de métadonnées aux fichiers convertis
description: Ajout de métadonnées aux fichiers convertis
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Windows Media Player, processus de conversion
- Plug-ins du lecteur Windows Media, conversion
- plug-ins, conversion
- plug-ins de conversion, ajout de métadonnées aux fichiers convertis
- ajout de métadonnées aux fichiers convertis
- métadonnées, ajouter aux fichiers convertis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727733"
---
# <a name="adding-metadata-to-converted-files"></a><span data-ttu-id="7c937-109">Ajout de métadonnées aux fichiers convertis</span><span class="sxs-lookup"><span data-stu-id="7c937-109">Adding Metadata to Converted Files</span></span>

<span data-ttu-id="7c937-110">Les fichiers convertis doivent contenir certaines métadonnées pour garantir une expérience utilisateur optimale.</span><span class="sxs-lookup"><span data-stu-id="7c937-110">Converted files must contain certain metadata to ensure a good user experience.</span></span> <span data-ttu-id="7c937-111">Au minimum, les fichiers convertis doivent contenir les attributs principaux figurant dans les [instructions d’utilisation des métadonnées Windows Media](/previous-versions/ms867702(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="7c937-111">At a minimum, converted files must contain the primary attributes listed in the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

<span data-ttu-id="7c937-112">Pour les fichiers musicaux, définissez la valeur de **WM/MediaClassPrimaryID** sur D1607DBC-E323-4BE2-86A1-48A42A28441E.</span><span class="sxs-lookup"><span data-stu-id="7c937-112">For music files, set the value for **WM/MediaClassPrimaryID** to D1607DBC-E323-4BE2-86A1-48A42A28441E.</span></span>

<span data-ttu-id="7c937-113">Pour les fichiers de messagerie vocale, définissez la valeur de **WM/MediaClassPrimaryID** sur 01CD0F29-DA4E-4157-897b-6275D50C4F11, qui est le GUID de la classe principale pour les fichiers audio.</span><span class="sxs-lookup"><span data-stu-id="7c937-113">For voicemail files, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11, which is the primary class GUID for audio files.</span></span> <span data-ttu-id="7c937-114">Définissez la valeur de **WM/MediaClassSecondaryID** sur 193c8824-4D52-4178-90BD-305240b04636.</span><span class="sxs-lookup"><span data-stu-id="7c937-114">Set the value for **WM/MediaClassSecondaryID** to 193c8824-4d52-4178-90bd-305240b04636.</span></span>

<span data-ttu-id="7c937-115">Pour les notes vocales, définissez la valeur de **WM/MediaClassPrimaryID** sur 01CD0F29-DA4E-4157-897b-6275D50C4F11.</span><span class="sxs-lookup"><span data-stu-id="7c937-115">For voice notes, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11.</span></span> <span data-ttu-id="7c937-116">Définissez la valeur de **WM/MediaClassSecondaryID** sur 3A172A13-2BD9-4831-835B-114F6A95943F.</span><span class="sxs-lookup"><span data-stu-id="7c937-116">Set the value for **WM/MediaClassSecondaryID** to 3A172A13-2BD9-4831-835B-114F6A95943F.</span></span>

<span data-ttu-id="7c937-117">Définissez la valeur de **WM/ContentDistributor** sur le nom de clé du service musical qui a fourni le contenu.</span><span class="sxs-lookup"><span data-stu-id="7c937-117">Set the value for **WM/ContentDistributor** to the key name for the music service that provided the content.</span></span>

<span data-ttu-id="7c937-118">Définissez la valeur de **WM/UniqueFileIdentifier** sur l’ID de contenu.</span><span class="sxs-lookup"><span data-stu-id="7c937-118">Set the value for **WM/UniqueFileIdentifier** to the content ID.</span></span> <span data-ttu-id="7c937-119">Cela vous permettra de récupérer des éléments de contenu spécifiques à un moment ultérieur.</span><span class="sxs-lookup"><span data-stu-id="7c937-119">This will enable you to retrieve specific content items at a future time.</span></span>

<span data-ttu-id="7c937-120">Définissez une valeur pour **WM/WMShadowFileSourceFileType**.</span><span class="sxs-lookup"><span data-stu-id="7c937-120">Set a value for **WM/WMShadowFileSourceFileType**.</span></span>

<span data-ttu-id="7c937-121">Pour le contenu protégé, utilisez le kit de développement logiciel (SDK) Windows Media format pour définir l’attribut **DRM \_ DRMHeader \_ CONTENTID** sur l’ID de contenu.</span><span class="sxs-lookup"><span data-stu-id="7c937-121">For protected content, use the Windows Media Format SDK to set the **DRM\_DRMHeader\_ContentID** attribute to the content ID.</span></span>

<span data-ttu-id="7c937-122">Pour le contenu protégé, définissez une valeur pour **WM/WMShadowFileSourceDRMType**.</span><span class="sxs-lookup"><span data-stu-id="7c937-122">For protected content, set a value for **WM/WMShadowFileSourceDRMType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c937-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c937-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c937-124">**À propos des plug-ins de conversion**</span><span class="sxs-lookup"><span data-stu-id="7c937-124">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="7c937-125">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="7c937-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 