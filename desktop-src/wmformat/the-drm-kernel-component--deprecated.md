---
title: Composant de noyau DRM (déconseillé)
description: Composant de noyau DRM (déconseillé)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- gestion des droits numériques (DRM), Microsoft Secure audio Path (SAP)
- DRM (gestion des droits numériques), Microsoft Secure audio Path (SAP)
- Windows Media Format SDK, Secure audio Path (SAP)
- gestion des droits numériques (DRM), chemin audio sécurisé (SAP)
- DRM (gestion des droits numériques), chemin d’accès audio sécurisé (SAP)
- Kit de développement logiciel (SDK) Windows Media format, composant de noyau DRM
- gestion des droits numériques (DRM), composant de noyau
- DRM (gestion des droits numériques), composant de noyau
- Microsoft Secure audio Path (SAP), composant noyau DRM
- Chemin audio sécurisé (SAP), composant de noyau DRM
- SAP (chemin d’accès audio sécurisé), composant de noyau DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacc0074fdf390ca478ed41b59188ad42ec193c1
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032072"
---
# <a name="the-drm-kernel-component-deprecated"></a><span data-ttu-id="1fa53-115">Composant de noyau DRM (déconseillé)</span><span class="sxs-lookup"><span data-stu-id="1fa53-115">The DRM Kernel Component (deprecated)</span></span>

<span data-ttu-id="1fa53-116">Cette page documente une fonctionnalité qui sera prise en charge avec une autre solution technique dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="1fa53-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="1fa53-117">Dans le modèle Microsoft Secure audio Path (SAP), le composant de noyau DRM fournit deux fonctionnalités de base qui protègent l’intégrité de la musique chiffrée.</span><span class="sxs-lookup"><span data-stu-id="1fa53-117">In the Microsoft Secure Audio Path (SAP) model, the DRM kernel component provides two basic features that protect the integrity of encrypted music.</span></span>

<span data-ttu-id="1fa53-118">Tout d’abord, le composant client DRM et le composant de noyau DRM sont en communication lorsqu’un fichier musical est lu.</span><span class="sxs-lookup"><span data-stu-id="1fa53-118">First, the DRM client component and the DRM kernel component are in communication when a music file is played.</span></span> <span data-ttu-id="1fa53-119">Cette communication entre les composants empêche quiconque de falsifier le signal chiffré ou d’insérer des informations erronées.</span><span class="sxs-lookup"><span data-stu-id="1fa53-119">This communication between components prevents anyone from tampering with the encrypted signal or from inserting false information.</span></span>

<span data-ttu-id="1fa53-120">Deuxièmement, le composant de noyau DRM ne déchiffre pas le signal musical tant que tous les composants restants n’ont pas été authentifiés.</span><span class="sxs-lookup"><span data-stu-id="1fa53-120">Second, the DRM kernel component does not decrypt the music signal until all remaining components are authenticated.</span></span> <span data-ttu-id="1fa53-121">Autrement dit, avant de déchiffrer le contenu et de le passer au composant système suivant, le composant de noyau DRM vérifie chaque composant qui reste dans le chemin d’accès à la carte son (chaque composant pouvant accéder au contenu) et vérifie que ces composants sont signés avec un certificat de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1fa53-121">That is, before decrypting content and passing it to the next system component, the DRM kernel component checks each component that remains in the path to the sound card (each component that can access the content) and verifies that these components are signed with a certificate from Microsoft.</span></span> <span data-ttu-id="1fa53-122">Un composant non signé peut indiquer un composant suspect ou un pilote malveillant.</span><span class="sxs-lookup"><span data-stu-id="1fa53-122">An unsigned component might indicate a suspicious component or a malicious driver.</span></span> <span data-ttu-id="1fa53-123">Ainsi, lorsque le composant de noyau DRM valide les composants restants, si un composant échoue à ce test, le signal s’arrête et ne peut pas être lu.</span><span class="sxs-lookup"><span data-stu-id="1fa53-123">So, when the DRM kernel component validates remaining components, if any component fails this test, the signal is halted and cannot be played.</span></span> <span data-ttu-id="1fa53-124">Dans le cas contraire, si tous les composants sont validés, le composant de noyau DRM déchiffre la musique et le transmet au composant suivant.</span><span class="sxs-lookup"><span data-stu-id="1fa53-124">Otherwise, if all components pass validation, the DRM kernel component decrypts the music and passes it to the next component.</span></span>

<span data-ttu-id="1fa53-125">Microsoft signe numériquement les pilotes qui réussissent les tests WHQL (Windows® Hardware Quality Lab) pour assurer aux utilisateurs qu’ils utilisent les pilotes de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="1fa53-125">Microsoft digitally signs drivers that pass the Windows® Hardware Quality Lab (WHQL) tests to assure users that they are using the highest-quality drivers.</span></span> <span data-ttu-id="1fa53-126">Cette pratique est standard et garantit l’authenticité des composants, car la signature ne peut pas être falsifiée et le code ne peut pas être modifié sans détruire la signature.</span><span class="sxs-lookup"><span data-stu-id="1fa53-126">This practice is standard and guarantees the authenticity of components because the signature cannot be forged, nor can the code be modified without destroying the signature.</span></span> <span data-ttu-id="1fa53-127">Les pilotes certifiés pour le chemin d’accès audio sécurisé doivent protéger les données audio qu’ils traitent de l’accès par des composants non fiables.</span><span class="sxs-lookup"><span data-stu-id="1fa53-127">Drivers that are certified for Secure Audio Path must protect the audio data they process from access by untrusted components.</span></span> 

<span data-ttu-id="1fa53-128">Les pilotes inclus dans Windows Millennium Edition et Windows XP sont mis à jour pour un chemin d’accès audio sécurisé et signés.</span><span class="sxs-lookup"><span data-stu-id="1fa53-128">Drivers included with Windows Millennium Edition and Windows XP are updated for Secure Audio Path and signed.</span></span> <span data-ttu-id="1fa53-129">Les pilotes qui ne sont pas signés pour une utilisation avec Windows me ou Windows XP ne peuvent pas lire de musique protégée.</span><span class="sxs-lookup"><span data-stu-id="1fa53-129">Drivers that are not signed for use with Windows Me or Windows XP cannot play protected music.</span></span> <span data-ttu-id="1fa53-130">Les fabricants de pilotes peuvent réémettre des versions mises à jour de leurs pilotes qui sont signés par WHQL et les publier sur Internet pour que les clients puissent les télécharger.</span><span class="sxs-lookup"><span data-stu-id="1fa53-130">Driver manufacturers can reissue updated versions of their drivers that are signed by WHQL, and publish them on the Internet for consumers to download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fa53-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1fa53-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fa53-132">**Chemin d’accès audio sécurisé Microsoft**</span><span class="sxs-lookup"><span data-stu-id="1fa53-132">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




