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
# <a name="new-features-in-tsf"></a>Nouvelles fonctionnalités de TSF

Avec le lancement de Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) propose plusieurs nouvelles fonctionnalités.

## <a name="extended-support-of-advanced-text-services"></a>Prise en charge étendue des services de texte avancés

La prise en charge a été ajoutée à TSF et Windows pour fournir une interface utilisateur cohérente pour toutes les applications sur le bureau. Cette nouvelle prise en charge permet aux applications ou aux contrôles hérités qui ne sont pas conscients de TSF de tirer parti de certains services de texte avancés gratuitement. Par exemple, la dictée vocale et l’écriture manuscrite peuvent maintenant être utilisées pour entrer du texte dans un document de n’importe quelle application.

Cette nouvelle fonctionnalité est disponible uniquement pour WindowsXP Service Pack1 ou version ultérieure. Elle est désactivée par défaut. Pour l’activer, cliquez sur la case à cocher dans l’onglet nouveau **avancé** de la partie **services de texte et langues d’entrée** du panneau de configuration **Options régionales et linguistiques** .

![prise en charge des applications non compatibles dans le panneau de configuration de TSF](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a>Support RichEdit

[Édition enrichie de Microsoft®](../controls/rich-edit-controls.md) La version 4,1, utilisée par les applications pour afficher et modifier du texte avec une mise en forme de caractère et de paragraphe spéciale, expose maintenant la fonctionnalité TSF. Cette prise en charge est désactivée par défaut. Pour activer TSF en Rich Edit, une application d’hébergement envoie un message de fenêtre spécial au contrôle RichEdit.

## <a name="security-improvements"></a>Améliorations apportées à la sécurité

La sécurité et la robustesse de TSF ont été considérablement améliorées, afin de réduire la probabilité qu’un programme hostile soit en mesure d’accéder à la pile, au segment de mémoire ou à d’autres emplacements de mémoire sécurisés. La sécurité des exemples d’applications et de services de texte du kit de développement logiciel (SDK) a également été améliorée.

 

 