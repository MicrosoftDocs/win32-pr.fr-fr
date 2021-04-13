---
title: Nouvelles fonctionnalités de TSF
description: Avec le lancement de Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) propose plusieurs nouvelles fonctionnalités.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Text Services Framework (TSF), nouvelles fonctionnalités
- TSF (Text Services Framework), nouvelles fonctionnalités
- services de texte, nouvelles fonctionnalités
- Applications compatibles TSF, nouvelles fonctionnalités
- Text Services Framework (TSF), prise en charge avancée
- TSF (Text Services Framework), prise en charge avancée
- services de texte, prise en charge avancée
- Applications compatibles TSF, prise en charge avancée
- Text Services Framework (TSF), Rich Edit
- TSF (Text Services Framework), modification riche
- services de texte, modification riche
- Applications compatibles TSF, modification riche
- Édition enrichie
- Text Services Framework (TSF), sécurité
- TSF (Text Services Framework), sécurité
- services de texte, sécurité
- Applications compatibles TSF, sécurité
- sécurité pour TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a345087304be638be93fa352845cdd468bf15
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382048"
---
# <a name="new-features-in-tsf"></a><span data-ttu-id="bee63-121">Nouvelles fonctionnalités de TSF</span><span class="sxs-lookup"><span data-stu-id="bee63-121">New Features in TSF</span></span>

<span data-ttu-id="bee63-122">Avec le lancement de Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) propose plusieurs nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="bee63-122">With the release of Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) has several new features.</span></span>

## <a name="extended-support-of-advanced-text-services"></a><span data-ttu-id="bee63-123">Prise en charge étendue des services de texte avancés</span><span class="sxs-lookup"><span data-stu-id="bee63-123">Extended Support of Advanced Text Services</span></span>

<span data-ttu-id="bee63-124">La prise en charge a été ajoutée à TSF et Windows pour fournir une interface utilisateur cohérente pour toutes les applications sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="bee63-124">Support has been added to TSF and Windows to provide a consistent user interface for all applications across the desktop.</span></span> <span data-ttu-id="bee63-125">Cette nouvelle prise en charge permet aux applications ou aux contrôles hérités qui ne sont pas conscients de TSF de tirer parti de certains services de texte avancés gratuitement.</span><span class="sxs-lookup"><span data-stu-id="bee63-125">This new support enables legacy applications or controls that are not aware of TSF to take advantage of some advanced text services for free.</span></span> <span data-ttu-id="bee63-126">Par exemple, la dictée vocale et l’écriture manuscrite peuvent maintenant être utilisées pour entrer du texte dans un document de n’importe quelle application.</span><span class="sxs-lookup"><span data-stu-id="bee63-126">For example, speech dictation and handwriting can now be used to enter text into a document in any application.</span></span>

<span data-ttu-id="bee63-127">Cette nouvelle fonctionnalité est disponible uniquement pour WindowsXP Service Pack1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bee63-127">This new feature is available only for WindowsXP Service Pack1 or later.</span></span> <span data-ttu-id="bee63-128">Elle est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="bee63-128">It is turned off by default.</span></span> <span data-ttu-id="bee63-129">Pour l’activer, cliquez sur la case à cocher dans l’onglet nouveau **avancé** de la partie **services de texte et langues d’entrée** du panneau de configuration **Options régionales et linguistiques** .</span><span class="sxs-lookup"><span data-stu-id="bee63-129">To enable it, click the check box in the new **Advanced** tab in the **Text Services and Input Languages** portion of the **Regional and Language Options** control panel.</span></span>

![prise en charge des applications non compatibles dans le panneau de configuration de TSF](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a><span data-ttu-id="bee63-131">Support RichEdit</span><span class="sxs-lookup"><span data-stu-id="bee63-131">Rich Edit Support</span></span>

<span data-ttu-id="bee63-132">[Édition enrichie de Microsoft®](../controls/rich-edit-controls.md) La version 4,1, utilisée par les applications pour afficher et modifier du texte avec une mise en forme de caractère et de paragraphe spéciale, expose maintenant la fonctionnalité TSF.</span><span class="sxs-lookup"><span data-stu-id="bee63-132">[Microsoft® Rich Edit](../controls/rich-edit-controls.md) Version 4.1, used by applications to view and edit text with special character and paragraph formatting, now exposes TSF functionality.</span></span> <span data-ttu-id="bee63-133">Cette prise en charge est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="bee63-133">By default this support is turned off.</span></span> <span data-ttu-id="bee63-134">Pour activer TSF en Rich Edit, une application d’hébergement envoie un message de fenêtre spécial au contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="bee63-134">To enable TSF in Rich Edit, a hosting application sends a special window message to the Rich Edit control.</span></span>

## <a name="security-improvements"></a><span data-ttu-id="bee63-135">Améliorations apportées à la sécurité</span><span class="sxs-lookup"><span data-stu-id="bee63-135">Security Improvements</span></span>

<span data-ttu-id="bee63-136">La sécurité et la robustesse de TSF ont été considérablement améliorées, afin de réduire la probabilité qu’un programme hostile soit en mesure d’accéder à la pile, au segment de mémoire ou à d’autres emplacements de mémoire sécurisés.</span><span class="sxs-lookup"><span data-stu-id="bee63-136">The security and robustness of TSF have been substantially improved, to reduce the likelihood of a hostile program being able to access the stack, heap, or other secure memory locations.</span></span> <span data-ttu-id="bee63-137">La sécurité des exemples d’applications et de services de texte du kit de développement logiciel (SDK) a également été améliorée.</span><span class="sxs-lookup"><span data-stu-id="bee63-137">The security of software development kit (SDK) sample applications and text services has also been improved.</span></span>

 

 