---
title: Désactivation de la sortie numérique (déconseillée)
description: Désactivation de la sortie numérique (déconseillée)
ms.assetid: 208ceb23-e0a0-4dee-aeba-e9d640248f75
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- gestion des droits numériques (DRM), Microsoft Secure audio Path (SAP)
- DRM (gestion des droits numériques), Microsoft Secure audio Path (SAP)
- Windows Media Format SDK, Secure audio Path (SAP)
- gestion des droits numériques (DRM), chemin audio sécurisé (SAP)
- DRM (gestion des droits numériques), chemin d’accès audio sécurisé (SAP)
- Microsoft Secure audio Path (SAP), désactivation de la sortie numérique
- Chemin d’accès audio sécurisé (SAP), désactivation de la sortie numérique
- SAP (chemin d’accès audio sécurisé), désactivation de la sortie numérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a667034d6b56a3f764865205681847b195eaaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380380"
---
# <a name="disabling-digital-output-deprecated"></a><span data-ttu-id="6d275-112">Désactivation de la sortie numérique (déconseillée)</span><span class="sxs-lookup"><span data-stu-id="6d275-112">Disabling Digital Output (deprecated)</span></span>

<span data-ttu-id="6d275-113">Cette page documente une fonctionnalité qui sera prise en charge avec une autre solution technique dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="6d275-113">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="6d275-114">Une autre fonctionnalité de Microsoft Secure audio Path est la possibilité de désactiver la sortie numérique.</span><span class="sxs-lookup"><span data-stu-id="6d275-114">Another feature of Microsoft Secure Audio Path is the ability to disable digital output.</span></span> <span data-ttu-id="6d275-115">Certaines cartes son offrent un moyen d’envoyer une sortie numérique à partir d’un périphérique matériel. ces appareils peuvent être certifiés et passer l’autorisation du composant de noyau DRM.</span><span class="sxs-lookup"><span data-stu-id="6d275-115">Certain sound cards provide a way to send digital output from a hardware device; these devices might be certified and will pass authorization from the DRM kernel component.</span></span> <span data-ttu-id="6d275-116">Par conséquent, si une sortie numérique est activée pour une carte son légitime, les gens peuvent toujours capturer un enregistrement numérique parfait de musique protégée.</span><span class="sxs-lookup"><span data-stu-id="6d275-116">So, if a legitimate sound card has digital output enabled, people can still capture a perfect digital recording of protected music.</span></span>

<span data-ttu-id="6d275-117">Cette fonctionnalité permet aux propriétaires de contenu ou aux émetteurs de licence de désactiver la sortie numérique en définissant un paramètre dans licences pour leur musique.</span><span class="sxs-lookup"><span data-stu-id="6d275-117">This feature lets content owners or license issuers disable digital output by setting a parameter in licenses for their music.</span></span> <span data-ttu-id="6d275-118">Si ce paramètre est défini, la carte son désactive la fonctionnalité de sortie numérique lors de la diffusion de musique protégée.</span><span class="sxs-lookup"><span data-stu-id="6d275-118">If this parameter is set, the sound card disables its digital output capability when playing protected music.</span></span> <span data-ttu-id="6d275-119">Les utilisateurs peuvent écouter la musique déchiffrée, mais ils ne peuvent pas effectuer de copies.</span><span class="sxs-lookup"><span data-stu-id="6d275-119">Users can listen to decrypted music, but they cannot make copies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d275-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6d275-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d275-121">**Chemin d’accès audio sécurisé Microsoft**</span><span class="sxs-lookup"><span data-stu-id="6d275-121">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




