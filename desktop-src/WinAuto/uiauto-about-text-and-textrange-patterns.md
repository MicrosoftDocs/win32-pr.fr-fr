---
title: À propos des modèles de contrôle Text et TextRange
description: Le contenu textuel d’un contrôle est exposé à l’aide du modèle de contrôle Text, qui représente le contenu d’un conteneur de texte sous la forme d’un flux de texte.
ms.assetid: acc2b513-9367-416a-b0d9-3c2bcc14a8a7
keywords:
- UI Automation, prise en charge du contenu textuel
- UI Automation, vue d’ensemble du modèle de texte
- UI Automation, vue d’ensemble des contrôles de texte
- UI Automation, modèle de contrôle de texte
- UI Automation, Text Services Framework (TSF)
- UI Automation, TSF
- UI Automation, performances
- modèles de texte, à propos de
- modèles de texte, Text Services Framework (TSF)
- contrôles de texte, à propos de
- contenu textuel, prise en charge de
- contrôles de texte, performances
- Text (modèle de contrôle)
- modèles de contrôle, texte
- Text Services Framework (TSF)
- TSF (Text Services Framework)
- performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9ff1eb75227454e3e9df6035798a304096a958
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010579"
---
# <a name="about-the-text-and-textrange-control-patterns"></a>À propos des modèles de contrôle Text et TextRange

Le contenu textuel d’un contrôle est exposé à l’aide du modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) , qui représente le contenu d’un conteneur de texte sous la forme d’un flux de texte. Le modèle de contrôle Text requiert la prise en charge du modèle de contrôle TextRange pour exposer les attributs de mise en forme et de style. Le modèle de contrôle TextRange prend en charge le modèle de contrôle Text en représentant des étendues de texte disjointes contiguës ou multiples dans un conteneur de texte avec une collection de points de terminaison de début et de fin. Le modèle de contrôle TextRange prend en charge des fonctionnalités telles que la sélection, la comparaison, la récupération et la traversée.

> [!Note]  
> Le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) ne permet pas d’insérer ou de modifier du texte. Toutefois, en fonction du contrôle, cela peut être accompli à l’aide du modèle de contrôle [value](uiauto-implementingvalue.md) d’UI Automation de Microsoft ou via une entrée directe au clavier. Il y a également un modèle [**TextEdit**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) qui prend en charge la modification par programmation en texte.

 

