---
title: Individualiser des applications DRM
description: Individualiser des applications DRM
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows Media Format SDK, individualisation des applications DRM
- Windows Media Format SDK, application individualisation
- ASF (Advanced Systems Format), individualisation des applications DRM
- ASF (format des systèmes avancés), individualisation des applications DRM
- ASF (Advanced Systems Format), application d’individualisation
- ASF (format des systèmes avancés), individualisation des applications
- gestion des droits numériques (DRM), individualisation des applications
- DRM (gestion des droits numériques), individualisation des applications
- gestion des droits numériques (DRM), individualisation des applications
- DRM (gestion des droits numériques), individualisation des applications
- individualisation de l’application
- individualiser des applications DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103940752"
---
# <a name="individualizing-drm-applications"></a><span data-ttu-id="57b5e-115">Individualiser des applications DRM</span><span class="sxs-lookup"><span data-stu-id="57b5e-115">Individualizing DRM Applications</span></span>

<span data-ttu-id="57b5e-116">Pour accroître la sécurité, le composant DRM des applications peut être *individualisé*.</span><span class="sxs-lookup"><span data-stu-id="57b5e-116">To increase security, the DRM component of applications can be *individualized*.</span></span> <span data-ttu-id="57b5e-117">Une application individualisée est une application qui a reçu une mise à niveau vers ses composants DRM qui la différencie de toutes les autres copies de la même application.</span><span class="sxs-lookup"><span data-stu-id="57b5e-117">An individualized application is one that has received an upgrade to its DRM components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="57b5e-118">Les propriétaires de contenu peuvent exiger que leurs fichiers protégés soient lus uniquement sur une application qui a été individualisée.</span><span class="sxs-lookup"><span data-stu-id="57b5e-118">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

<span data-ttu-id="57b5e-119">Le processus d’individualisation démarre lorsque l’application contacte le service d’individualisation Microsoft, qui installe ensuite une mise à niveau de sécurité sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57b5e-119">The individualization process starts when the application contacts the Microsoft Individualization Service, which then installs a security upgrade on the user's computer.</span></span> <span data-ttu-id="57b5e-120">Étant donné que le service d’individualisation gère les informations de l’utilisateur, vous devez afficher la politique de confidentialité de Microsoft ou fournir un lien vers cette page sur le site Web de Microsoft : <https://privacy.microsoft.com/privacystatement> .</span><span class="sxs-lookup"><span data-stu-id="57b5e-120">Because the Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft Web site: <https://privacy.microsoft.com/privacystatement>.</span></span>

<span data-ttu-id="57b5e-121">L’individualisation peut être effectuée de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="57b5e-121">Individualization can be accomplished in different ways.</span></span> <span data-ttu-id="57b5e-122">Par exemple, une individualisation peut avoir lieu lorsqu’un utilisateur lit un fichier protégé.</span><span class="sxs-lookup"><span data-stu-id="57b5e-122">For example, individualization can take place when a user plays a protected file.</span></span> <span data-ttu-id="57b5e-123">La demande de licence est envoyée au [*service de licence Windows Media*](wmformat-glossary.md), qui inspecte le certificat de l’application demandant la [*licence*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="57b5e-123">The license request is sent to the [*Windows Media License Service*](wmformat-glossary.md), which inspects the certificate of the application requesting the [*license*](wmformat-glossary.md).</span></span> <span data-ttu-id="57b5e-124">Si le composant DRM de l’application n’a pas été individualisé, le service de licence Windows Media refuse d’émettre la licence, car il s’agit de la stratégie du service de licence Windows Media pour émettre des licences uniquement pour des joueurs individuels.</span><span class="sxs-lookup"><span data-stu-id="57b5e-124">If the DRM component of the application has not been individualized, Windows Media License Service refuses to issue the license, because it is the policy of Windows Media License Service to issue licenses only to individualized players.</span></span> <span data-ttu-id="57b5e-125">L’application peut ensuite informer l’utilisateur que l’application doit être mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="57b5e-125">The application can then notify the user that the application must be upgraded.</span></span> <span data-ttu-id="57b5e-126">Si l’utilisateur accepte, une mise à niveau de sécurité est fournie pour individualiser le composant DRM de l’application.</span><span class="sxs-lookup"><span data-stu-id="57b5e-126">If the user agrees, a security upgrade is provided to individualize the DRM component of the application.</span></span>

<span data-ttu-id="57b5e-127">Pour une meilleure expérience utilisateur, vous pouvez lancer le processus d’individualisation comme étape de mise à niveau de la sécurité lors de l’installation. l’utilisateur n’est alors pas interrompu pour obtenir une mise à niveau de sécurité lors de la tentative de lecture d’un fichier protégé.</span><span class="sxs-lookup"><span data-stu-id="57b5e-127">For a better user experience, you can initiate the individualization process as a security upgrade step during setup; then the user is not interrupted to get a security upgrade while trying to play a protected file.</span></span> <span data-ttu-id="57b5e-128">Vous pouvez également encourager activement l’individualisation en ajoutant une commande de menu ou un bouton de **mise à niveau de sécurité** à l’application.</span><span class="sxs-lookup"><span data-stu-id="57b5e-128">You can also actively encourage individualization by adding a **Security Upgrade** menu command or button to the application.</span></span>

> [!Note]  
> <span data-ttu-id="57b5e-129">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="57b5e-129">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="57b5e-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57b5e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57b5e-131">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="57b5e-131">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="57b5e-132">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="57b5e-132">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




