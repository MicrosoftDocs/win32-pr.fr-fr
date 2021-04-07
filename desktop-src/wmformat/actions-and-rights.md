---
title: Actions et droits
description: Actions et droits
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, licences DRM
- Windows Media Format SDK, licences pour DRM
- gestion des droits numériques (DRM), actions
- DRM (gestion des droits numériques), actions
- gestion des droits numériques (DRM), droits
- DRM (gestion des droits numériques), droits
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- licences, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028678"
---
# <a name="actions-and-rights"></a><span data-ttu-id="fc048-113">Actions et droits</span><span class="sxs-lookup"><span data-stu-id="fc048-113">Actions and Rights</span></span>

<span data-ttu-id="fc048-114">Lorsqu’un fichier est protégé à l’aide de Windows Media DRM, son utilisation est complètement restreinte.</span><span class="sxs-lookup"><span data-stu-id="fc048-114">When a file is protected by using Windows Media DRM, its use is completely restricted.</span></span> <span data-ttu-id="fc048-115">Les licences peuvent être émises pour permettre à un utilisateur d’utiliser le contenu de manière spécifique.</span><span class="sxs-lookup"><span data-stu-id="fc048-115">Licenses can be issued to enable a user to use the content in specific ways.</span></span> <span data-ttu-id="fc048-116">Chaque méthode dans laquelle un utilisateur peut utiliser le contenu est décrite par une action.</span><span class="sxs-lookup"><span data-stu-id="fc048-116">Each way in which a user might use the content is described by an action.</span></span> <span data-ttu-id="fc048-117">Par exemple, la réexécution d’un fichier sur un ordinateur est une action.</span><span class="sxs-lookup"><span data-stu-id="fc048-117">For example, playing a file on a computer is an action.</span></span>

<span data-ttu-id="fc048-118">Une licence qui permet d’effectuer une action donnée est dite d’accorder un droit.</span><span class="sxs-lookup"><span data-stu-id="fc048-118">A license that enables a given action is said to grant a right.</span></span> <span data-ttu-id="fc048-119">Par exemple, une licence peut accorder le droit de lire du contenu sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fc048-119">For example, a license can grant the right to play content on a computer.</span></span>

<span data-ttu-id="fc048-120">Les actions et les droits font référence aux mêmes façons d’utiliser le contenu.</span><span class="sxs-lookup"><span data-stu-id="fc048-120">Actions and rights refer to the same ways of using content.</span></span> <span data-ttu-id="fc048-121">La différence est que l’action fait référence à l’utilisation alors que le droit fait référence à l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="fc048-121">The difference is that the action refers to the use while the right refers to the permission.</span></span> <span data-ttu-id="fc048-122">Malgré cette distinction, les mots action et Right sont souvent utilisés de façon interchangeable dans cette documentation et dans d’autres documents qui décrivent Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="fc048-122">Despite this distinction, the words action and right are often used interchangeably in this documentation and in other documents that describe Windows Media DRM.</span></span>

<span data-ttu-id="fc048-123">Les actions régies par les droits DRM Windows Media sont répertoriées dans la section des [constantes de droits](rights-constants.md) de cette documentation.</span><span class="sxs-lookup"><span data-stu-id="fc048-123">The actions governed by Windows Media DRM rights are listed in the [Rights Constants](rights-constants.md) section of this documentation.</span></span>

<span data-ttu-id="fc048-124">Certaines méthodes des API étendues du client Windows Media DRM utilisent des constantes différentes pour faire référence aux droits DRM de base.</span><span class="sxs-lookup"><span data-stu-id="fc048-124">Certain methods of the Windows Media DRM Client Extended APIs use different constants to refer to the basic DRM rights.</span></span> <span data-ttu-id="fc048-125">Par exemple, la méthode [**IWMDRMLicenseQuery :: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) utilise un ensemble de chaînes spécifiques aux États de licence.</span><span class="sxs-lookup"><span data-stu-id="fc048-125">For example, the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method uses a set of strings specific to license states.</span></span> <span data-ttu-id="fc048-126">Même si ces constantes définissent des chaînes différentes de celles des constantes de droits de base, elles font référence aux mêmes droits dans la licence.</span><span class="sxs-lookup"><span data-stu-id="fc048-126">Even though these constants are defining different strings than the basic rights constants, they refer to the same rights in the license.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc048-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc048-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc048-128">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="fc048-128">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




