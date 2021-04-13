---
title: Notions de base de DRM
description: Notions de base de DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- SDK Windows Media format, principes de base de DRM
- gestion des droits numériques (DRM), à propos de
- DRM (gestion des droits numériques), à propos de
- gestion des droits numériques (DRM), protection du contenu
- DRM (gestion des droits numériques), protection du contenu
- gestion des droits numériques (DRM), empaquetage de contenu
- DRM (gestion des droits numériques), empaquetage de contenu
- gestion des droits numériques (DRM), lecture de contenu protégé
- DRM (gestion des droits numériques), lecture de contenu protégé
- protection du contenu
- contenu de l’empaquetage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380377"
---
# <a name="drm-basics"></a><span data-ttu-id="7a4dc-114">Notions de base de DRM</span><span class="sxs-lookup"><span data-stu-id="7a4dc-114">DRM Basics</span></span>

<span data-ttu-id="7a4dc-115">Les technologies Windows Media DRM sont relativement simples du point de vue du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-115">The Windows Media DRM technologies are fairly simple from the perspective of the Windows Media Format SDK.</span></span> <span data-ttu-id="7a4dc-116">Les composants du kit de développement logiciel (SDK) peuvent être utilisés pour protéger du contenu et pour lire du contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-116">Components of the SDK can be used to protect content and to play protected content.</span></span>

## <a name="protecting-content"></a><span data-ttu-id="7a4dc-117">Protection du contenu</span><span class="sxs-lookup"><span data-stu-id="7a4dc-117">Protecting Content</span></span>

<span data-ttu-id="7a4dc-118">La protection du contenu (également appelé contenu d’empaquetage) consiste à chiffrer la section des données du fichier et à inclure des informations dans l’en-tête de fichier qui permet aux joueurs de déchiffrer le contenu.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-118">Protecting content (also called packaging content) involves encrypting the data section of the file and including some information in the file header that enables players to decrypt the content.</span></span>

<span data-ttu-id="7a4dc-119">Pour chiffrer le contenu, vous avez besoin d’une clé, qui est une valeur utilisée pour amorcer les algorithmes de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-119">To encrypt the content, you need a key, which is a value used to seed the encryption algorithms.</span></span> <span data-ttu-id="7a4dc-120">Une clé est constituée de deux parties : une valeur initiale de clé (ou une clé privée) et un identificateur de clé (ou une clé publique).</span><span class="sxs-lookup"><span data-stu-id="7a4dc-120">A key is made up of two pieces: a key seed (or private key), and a key identifier (or public key).</span></span> <span data-ttu-id="7a4dc-121">La valeur initiale de la clé est la valeur secrète avec laquelle vous encodez du contenu.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-121">The key seed is the secret value with which you encode content.</span></span> <span data-ttu-id="7a4dc-122">L’identificateur de clé est une valeur publique qui est incluse dans l’en-tête d’un fichier protégé.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-122">The key identifier is a public value that is included in the header of a protected file.</span></span>

<span data-ttu-id="7a4dc-123">Lorsqu’un fichier est protégé, il ne peut pas être déchiffré sans licence.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-123">When a file is protected, it cannot be decrypted without a license.</span></span> <span data-ttu-id="7a4dc-124">Une licence contient des informations qui spécifient les conditions d’utilisation du contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-124">A license includes information that specifies the terms of use for the protected content.</span></span> <span data-ttu-id="7a4dc-125">Les termes d’une licence sont choisis par le propriétaire du contenu et peuvent être personnalisés pour répondre à un large éventail de besoins.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-125">The terms of a license are decided by the content owner and can be customized to meet a variety of needs.</span></span> <span data-ttu-id="7a4dc-126">Une partie du processus d’empaquetage d’un fichier consiste à inclure l’URL d’une page Web où les utilisateurs peuvent acquérir une licence pour accéder au contenu.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-126">Part of the process of packaging a file is to include the URL of a Web page where users can acquire a license to access the content.</span></span>

## <a name="reading-protected-content"></a><span data-ttu-id="7a4dc-127">Lecture du contenu protégé</span><span class="sxs-lookup"><span data-stu-id="7a4dc-127">Reading Protected Content</span></span>

<span data-ttu-id="7a4dc-128">Pour lire du contenu protégé, une licence pour le contenu doit résider sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-128">To read protected content, a license for the content must reside on the client computer.</span></span> <span data-ttu-id="7a4dc-129">Certaines restrictions de licence sont vérifiées en interne par les composants DRM du kit de développement logiciel (SDK) du format Windows Media, tandis que d’autres doivent être appliqués par votre application.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-129">Some license restrictions are checked internally by the DRM components of the Windows Media Format SDK, while others must be enforced by your application.</span></span>

<span data-ttu-id="7a4dc-130">Vous pouvez utiliser les objets du kit de développement logiciel (SDK) de format Windows Media pour aider l’utilisateur à acquérir des licences pour du contenu et à effectuer d’autres tâches administratives, telles que la mise à jour des composants DRM et la sauvegarde des licences.</span><span class="sxs-lookup"><span data-stu-id="7a4dc-130">You can use the objects of the Windows Media Format SDK to assist the user in acquiring licenses for content and to perform other administrative tasks, such as updating DRM components and backing up licenses.</span></span>

> [!Note]  
> <span data-ttu-id="7a4dc-131">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="7a4dc-131">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7a4dc-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a4dc-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a4dc-133">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="7a4dc-133">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="7a4dc-134">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="7a4dc-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




