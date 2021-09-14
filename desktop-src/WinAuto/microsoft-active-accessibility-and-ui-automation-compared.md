---
title: Comparaison entre Microsoft Active Accessibility et UI Automation
description: Cette rubrique fournit des résumés des principales différences entre Microsoft Active Accessibility et UI Automation.
ms.assetid: ba963e53-6fb8-4bc1-8883-62547f52b0e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c90c4bffd0646aea592e19adc51ca020b2c90d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010684"
---
# <a name="microsoft-active-accessibility-and-ui-automation-compared"></a>Comparaison entre Microsoft Active Accessibility et UI Automation

l’API Windows automation est constituée de deux technologies : microsoft Active Accessibility et microsoft UI automation. microsoft Active Accessibility est la technologie d’accessibilité héritée qui a été introduite en tant que complément de plateforme pour Windows 95, alors que l’automatisation d’interface utilisateur est une technologie plus récente et plus puissante qui se limite aux limitations inhérentes à Microsoft Active Accessibility.

Cette rubrique fournit des résumés des principales différences entre Microsoft Active Accessibility et UI Automation. Il comprend les sections suivantes :

-   [Principes de conception de base](#basic-design-principles)
-   [Propriétés et modèles de contrôle](#properties-and-control-patterns)
-   [Rôles MSAA et modèles de contrôle UI Automation](#msaa-roles-and-ui-automation-control-patterns)
-   [Navigation dans le modèle objet](#object-model-navigation)
-   [Extensibilité du modèle objet](#object-model-extensibility)
-   [Transition depuis MSAA](#transitioning-from-msaa)
-   [Choix de Microsoft Active Accessibility, UI Automation ou IAccessibleEx](#choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex)
    -   [Nouvelles applications et contrôles](#new-applications-and-controls)
    -   [Implémentations de Microsoft Active Accessibility existantes](#existing-microsoft-active-accessibility-implementations)
-   [Rubriques connexes](#related-topics)

## <a name="basic-design-principles"></a>Principes de conception de base

Bien que Microsoft Active Accessibility et UI Automation soient deux technologies différentes, les principes de conception de base sont similaires. l’objectif des deux technologies est d’exposer des informations riches sur les éléments d’interface utilisateur utilisés dans les applications Windows. les développeurs d’outils d’accessibilité peuvent utiliser ces informations pour créer des logiciels qui rendent les applications s’exécutant sur Windows plus accessibles aux personnes souffrant de troubles de la vision, de l’audition ou du mouvement.

Microsoft Active Accessibility et UI Automation exposent le modèle d’objet d’interface utilisateur sous la forme d’une arborescence hiérarchique, enracinée sur le bureau. Microsoft Active Accessibility représente des éléments d’interface utilisateur individuels comme des *objets accessibles*, et UI Automation les représente comme des *éléments Automation*. Ils font tous deux référence à l’outil d’accessibilité ou au programme d’automatisation logicielle en tant que *client*. Toutefois, Microsoft Active Accessibility fait référence à l’application ou au contrôle qui offre l’interface utilisateur pour l’accessibilité en tant que *serveur*, tandis que l’automatisation d’interface utilisateur se réfère à ceci comme *fournisseur*.

## <a name="properties-and-control-patterns"></a>Propriétés et modèles de contrôle

Microsoft Active Accessibility offre une interface COM (Component Object Model) unique avec un ensemble fixe et restreint de propriétés. UI Automation offre un ensemble plus riche de propriétés, ainsi qu’un ensemble d’interfaces étendues appelées *modèles de contrôle* pour manipuler les objets accessibles de la manière dont Microsoft Active Accessibility ne peut pas.

Pour plus d’informations, consultez [vue d’ensemble des propriétés UI Automation](uiauto-propertiesoverview.md) et [vue d’ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md).

## <a name="msaa-roles-and-ui-automation-control-patterns"></a>Rôles MSAA et modèles de contrôle UI Automation

microsoft a conçu le modèle d’objet microsoft Active Accessibility en même temps que Windows version de 95. Le modèle est basé sur des « rôles » définis il y a une décennie, et vous ne pouvez pas prendre en charge de nouveaux comportements de l’interface utilisateur ou fusionner deux ou plusieurs rôles ensemble. Il n’existe pas de modèle d’objet de texte, par exemple, pour aider les technologies d’assistance à gérer du contenu Web complexe. UI Automation expose ces limitations en introduisant des modèles de contrôle qui permettent aux objets de prendre en charge plusieurs rôles, et le modèle de contrôle de [texte](uiauto-implementingtextandtextrange.md) UI Automation offre un modèle d’objet de texte à part entière.

## <a name="object-model-navigation"></a>Navigation dans le modèle objet

Une autre limitation de Microsoft Active Accessibility consiste à naviguer dans le modèle objet. Microsoft Active Accessibility représente l’interface utilisateur sous la forme d’une hiérarchie d’objets accessibles. Les clients naviguent d’un objet accessible à un autre à l’aide d’interfaces et de méthodes disponibles à partir de l’objet accessible. Les serveurs peuvent exposer les enfants d’un objet accessible avec les propriétés de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , ou avec l’interface com [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) standard. Toutefois, les clients doivent être en mesure de gérer les deux approches pour n’importe quel serveur. Cette ambiguïté signifie un travail supplémentaire pour les implémenteurs clients et des modèles d’objets accessibles rompus pour les implémenteurs de serveurs.

UI Automation représente l’interface utilisateur sous la forme d’une arborescence hiérarchique d’éléments Automation et fournit une interface unique pour naviguer dans l’arborescence. Les clients peuvent personnaliser l’affichage des éléments dans l’arborescence par l’étendue et le filtrage.

## <a name="object-model-extensibility"></a>Extensibilité du modèle objet

Les propriétés et les fonctions de Microsoft Active Accessibility ne peuvent pas être étendues sans rompre ou modifier la spécification de l’interface com [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Le résultat est que le nouveau comportement de contrôle ne peut pas être exposé par le biais du modèle objet ; Il a tendance à être statique.

Avec UI Automation, à mesure que de nouveaux éléments d’interface utilisateur sont créés, les développeurs d’applications peuvent introduire des propriétés personnalisées, des modèles de contrôle et des événements pour décrire les nouveaux éléments. Pour plus d’informations, consultez [propriétés personnalisées, événements et modèles de contrôle](uiauto-custompropertieseventscontrolpatterns.md).

## <a name="transitioning-from-msaa"></a>Transition depuis MSAA

l’infrastructure de l’API automation Windows fournit la prise en charge de la transition des serveurs Microsoft Active Accessibility aux fournisseurs UI automation. L’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) permet d’ajouter à la prise en charge des propriétés UI Automation et des modèles de contrôle spécifiques à des serveurs Microsoft Active Accessibility hérités sans avoir à réécrire la totalité de l’implémentation. L’interface **IAccessibleEx** permet également aux clients Microsoft Active Accessibilitys in-process d’accéder directement aux interfaces du fournisseur UI Automation, plutôt qu’à l’aide des interfaces du client UI Automation. Pour plus d’informations, consultez [l’interface IAccessibleEx](iaccessibleex.md).

## <a name="choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex"></a>Choix de Microsoft Active Accessibility, UI Automation ou IAccessibleEx

cette section vous aide à déterminer quelle solution API d’automatisation d’Windows utiliser pour implémenter un produit de technologie d’assistance ou pour rendre votre application accessible aux produits de technologie d’assistance.

### <a name="new-applications-and-controls"></a>Nouvelles applications et contrôles

Si vous développez une nouvelle application ou un nouveau contrôle, Microsoft recommande l’utilisation d’UI Automation. Bien que Microsoft Active Accessibility puisse être plus facile à mettre en œuvre à long terme, les limitations inhérentes à cette technologie, telles que son modèle d’objet vieillissant et l’incapacité à prendre en charge de nouveaux comportements de l’interface utilisateur ou de fusionner des rôles, le rendent plus difficile et coûteuse sur le long terme. Ces limitations deviennent particulièrement évidentes lors de l’introduction de nouveaux contrôles.

Le modèle d’objet UI Automation est plus facile à utiliser et est plus souple que celui de Microsoft Active Accessibility. Les éléments UI Automation reflètent l’évolution des interfaces utilisateur, et les développeurs peuvent définir des modèles de contrôle, des propriétés et des événements UI Automation personnalisés.

Microsoft Active Accessibility tend à s’exécuter lentement pour les clients qui ne sont pas en cours d’exécution. Pour améliorer les performances, les développeurs de programmes d’outils d’accessibilité choisissent souvent de raccorder et d’exécuter leurs programmes dans le processus de l’application cible : une approche extrêmement difficile et risquée. UI Automation est beaucoup plus facile à implémenter pour les clients hors processus et offre de meilleures performances et une plus grande fiabilité.

### <a name="existing-microsoft-active-accessibility-implementations"></a>Implémentations de Microsoft Active Accessibility existantes

Si vous mettez à jour une application ou un contrôle existant basé sur Microsoft Active Accessibility, envisagez d’ajouter la prise en charge d’UI Automation en implémentant l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Tout d’abord, assurez-vous que votre application ou contrôle répond aux spécifications suivantes :

-   La hiérarchie des objets accessibles de base Microsoft Active Accessibility Server doit être bien organisée et ne pas répondre aux erreurs. [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) ne peut pas résoudre les problèmes liés à des hiérarchies d’objets accessibles existantes.
-   Votre implémentation de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) doit être conforme à la spécification Microsoft Active Accessibility et à la spécification UI Automation. Microsoft fournit un ensemble d’outils permettant de valider la conformité avec les deux spécifications. Pour plus d’informations, consultez [outils de test](testing-tools.md).

Si l’une de ces conditions n’est pas remplie, envisagez d’implémenter UI Automation en mode natif. Vous pouvez conserver les implémentations de Microsoft Active Accessibility Server existantes pour la compatibilité descendante, si nécessaire. Du point de vue du client UI Automation, il n’existe aucune différence entre les fournisseurs UI Automation et les serveurs Microsoft Active Accessibility qui implémentent correctement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Pour plus d’informations, consultez [l’interface IAccessibleEx](iaccessibleex.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Vue d’ensemble de l’API Automation](windows-automation-api-overview.md)
</dt> <dt>

[Microsoft Active Accessibility](microsoft-active-accessibility.md)
</dt> <dt>

[UI Automation](entry-uiauto-win32.md)
</dt> <dt>

[Interface IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 