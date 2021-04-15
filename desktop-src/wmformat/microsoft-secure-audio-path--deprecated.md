---
title: Chemin d’accès audio sécurisé Microsoft (déconseillé)
description: Chemin d’accès audio sécurisé Microsoft (déconseillé)
ms.assetid: 55833ca4-b25b-408c-af66-f89e9b6110c9
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- gestion des droits numériques (DRM), Microsoft Secure audio Path (SAP)
- DRM (gestion des droits numériques), Microsoft Secure audio Path (SAP)
- Windows Media Format SDK, Secure audio Path (SAP)
- gestion des droits numériques (DRM), chemin audio sécurisé (SAP)
- DRM (gestion des droits numériques), chemin d’accès audio sécurisé (SAP)
- Microsoft Secure audio Path (SAP), à propos de
- Chemin audio sécurisé (SAP), à propos de
- SAP (chemin d’accès audio sécurisé), à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f57111aaa9b020c4efbd1635c602f9c917d02
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321393"
---
# <a name="microsoft-secure-audio-path-deprecated"></a><span data-ttu-id="914d2-112">Chemin d’accès audio sécurisé Microsoft (déconseillé)</span><span class="sxs-lookup"><span data-stu-id="914d2-112">Microsoft Secure Audio Path (deprecated)</span></span>

<span data-ttu-id="914d2-113">Cette page documente une fonctionnalité qui sera prise en charge avec une autre solution technique dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="914d2-113">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="914d2-114">Les créateurs et les serveurs de distribution de contenu peuvent spécifier, dans une licence DRM, qu’un fichier audio ne peut être lu que sur un système avec des composants SAP (Secure audio Path) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="914d2-114">Content creators and distributors can specify in a DRM license that an audio file is only allowed to be played on a system with Microsoft Secure Audio Path (SAP) components.</span></span> <span data-ttu-id="914d2-115">Le chemin d’accès audio sécurisé fournit un degré de protection plus élevé du contenu audio en rendant pratiquement impossible aux applications non fiables ou aux pilotes audio d’accéder aux bits audio non chiffrés.</span><span class="sxs-lookup"><span data-stu-id="914d2-115">Secure Audio Path provides a much higher degree of protection to audio content by making it virtually impossible for untrusted applications or audio drivers to access the unencrypted audio bits.</span></span> <span data-ttu-id="914d2-116">Le chemin d’accès audio sécurisé est pris en charge sur Microsoft Windows® me et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="914d2-116">Secure Audio Path is supported on Microsoft Windows® Me and Windows XP.</span></span> <span data-ttu-id="914d2-117">Il sécurise la musique numérique dans le noyau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="914d2-117">It secures digital music in the operating system kernel.</span></span> <span data-ttu-id="914d2-118">En outre, le copyright de Digital Millennium fait de contourner les mesures antipiratages dans les logiciels d’un crime.</span><span class="sxs-lookup"><span data-stu-id="914d2-118">In addition, the Digital Millennium Copyright Act makes circumventing antipiracy measures in software a crime.</span></span>

<span data-ttu-id="914d2-119">Le chemin d’accès audio sécurisé est activé et implémenté entièrement automatiquement par le composant Microsoft DRM quand une licence DRM requiert SAP.</span><span class="sxs-lookup"><span data-stu-id="914d2-119">Secure Audio Path is activated and implemented completely automatically by the Microsoft DRM component when a DRM license requires SAP.</span></span> <span data-ttu-id="914d2-120">Pour les applications qui s’exécutent sur Windows® XP Service Pack 1, vous pouvez activer le chiffrement SAP pour tout contenu audio, en dehors du contexte de la solution DRM Microsoft, à l’aide du kit de développement logiciel (SDK) Secure audio Path.</span><span class="sxs-lookup"><span data-stu-id="914d2-120">For applications running on Windows® XP Service Pack 1, you can enable SAP encryption to any audio content, outside the context of the Microsoft DRM solution, by using the Secure Audio Path SDK.</span></span> <span data-ttu-id="914d2-121">Pour plus d’informations sur le kit de développement logiciel (SDK) Secure audio Path, consultez le [site Web Microsoft](/documentation/).</span><span class="sxs-lookup"><span data-stu-id="914d2-121">For more information on the Secure Audio Path SDK, see the [Microsoft Web site](/documentation/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="914d2-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="914d2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="914d2-123">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="914d2-123">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> </dl>

 

 