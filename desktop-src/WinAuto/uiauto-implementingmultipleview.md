---
title: Modèle de contrôle MultipleView
description: Fournit des instructions et des conventions pour l’implémentation de IMultipleViewProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- UI Automation, implémentation du modèle de contrôle MultipleView
- UI Automation, modèle de contrôle MultipleView
- UI Automation, IMultipleViewProvider
- IMultipleViewProvider
- implémentation des modèles de contrôle MultipleView d’UI Automation
- Modèles de contrôle MultipleView
- modèles de contrôle, IMultipleViewProvider
- modèles de contrôle, implémenter des MultipleView UI Automation
- modèles de contrôle, MultipleView
- interfaces, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010490"
---
# <a name="multipleview-control-pattern"></a>Modèle de contrôle MultipleView

Fournit des instructions et des conventions pour l’implémentation de [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), y compris des informations sur les propriétés et les méthodes. Des liens vers des références supplémentaires sont répertoriés à la fin de la rubrique. Le modèle de contrôle **MultipleView** est utilisé pour prendre en charge les contrôles qui fournissent et peuvent basculer entre plusieurs représentations des mêmes informations ou le même jeu de contrôles enfants.

voici des exemples de contrôles qui peuvent présenter plusieurs vues, notamment le mode liste (qui peut afficher son contenu sous forme de miniatures, vignettes, icônes ou détails), Microsoft Excel des graphiques (secteurs, courbes, barres, valeurs de cellule avec une formule), Microsoft Word documents (normal, disposition web, page, page, disposition de lecture, plan), calendrier microsoft Outlook (année, mois, semaine, jour) et enveloppes de Lecteur Windows Media microsoft. Les vues prises en charge sont déterminées par le développeur de contrôle et sont spécifiques à chaque contrôle.

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IMultipleViewProvider**](#required-members-for-imultipleviewprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **MultipleView** , notez les conventions et recommandations suivantes :

-   [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) doit également être implémenté sur un conteneur qui gère la vue actuelle s’il est différent d’un contrôle qui fournit la vue actuelle. par exemple, Windows Explorer contient un contrôle de liste pour le contenu du dossier actuel, tandis que la vue du contrôle est gérée à partir de l’application Windows Explorer.
-   Un contrôle qui est en mesure de trier son contenu n’est pas censé prendre en charge plusieurs vues.
-   La collection de vues doit être identique sur l’ensemble des instances.
-   Les noms des vues doivent pouvoir être utilisés dans la conversion de texte en parole, en braille et dans d’autres applications lisibles par l’homme.

## <a name="required-members-for-imultipleviewprovider"></a>Membres requis pour **IMultipleViewProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) .



| Membres nécessaires                                                            | Type de membre | Notes |
|-----------------------------------------------------------------------------|-------------|-------|
| [**Appliquée**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | Propriété    | None  |
| [**GetSupportedViews**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | Méthode      | None  |
| [**GetViewName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | Méthode      | None  |
| [**SetCurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | Méthode      | None  |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Modèle de contrôle ExpandCollapse](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




