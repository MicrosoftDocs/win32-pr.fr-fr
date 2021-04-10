---
title: Nouveautés (kit de développement logiciel (SDK) Windows Media format 11)
description: What's New
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media Format SDK, nouveautés
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalités
- Windows Media Format SDK, nouvelles fonctionnalités
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, mises à jour DRM
- Windows Media Format SDK, mises à jour de codec
- Windows Media Format SDK, images miniatures
- gestion des droits numériques (DRM), nouvelles fonctionnalités
- DRM (gestion des droits numériques), nouvelles fonctionnalités
- images miniatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739501"
---
# <a name="whats-new-windows-media-format-11-sdk"></a><span data-ttu-id="707b0-113">Nouveautés (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="707b0-113">What's New (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="707b0-114">Le kit de développement logiciel (SDK) Windows Media format 11 introduit de nouvelles fonctionnalités de gestion des droits numériques (DRM).</span><span class="sxs-lookup"><span data-stu-id="707b0-114">The Windows Media Format 11 SDK introduces new digital rights management (DRM) features.</span></span> <span data-ttu-id="707b0-115">Les modifications suivantes ont été apportées au kit de développement logiciel depuis la version 9,5.</span><span class="sxs-lookup"><span data-stu-id="707b0-115">The following changes have been made to the SDK since the 9.5 release.</span></span>

## <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="707b0-116">API étendues du client Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="707b0-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="707b0-117">Le kit de développement logiciel (SDK) Windows Media format 11 est fourni avec un nouvel ensemble d’API DRM.</span><span class="sxs-lookup"><span data-stu-id="707b0-117">The Windows Media Format 11 SDK ships with a new set of DRM APIs.</span></span> <span data-ttu-id="707b0-118">Ces API sont implémentées dans leur propre bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="707b0-118">These APIs are implemented in their own library.</span></span> <span data-ttu-id="707b0-119">La plupart des fonctionnalités DRM prises en charge par les objets du kit de développement logiciel (SDK) Windows Media format sont également prises en charge par les API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="707b0-119">Many of the DRM features supported by the objects of the Windows Media Format SDK are also supported by the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="707b0-120">La principale différence dans les nouvelles API est qu’elles ne s’appuient pas sur la présence d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="707b0-120">The primary difference in the new APIs is that they do not rely on having an ASF file to work.</span></span> <span data-ttu-id="707b0-121">Au lieu de cela, les nouvelles API traitent le magasin de licences local directement, en utilisant souvent l’ID de clé pour identifier les licences.</span><span class="sxs-lookup"><span data-stu-id="707b0-121">Instead, the new APIs deal with the local license store directly, often using the key ID to identify licenses.</span></span>

<span data-ttu-id="707b0-122">Pour plus d’informations, consultez la documentation sur les [API étendues du client Windows Media DRM](windows-media-drm-client-extended-apis.md) .</span><span class="sxs-lookup"><span data-stu-id="707b0-122">For more information, see the [Windows Media DRM Client Extended APIs](windows-media-drm-client-extended-apis.md) documentation.</span></span>

## <a name="updated-codecs"></a><span data-ttu-id="707b0-123">Codecs mis à jour</span><span class="sxs-lookup"><span data-stu-id="707b0-123">Updated Codecs</span></span>

<span data-ttu-id="707b0-124">Le codec du profil avancé Windows Media Video 9 a été mis à jour pour produire un flux binaire compressé conforme à la norme SMPTE VC-1.</span><span class="sxs-lookup"><span data-stu-id="707b0-124">The Windows Media Video 9 Advanced Profile codec has been updated to produce a compressed bit stream that is compliant with the published SMPTE VC-1 standard.</span></span>

<span data-ttu-id="707b0-125">Le codec Windows Media Audio 10 Professional est également inclus dans cette version du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="707b0-125">The Windows Media Audio 10 Professional codec is also included in this release of the SDK.</span></span> <span data-ttu-id="707b0-126">Le nouveau codec audio offre une qualité améliorée aux taux de bits inférieurs.</span><span class="sxs-lookup"><span data-stu-id="707b0-126">The new audio codec features improved quality at lower bit rates.</span></span>

## <a name="thumbnail-right"></a><span data-ttu-id="707b0-127">Miniature droite</span><span class="sxs-lookup"><span data-stu-id="707b0-127">Thumbnail Right</span></span>

<span data-ttu-id="707b0-128">Les applications peuvent demander une nouvelle action DRM pour lire à partir de la vidéo afin de créer une image miniature.</span><span class="sxs-lookup"><span data-stu-id="707b0-128">Applications can request a new DRM action to read from video to create a thumbnail image.</span></span> <span data-ttu-id="707b0-129">Cela permet aux applications de créer et d’afficher des images miniatures pour les fichiers vidéo sans ouvrir le fichier pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="707b0-129">This enables applications to create and display thumbnail images for video files without opening the file for playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="707b0-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="707b0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="707b0-131">**À propos du kit de développement logiciel (SDK) Windows Media format**</span><span class="sxs-lookup"><span data-stu-id="707b0-131">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