Les fonctionnalités décrites dans cette rubrique sont essentielles pour les fournisseurs de technologies d’assistance et leurs utilisateurs finaux. Les technologies d’assistance peuvent utiliser UI Automation pour collecter des informations complètes sur la mise en forme du texte pour l’utilisateur et fournir une navigation par programmation et une sélection de texte par [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (caractère, mot, ligne ou paragraphe).

Cette rubrique contient les sections suivantes :

-   [UI Automation TextPattern et l’infrastructure de services de texte](#ui-automation-textpattern-and-the-text-services-framework)
-   [Types de contrôles](#control-types)
-   [Interfaces de fournisseur](#provider-interfaces)
-   [Interfaces clientes](#client-interfaces)
-   [Performances](#performance)
-   [Modèle de texte et objets incorporés virtualisés](#text-pattern-and-virtualized-embedded-objects)
-   [Utilisation du type de contrôle personnalisé avec le modèle de contrôle Text](#using-the-custom-control-type-with-the-text-control-pattern)
-   [Durée de vie d’une plage de texte](#lifetime-of-a-text-range)
-   [Rubriques connexes](#related-topics)

## <a name="ui-automation-textpattern-and-the-text-services-framework"></a>UI Automation TextPattern et l’infrastructure de services de texte

Text Services Framework (TSF) est une infrastructure système simple et évolutive qui permet les services de langage naturel et l’entrée de texte avancée sur le bureau et dans les applications. En plus de fournir des interfaces permettant aux applications d’exposer leur magasin de texte, il prend également en charge les métadonnées pour le magasin de texte.

TSF a été conçu pour les applications qui doivent injecter des entrées dans des scénarios contextuels. Le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) , toutefois, est une solution en lecture seule destinée à fournir un accès optimisé à un magasin de texte pour les lecteurs d’écran et les appareils en braille.

Les technologies accessibles qui requièrent un accès en lecture seule à un magasin de texte peuvent utiliser le modèle de contrôle Text, mais elles auront besoin des fonctionnalités de TSF pour les entrées contextuelles.

Pour plus d’informations, consultez [Text Services Framework](/windows/desktop/TSF/text-services-framework).

## <a name="control-types"></a>Types de contrôles

Le type de contrôle d' [édition](uiauto-supporteditcontroltype.md) UI Automation et le type de contrôle [document](uiauto-supportdocumentcontroltype.md) doivent prendre en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) . Pour une meilleure accessibilité, Microsoft recommande que les types de contrôle d' [info-bulle](uiauto-supporttooltipcontroltype.md) et de texte prennent également en charge le modèle de contrôle Text, mais ce n’est pas obligatoire.

## <a name="provider-interfaces"></a>Interfaces de fournisseur

Les fournisseurs UI Automation prennent en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) pour un contrôle en implémentant les interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) et [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) . Ces interfaces exposent des informations d’attribut détaillées pour le texte dans le contrôle et fournissent des fonctionnalités de navigation robustes.

Un fournisseur n’a pas besoin de prendre en charge tous les attributs de texte si le contrôle ne prend pas en charge un attribut particulier.

Un fournisseur doit prendre en charge les méthodes [**ITextProvider :: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) et [**ITextRangeProvider :: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) si le contrôle prend en charge la sélection de texte ou le positionnement du curseur de texte (ou signe insertion de système) dans la zone de texte. Si le contrôle ne prend pas en charge cette fonctionnalité, il n’a pas besoin de prendre en charge l’une de ces méthodes. Toutefois, le contrôle doit exposer le type de sélection de texte qu’il prend en charge en implémentant la propriété [**ITextProvider :: SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) .

Un fournisseur doit toujours prendre en charge les constantes [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) , le **\_ caractère TextUnit** et le **\_ document TextUnit**, ainsi que les autres éléments qu’il est en mesure de prendre en charge.

> [!Note]  
> Le fournisseur peut ignorer la prise en charge d’un [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) spécifique en reportant à la plus grande unité prise en charge dans l’ordre suivant : **TextUnit \_ character**, **TextUnit \_ format**, **TextUnit \_ Word**, **TextUnit \_ line**, **TextUnit \_ paragraphe**, **TextUnit \_ page** et TextUnit **\_ document**.

 

## <a name="client-interfaces"></a>Interfaces clientes

Les applications clientes UI Automation utilisent les interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) et [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) pour accéder au contenu textuel d’un contrôle de texte. Les clients utilisent **IUIAutomationTextPattern** pour sélectionner des étendues de texte appelées *plages de texte* et pour récupérer des pointeurs vers des interfaces **IUIAutomationTextRange** pour les plages. L’interface **IUIAutomationTextRange** permet aux clients de manipuler la plage de texte et de récupérer des informations sur le texte de la plage, y compris des attributs tels que le nom de la police, la couleur de premier plan, le style de soulignement, etc. Pour plus d’informations, consultez [identificateurs d’attribut de texte](uiauto-textattribute-ids.md).

## <a name="performance"></a>Performances

Le modèle de contrôle **Text** s’appuie sur des appels interprocessus pour la plupart de ses fonctionnalités, il ne fournit donc pas de mécanisme de mise en cache pour améliorer les performances lors du traitement du contenu. D’autres modèles de contrôle de Microsoft UI Automation sont accessibles à l’aide de la méthode [**IUIAutomationElement :: GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern) .

Une technique pour améliorer les performances consiste à s’assurer que les clients UI Automation tentent de récupérer des blocs de texte de taille modérée à l’aide de la méthode [**IUIAutomationTextRange :: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) . Par exemple, l’utilisation de **gettext** pour récupérer des caractères uniques entraînera des accès interprocessus pour chaque caractère, alors que la spécification d’une longueur maximale lors de l’appel de **gettext** entraînera un accès inter-processus, mais peut présenter une latence élevée selon la taille de la plage de texte.

## <a name="text-pattern-and-virtualized-embedded-objects"></a>Modèle de texte et objets incorporés virtualisés

Dans la mesure du possible, une implémentation de fournisseur de [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) et [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) doit prendre en charge l’intégralité du texte d’un document, y compris tout texte en dehors de la fenêtre d’affichage. Pour le texte hors écran ou les objets incorporés qui sont virtualisés, les fournisseurs doivent prendre en charge le [modèle de contrôle VirtualizedItem](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)).

Si un document est virtualisé alors que le flux de texte entier est toujours disponible, la propriété [**ITextProvider ::D ocumentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) récupère une plage de texte qui comprend le document entier. Toutefois, l’appel de la méthode [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) permet de récupérer une collection d’objets virtualisés représentant tous les objets incorporés dans le document. Pour interagir avec un objet incorporé virtualisé, les clients doivent appeler la méthode [**IVirtualizedItemProvider :: réalise**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) , qui rend les éléments entièrement accessibles en tant qu’éléments UI Automation. Les clients doivent suivre un processus similaire pour travailler avec des éléments de grille dans une table incorporée dans laquelle une partie de la table est déconnectée de l’écran et virtualisée.

## <a name="using-the-custom-control-type-with-the-text-control-pattern"></a>Utilisation du type de contrôle personnalisé avec le modèle de contrôle Text

Alors que le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) prend en charge de nombreux attributs de texte et objets incorporés, il n’est pas possible de définir à l’avance tous les éléments de document et types de présentation possibles. Pour les éléments de document qui ne sont pas pris en charge par les attributs ou les types de contrôles standard existants, les fournisseurs peuvent utiliser les fonctionnalités d’extensibilité fournies par le type de contrôle **personnalisé** UI Automation.

Pour les applications et les interfaces utilisateur basées sur des présentations de page, la présentation de la limite et de la disposition de la « page » peut également être exprimée sous la forme d’un objet incorporé qui a un type de contrôle personnalisé (autrement dit, `LocalizedControlType="page"` ). De cette façon, l’objet incorporé peut héberger d’autres éléments de page qui ne peuvent pas facilement faire partie du flux de texte du document, tels que les champs d’en-tête et de pied de page de chaque page, en tant qu’enfants de l’objet incorporé « page ». Chaque objet « page » peut également prendre en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) de manière indépendante, ce qui fonctionne bien pour les applications telles que les outils de création pour les présentations de diaporama ou les environnements de publication de bureau basés sur une page.

## <a name="lifetime-of-a-text-range"></a>Durée de vie d’une plage de texte

Si possible, un fournisseur doit s’assurer que toutes les modifications de texte, telles que les suppressions, les insertions et les déplacements, sont reflétées dans la plage de texte associée. Si la mise à jour de la plage de texte n’est pas possible, le fournisseur doit déclencher un événement [**\_ \_ TextChangedEventId de texte UIA**](uiauto-event-ids.md) pour informer les clients que la plage de texte n’est plus valide et qu’une nouvelle doit être récupérée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Comment UI Automation prend en charge les objets incorporés](uiauto-textpattern-and-embedded-objects-overview.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Prise en charge d’UI Automation pour le contenu textuel](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Utilisation de contrôles textuels](uiauto-workingwithtextbasedcontrols.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Text Services Framework](/windows/desktop/TSF/text-services-framework)
</dt> </dl>

 

 