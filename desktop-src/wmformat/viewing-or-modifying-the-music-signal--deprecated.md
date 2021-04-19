---
title: Affichage ou modification du signal musical (déconseillé)
description: Affichage ou modification du signal musical (déconseillé)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- gestion des droits numériques (DRM), Microsoft Secure audio Path (SAP)
- DRM (gestion des droits numériques), Microsoft Secure audio Path (SAP)
- Windows Media Format SDK, Secure audio Path (SAP)
- gestion des droits numériques (DRM), chemin audio sécurisé (SAP)
- DRM (gestion des droits numériques), chemin d’accès audio sécurisé (SAP)
- Windows Media Format SDK, musique signal (affichage ou modification)
- gestion des droits numériques (DRM), affichage ou modification des signaux musicaux
- DRM (gestion des droits numériques), affichage ou modification des signaux musicaux
- Microsoft Secure audio Path (SAP), affichage ou modification des signaux musicaux
- Chemin audio sécurisé (SAP), affichage ou modification d’un signal musical
- SAP (chemin d’accès audio sécurisé), affichage ou modification d’un signal musical
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513490"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a><span data-ttu-id="a0eb3-115">Affichage ou modification du signal musical (déconseillé)</span><span class="sxs-lookup"><span data-stu-id="a0eb3-115">Viewing or Modifying the Music Signal (deprecated)</span></span>

<span data-ttu-id="a0eb3-116">Cette page documente une fonctionnalité qui sera prise en charge avec une autre solution technique dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="a0eb3-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="a0eb3-117">Dans le modèle SAP (Secure audio Path) de Microsoft, les applications ne peuvent pas modifier la musique protégée de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="a0eb3-117">In the Microsoft Secure Audio Path (SAP) model, applications cannot modify protected music in any way.</span></span> <span data-ttu-id="a0eb3-118">Par exemple, lorsqu’une application tente d’intercepter un signal musical, le signal ressemble à un bruit aléatoire.</span><span class="sxs-lookup"><span data-stu-id="a0eb3-118">For example, when an application attempts to intercept a music signal, the signal sounds like random noise.</span></span> <span data-ttu-id="a0eb3-119">Par conséquent, les applications qui modifient normalement les signaux (par exemple, un égaliseur) ne peuvent pas modifier le son de la musique.</span><span class="sxs-lookup"><span data-stu-id="a0eb3-119">As a result, applications that normally modify signals (such as an equalizer) cannot change the sound of the music.</span></span>

<span data-ttu-id="a0eb3-120">Certaines applications affichent simplement un signal musical.</span><span class="sxs-lookup"><span data-stu-id="a0eb3-120">Some applications merely view a music signal.</span></span> <span data-ttu-id="a0eb3-121">Par exemple, certaines applications affichent des lumières clignotantes dans le temps avec le signal musical, mais ne les modifient pas.</span><span class="sxs-lookup"><span data-stu-id="a0eb3-121">For example, some applications display flashing lights in time with the music signal, but do not modify it.</span></span> <span data-ttu-id="a0eb3-122">Pour prendre en charge les applications qui affichent des signaux, une petite partie de la musique est déchiffrée et transmise sous forme claire avec le contenu chiffré.</span><span class="sxs-lookup"><span data-stu-id="a0eb3-122">To accommodate applications that view signals, a small part of the music is decrypted and passed in clear form with the encrypted content.</span></span> <span data-ttu-id="a0eb3-123">Le signal résultant est très médiocre (pire que la qualité téléphonique), mais peut suffire pour les applications qui affichent des signaux.</span><span class="sxs-lookup"><span data-stu-id="a0eb3-123">The resulting signal is very poor (worse than telephone quality) but can suffice for applications that view signals.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0eb3-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0eb3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0eb3-125">**Chemin d’accès audio sécurisé Microsoft**</span><span class="sxs-lookup"><span data-stu-id="a0eb3-125">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




