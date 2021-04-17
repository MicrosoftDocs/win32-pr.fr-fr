---
title: Le modèle de chemin d’accès audio sécurisé (déconseillé)
description: Le modèle de chemin d’accès audio sécurisé (déconseillé)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- gestion des droits numériques (DRM), Microsoft Secure audio Path (SAP)
- DRM (gestion des droits numériques), Microsoft Secure audio Path (SAP)
- Windows Media Format SDK, Secure audio Path (SAP)
- gestion des droits numériques (DRM), chemin audio sécurisé (SAP)
- DRM (gestion des droits numériques), chemin d’accès audio sécurisé (SAP)
- Microsoft Secure audio Path (SAP), modèle
- Chemin d’accès audio sécurisé (SAP), modèle
- SAP (chemin d’accès audio sécurisé), modèle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee21d05113deb3c4e8d64141374c87da090f41c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379837"
---
# <a name="the-secure-audio-path-model-deprecated"></a><span data-ttu-id="36d1d-112">Le modèle de chemin d’accès audio sécurisé (déconseillé)</span><span class="sxs-lookup"><span data-stu-id="36d1d-112">The Secure Audio Path Model (deprecated)</span></span>

<span data-ttu-id="36d1d-113">Cette page documente une fonctionnalité qui sera prise en charge avec une autre solution technique dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="36d1d-113">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="36d1d-114">Le protocole SAP (Secure audio Path) de Microsoft est une fonctionnalité de Microsoft Windows® me et de Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="36d1d-114">Microsoft Secure Audio Path (SAP) is a feature of Microsoft Windows® Me and Microsoft Windows XP.</span></span> <span data-ttu-id="36d1d-115">La nécessité de lire un fichier audio uniquement via un chemin d’accès audio sécurisé est spécifiée dans la licence DRM et appliquée par les composants du client DRM.</span><span class="sxs-lookup"><span data-stu-id="36d1d-115">The requirement that an audio file be played only through a secure audio path is specified in the DRM license and enforced by the DRM client components.</span></span> <span data-ttu-id="36d1d-116">Aucun chiffrement supplémentaire n’est ajouté pour les fichiers SAP uniquement lorsqu’ils sont protégés initialement.</span><span class="sxs-lookup"><span data-stu-id="36d1d-116">There is no extra encryption added for SAP-only files when they are initially protected.</span></span> <span data-ttu-id="36d1d-117">Le chiffrement SAP est ajouté automatiquement par les composants DRM au moment de la lecture, comme le processus d’authentification pour tous les composants logiciels impliqués dans la lecture.</span><span class="sxs-lookup"><span data-stu-id="36d1d-117">The SAP encryption is added automatically by the DRM components at playback time, as is the authentication process for all software components involved in playback.</span></span> <span data-ttu-id="36d1d-118">Le fonctionnement de SAP est donc complètement transparent pour les applications. c’est pourquoi il n’existe aucune méthode ou propriété dans le kit de développement logiciel (SDK) de format Windows Media pour l’activation ou la désactivation de SAP.</span><span class="sxs-lookup"><span data-stu-id="36d1d-118">The workings of SAP are therefore completely transparent to applications, and that is why there is no method or property in the Windows Media Format SDK for enabling or disabling SAP.</span></span> <span data-ttu-id="36d1d-119">Si vous le souhaitez, lors de la création d’un fichier protégé, le propriétaire du contenu peut ajouter un attribut d’en-tête personnalisé appelé « DRMHeader. SAPRequired » afin d’indiquer à un serveur de licences d’ajouter les exigences SAP à la licence.</span><span class="sxs-lookup"><span data-stu-id="36d1d-119">If desired, when creating a protected file a content owner can add a custom header attribute called something like "DRMHeader.SAPRequired" in order to instruct a license server to add the SAP requirement to the license.</span></span> <span data-ttu-id="36d1d-120">L’implémentation d’un tel schéma est jusqu’au propriétaire du contenu et au service de licence.</span><span class="sxs-lookup"><span data-stu-id="36d1d-120">The implementation of such a scheme is up to the content owner and the license service.</span></span>

<span data-ttu-id="36d1d-121">Dans le modèle DRM actuel, si SAP n’est pas appliqué, lorsque la musique numérique protégée est jouée, le contenu chiffré passe au composant client DRM.</span><span class="sxs-lookup"><span data-stu-id="36d1d-121">In the current DRM model, if SAP is not applied, when protected digital music is played, the encrypted content passes to the DRM client component.</span></span> <span data-ttu-id="36d1d-122">Le client DRM vérifie que l’application et le composant DRM incorporant le kit de développement logiciel (SDK) du format Windows Media sont valides.</span><span class="sxs-lookup"><span data-stu-id="36d1d-122">The DRM client verifies that the application and the DRM component incorporating the Windows Media Format SDK are valid.</span></span> <span data-ttu-id="36d1d-123">S’ils sont valides, le client DRM déchiffre le contenu et l’envoie à l’application, qui l’envoie ensuite aux composants audio de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="36d1d-123">If they are valid, the DRM client decrypts the content and sends it to the application, which then sends it to the lower-level audio components.</span></span> <span data-ttu-id="36d1d-124">À ce stade, la musique déchiffrée est disponible pour les applications en mode utilisateur et les plug-ins et les pilotes en mode noyau qui peuvent intercepter les bits audio déchiffrés.</span><span class="sxs-lookup"><span data-stu-id="36d1d-124">At this point, the decrypted music is available to user mode applications and plug-ins and kernel mode drivers that can intercept the decrypted audio bits.</span></span>

<span data-ttu-id="36d1d-125">Lorsque la spécification du chemin d’accès audio sécurisé est appliquée, le contenu n’est pas déchiffré par l’application, mais il est transmis dans un État chiffré à des composants de niveau inférieur, tous ayant été authentifiés par Microsoft comme dignes de confiance.</span><span class="sxs-lookup"><span data-stu-id="36d1d-125">When the Secure Audio Path requirement is applied, the content is not decrypted by the application, but rather is passed in an encrypted state to lower level components, all of which have been authenticated by Microsoft as trustworthy.</span></span> <span data-ttu-id="36d1d-126">Un composant audio approuvé est un composant qui ne met pas le contenu audio à la disposition d’un composant système, à l’exception d’autres composants de confiance spécifiques.</span><span class="sxs-lookup"><span data-stu-id="36d1d-126">A trusted audio component is one that does not make the audio content available to any system component except other specific trusted components.</span></span> <span data-ttu-id="36d1d-127">De cette façon, le contenu numérique reste protégé jusqu’au niveau du pilote.</span><span class="sxs-lookup"><span data-stu-id="36d1d-127">In this way, the digital content remains protected all the way down to the driver level.</span></span>

<span data-ttu-id="36d1d-128">Le diagramme suivant affiche le modèle actuel par rapport au modèle de chemin d’accès audio sécurisé.</span><span class="sxs-lookup"><span data-stu-id="36d1d-128">The following diagram displays the current model in comparison to the Secure Audio Path model.</span></span>

![diagramme du modèle de chemin d’accès audio sécurisé](images/sap.png)

 

 




