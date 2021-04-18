---
title: Vue d’ensemble de Windows Media DRM
description: Vue d’ensemble de Windows Media DRM
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, licences DRM
- Windows Media Format SDK, licences pour DRM
- gestion des droits numériques (DRM), à propos de
- DRM (gestion des droits numériques), à propos de
- gestion des droits numériques (DRM), empaquetage de fichiers Windows Media
- DRM (gestion des droits numériques), empaquetage de fichiers Windows Media
- gestion des droits numériques (DRM), gestion des licences de fichiers protégés
- DRM (gestion des droits numériques), gestion des licences de fichiers protégés
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), lecture des fichiers protégés
- DRM (gestion des droits numériques), lecture des fichiers protégés
- ASF (Advanced Systems Format), gestion des droits numériques (DRM)
- ASF (format de systèmes avancés), gestion des droits numériques (DRM)
- licences, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512433"
---
# <a name="overview-of-windows-media-drm"></a><span data-ttu-id="18049-119">Vue d’ensemble de Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="18049-119">Overview of Windows Media DRM</span></span>

<span data-ttu-id="18049-120">La Rights Management Windows Media Digital (DRM) est un système de protection du contenu des fichiers Windows Media afin que les utilisateurs non autorisés ne puissent pas y accéder.</span><span class="sxs-lookup"><span data-stu-id="18049-120">Windows Media Digital Rights Management (DRM) is a system for protecting the content in Windows Media files so that unauthorized users cannot access it.</span></span> <span data-ttu-id="18049-121">Il existe trois phases pour le cycle DRM de base : l’empaquetage, la gestion des licences et la lecture.</span><span class="sxs-lookup"><span data-stu-id="18049-121">There are three phases to the basic DRM cycle: packaging, licensing, and reading.</span></span>

## <a name="packaging-windows-media-files"></a><span data-ttu-id="18049-122">Empaquetage de fichiers Windows Media</span><span class="sxs-lookup"><span data-stu-id="18049-122">Packaging Windows Media Files</span></span>

<span data-ttu-id="18049-123">Windows Media DRM est conçu pour fonctionner avec les fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="18049-123">Windows Media DRM is designed to work with Windows Media files.</span></span> <span data-ttu-id="18049-124">Un fichier Windows Media est un fichier conforme à la spécification ASF (Advanced Systems Format) et qui contient uniquement des données audio et vidéo qui ont été compressées à l’aide de la Windows Media Audio et des codecs vidéo.</span><span class="sxs-lookup"><span data-stu-id="18049-124">A Windows Media file is a file that conforms to the Advanced Systems Format (ASF) specification and only contains Audio and Video that has been compressed by using the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="18049-125">Lorsqu’un fichier ASF est empaqueté, une section spécifique à DRM est ajoutée à l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="18049-125">When an ASF file is packaged, a DRM-specific section is added to the header.</span></span> <span data-ttu-id="18049-126">L’en-tête DRM contient un ID de clé qui identifie le contenu à des fins de licence, et une URL d’acquisition de licence, qui est l’adresse d’une page Web qui peut émettre des licences pour lire le contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="18049-126">The DRM header contains a Key ID, which identifies the content for the purposes of licensing, and a license acquisition URL, which is the address of a Web page that can issue licenses to read the protected content.</span></span> <span data-ttu-id="18049-127">Il existe bien d’autres informations qui peuvent être placées dans l’en-tête DRM, mais elles sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="18049-127">There is much more information that can be put in the DRM header, but it is optional.</span></span> <span data-ttu-id="18049-128">L’en-tête DRM est signé afin que le gestionnaire de package puisse être vérifié.</span><span class="sxs-lookup"><span data-stu-id="18049-128">The DRM header is signed so that the packager can be verified.</span></span>

<span data-ttu-id="18049-129">Le contenu du fichier ASF est chiffré pendant le processus de compression.</span><span class="sxs-lookup"><span data-stu-id="18049-129">The content in the ASF file is encrypted during the packing process.</span></span> <span data-ttu-id="18049-130">Toutefois, les informations suivantes dans le fichier empaqueté sont disponibles, même pour les clients qui n’ont pas de licence :</span><span class="sxs-lookup"><span data-stu-id="18049-130">However, the following information in the packaged file is available even to clients that do not have a license:</span></span>

-   <span data-ttu-id="18049-131">Métadonnées stockées dans l’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="18049-131">Metadata that is stored in the ASF header.</span></span>
-   <span data-ttu-id="18049-132">Certaines métadonnées stockées dans l’en-tête DRM (par exemple, vous pouvez toujours obtenir l’URL d’acquisition de licence).</span><span class="sxs-lookup"><span data-stu-id="18049-132">Some metadata that is stored in the DRM header (for example, you can always get the license acquisition URL).</span></span>

## <a name="licensing-protected-files"></a><span data-ttu-id="18049-133">Gestion des licences des fichiers protégés</span><span class="sxs-lookup"><span data-stu-id="18049-133">Licensing Protected Files</span></span>

<span data-ttu-id="18049-134">Pour qu’un fichier empaqueté soit lu, une licence doit être émise sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="18049-134">For a packaged file to be read, a license must be issued to the client computer.</span></span> <span data-ttu-id="18049-135">Une licence est un ensemble de données décrivant les conditions dans lesquelles les données des fichiers protégés peuvent être lues.</span><span class="sxs-lookup"><span data-stu-id="18049-135">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="18049-136">La plupart du temps, une licence est émise pour un fichier protégé en réponse à l’utilisateur qui tente d’effectuer une opération sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="18049-136">Most often, a license is issued for a protected file in response to the user trying to perform some operation on the file.</span></span> <span data-ttu-id="18049-137">Toutefois, il est également possible qu’un émetteur de licence remette des licences à un client avant qu’il ne soit demandé explicitement.</span><span class="sxs-lookup"><span data-stu-id="18049-137">It is also possible, however, for a license issuer to deliver licenses to a client before it is explicitly requested.</span></span> <span data-ttu-id="18049-138">Pour plus d’informations sur les licences, consultez [licences](licenses.md).</span><span class="sxs-lookup"><span data-stu-id="18049-138">For more information about licenses, see [Licenses](licenses.md).</span></span>

## <a name="reading-data-from-protected-files"></a><span data-ttu-id="18049-139">Lecture de données à partir de fichiers protégés</span><span class="sxs-lookup"><span data-stu-id="18049-139">Reading Data from Protected Files</span></span>

<span data-ttu-id="18049-140">Lorsqu’un utilisateur tente d’effectuer une opération sur un fichier protégé (lire, graver sur un CD-ROM, copier sur un appareil, etc.), l’application doit vérifier les licences du contenu sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="18049-140">When a user tries to perform an operation on a protected file (play, burn to CD, copy to a device, and so on), the application must check for licenses for the content on the client computer.</span></span> <span data-ttu-id="18049-141">Si une licence valide existe sur l’ordinateur client, l’opération peut se poursuivre.</span><span class="sxs-lookup"><span data-stu-id="18049-141">If a valid license exists on the client computer, the operation can proceed.</span></span> <span data-ttu-id="18049-142">S’il n’existe aucune licence pour le contenu, ou si aucune licence pour le contenu de l’ordinateur client n’autorise l’action demandée, une licence doit être acquise.</span><span class="sxs-lookup"><span data-stu-id="18049-142">If there isn't a license for the content, or if no license for the content that is on the client computer allows the requested action, then a license must be acquired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18049-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18049-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18049-144">**À propos des API étendues du client Windows Media DRM**</span><span class="sxs-lookup"><span data-stu-id="18049-144">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




