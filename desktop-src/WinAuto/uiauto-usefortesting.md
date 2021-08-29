---
title: Utilisation d'UI Automation pour des tests automatisés
description: Cette vue d’ensemble décrit comment l’automatisation de l’interface utilisateur de Microsoft peut être utile en tant qu’infrastructure pour l’accès par programme dans les scénarios de test automatisé.
ms.assetid: 192162f9-55bf-4111-9f15-c0d3b5af2ab7
keywords:
- clients, tests automatisés UI Automation
- clients, tests automatisés
- clients, test
- clients, outils pour les tests automatisés
- clients, outils d’automatisation d’interface utilisateur pour les tests automatisés
- clients, test UI Automation
- UI Automation, tests automatisés
- UI Automation, test
- UI Automation, outils pour les tests automatisés
- tests automatisés
- outils pour les tests automatisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8055a024c31df615125f2b8b64251a7b3c6eafb6f271c1890e1f49264350c10c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861199"
---
# <a name="using-ui-automation-for-automated-testing"></a>Utilisation d'UI Automation pour des tests automatisés

Cette vue d’ensemble décrit comment l’automatisation de l’interface utilisateur de Microsoft peut être utile en tant qu’infrastructure pour l’accès par programme dans les scénarios de test automatisé.

UI Automation fournit un modèle objet unifié qui permet à toutes les infrastructures d’interface utilisateur d’exposer des fonctionnalités complexes et riches de manière accessible et facilement automatisée.

UI Automation a été développé en tant que successeur de Microsoft Active Accessibility, une infrastructure conçue pour fournir une solution permettant de rendre les contrôles et les applications accessibles. Microsoft Active Accessibility n’a pas été conçu avec l’automatisation des tests à l’esprit, bien qu’il ait évolué dans ce rôle en raison des exigences similaires de l’accessibilité et de l’automatisation. UI Automation est spécifiquement conçu pour fournir des fonctionnalités robustes pour les tests automatisés, en plus de fournir des solutions plus précises pour l’accessibilité. Par exemple, Microsoft Active Accessibility s’appuie sur une seule interface pour exposer des informations sur l’interface utilisateur et collecter les informations nécessaires aux produits de technologie d’assistance. UI Automation sépare les deux modèles.

Un fournisseur et un client sont nécessaires pour implémenter UI Automation pour qu’il soit utile en tant qu’outil de test automatisé. les fournisseurs UI Automation sont des applications, telles que Microsoft Word, Microsoft Excel et d’autres applications ou contrôles tiers basés sur le système d’exploitation Windows. Les clients UI Automation incluent des scripts de tests automatisés et des applications de technologie d’assistance.

Cette rubrique contient les sections suivantes.

-   [UI Automation dans les fournisseurs](#ui-automation-in-providers)
-   [UI Automation dans les clients](#ui-automation-in-clients)
    -   [Accès par programme](#programmatic-access)
-   [Propriétés principales pour l’automatisation des tests](#key-properties-for-test-automation)
-   [Outils et technologies associés](#related-tools-and-technologies)
-   [Rubriques connexes](#related-topics)

## <a name="ui-automation-in-providers"></a>UI Automation dans les fournisseurs

Pour automatiser un élément de l’interface utilisateur, le développeur doit examiner les actions qu’un utilisateur final peut effectuer sur l’objet d’interface utilisateur à l’aide du clavier et de l’interaction avec la souris standard. Une fois ces actions clés identifiées, les modèles de contrôle UI Automation qui reflètent les fonctionnalités et le comportement de l’élément d’interface utilisateur doivent être implémentés sur le contrôle. Par exemple, l’interaction de l’utilisateur avec un contrôle de zone de liste déroulante implique généralement le développement et la réduction de la zone de liste déroulante pour afficher ou masquer une liste d’éléments, la sélection d’un élément dans la liste ou l’ajout d’une nouvelle valeur via l’entrée au clavier.

Avec d’autres modèles d’accessibilité, les développeurs doivent rassembler les informations directement à partir des boutons, menus ou autres contrôles individuels. Chaque type de contrôle est fourni en dizaines de variations mineures. En d’autres termes, même si dix variations d’un bouton de commande fonctionnent de la même manière et exécutent la même fonction, elles doivent toutes être traitées comme des contrôles uniques. Il n’existe aucun moyen de savoir si ces contrôles sont équivalents d’un point de vue fonctionnel. Les modèles de contrôle UI Automation ont été développés pour représenter ces comportements de contrôles communs. Pour plus d'informations, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

Sans le modèle unifié de modèles de contrôle fournis par UI Automation, les outils de test et les développeurs doivent avoir des informations spécifiques à l’infrastructure pour exposer les propriétés et les comportements de contrôle dans cette infrastructure. étant donné que plusieurs infrastructures d’interface utilisateur peuvent être présentes en même temps dans Windows systèmes d’exploitation, notamment Microsoft Win32, Windows Forms et Windows Presentation Foundation (WPF), il peut s’agir d’une tâche fastidieuse pour tester plusieurs applications avec des contrôles apparemment similaires. Par exemple, le tableau suivant répertorie les noms de propriétés spécifiques à l’infrastructure requis pour récupérer le nom ou le texte associé à un contrôle Button et affiche la propriété UI Automation équivalente.



| Type de contrôle | Infrastructure d’interface utilisateur | Propriété spécifique à l’infrastructure | Propriété UI Automation |
|--------------|--------------|-----------------------------|------------------------|
| Bouton       | WPF          | Content                     | Nom de la propriété          |
| Bouton       | Win32        | Caption                     | Nom de la propriété          |
| Image        | HTML         | alt                         | Nom de la propriété          |



 

Les fournisseurs UI Automation sont chargés de mapper les propriétés spécifiques à l’infrastructure de leurs contrôles aux propriétés d’UI Automation équivalentes. Pour plus d’informations sur l’implémentation d’UI Automation dans un fournisseur, consultez le [Guide du programmeur de fournisseur UI Automation](uiauto-providerportal.md). Pour plus d’informations sur l’implémentation des modèles de contrôle, consultez [implémentation de modèles de contrôle UI Automation](uiauto-implementinguiautocontrolpatterns.md).

## <a name="ui-automation-in-clients"></a>UI Automation dans les clients

L’objectif des outils et des scénarios de test automatisés est la manipulation cohérente et reproductible de l’interface utilisateur. Par exemple, cela peut impliquer le test unitaire de contrôles spécifiques, et l’enregistrement et l’exécution de scripts de test qui itèrent au sein d’une série d’actions génériques sur un groupe de contrôles.

une complication dans les applications automatisées est la difficulté de la synchronisation d’un test avec une cible dynamique, par exemple, un contrôle de zone de liste, tel que Windows gestionnaire des tâches, qui affiche une liste d’applications en cours d’exécution. Étant donné que les éléments de la zone de liste sont mis à jour dynamiquement en dehors du contrôle de l’application de test, il est impossible de répéter la sélection d’un élément spécifique dans la zone de liste avec cohérence. Des problèmes similaires peuvent survenir quand vous tentez de répéter des changements de focus simples dans une interface utilisateur qui est en dehors du contrôle de l’application de test.

### <a name="programmatic-access"></a>Accès par programme

L’accès par programmation permet d’imiter, avec du code, les interactions et les expériences produites par les entrées classiques au clavier et à la souris. UI Automation permet un accès par programmation via cinq composants :

-   L’arborescence UI Automation facilite la navigation dans la structure de l’interface utilisateur. L’arborescence est créée à partir de la collection de **HWND**. Pour plus d’informations, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).
-   Les éléments Automation sont des composants individuels dans l’interface utilisateur. Ils peuvent souvent être plus granulaires qu’un **HWND**.
-   Les propriétés Automation fournissent des informations spécifiques sur les éléments d’interface utilisateur. Pour plus d'informations, consultez [UI Automation Properties Overview](uiauto-propertiesoverview.md).
-   Les modèles de contrôle définissent un aspect particulier des fonctionnalités d’un contrôle. Il peut s’agir d’informations sur les propriétés, les méthodes, les événements et les structures. Pour plus d'informations, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).
-   Les événements Automation fournissent des informations et des notifications d’événements. Pour plus d'informations, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="key-properties-for-test-automation"></a>Propriétés principales pour l’automatisation des tests

La possibilité d’identifier et de localiser par la suite un contrôle dans l’interface utilisateur permet aux applications de tests automatisés de fonctionner sur cette interface utilisateur. Les propriétés UI Automation utilisées par les clients et les fournisseurs pour identifier et localiser les contrôles sont décrites dans le tableau suivant.



| Propriété     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AutomationId | Distingue de manière unique un élément Automation de ses frères. La prise en charge de la propriété AutomationId n’est pas obligatoire. Lorsqu’elle est disponible, la propriété AutomationId d’un élément est la même dans toute instance de l’application, quelle que soit la langue locale. Bien que la propriété AutomationId soit unique parmi les éléments frères, elle peut ne pas être unique sur l’ensemble du bureau. par exemple, plusieurs instances d’une application, ou plusieurs affichages de dossiers dans l’explorateur de Windows Microsoft, peuvent contenir des éléments avec le même AutomationIdProperty, par exemple « SystemMenuBar ». Les clients ne doivent pas faire d’hypothèses concernant les AutomationIds exposés par d’autres applications. Il n’est pas garanti que AutomationId soit stable dans les différentes versions ou les versions d’une application. |
| ControlType  | Identifie le type de contrôle représenté par un élément Automation. Des informations importantes peuvent être déduites à partir de la connaissance du type de contrôle. Pour plus d'informations, consultez [UI Automation Control Types Overview](uiauto-controltypesoverview.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Nom         | Chaîne de texte qui identifie ou explique l’objectif d’un élément Automation. Elle doit être utilisée avec prudence, car elle peut être localisée. La propriété Name n’est pas un identificateur unique parmi les frères. Pour l’automatisation des tests, les clients doivent utiliser la propriété AutomationId ou la propriété RuntimeId à la place.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| RuntimeId    | Tableau d’entiers qui représentent un identificateur pour un élément Automation. L’identificateur est unique sur le bureau, mais il est garanti comme étant unique à l’interface utilisateur du Bureau sur lequel il a été généré. Les identificateurs peuvent être réutilisés au fil du temps. Utilisez [**IUIAutomation :: CompareElements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-compareelements) pour déterminer si l’élément qui a actuellement un ID de Runtime particulier est le même que celui qui contenait précédemment cet ID. En outre, le format de la propriété RuntimeId peut changer. Elle doit être traitée comme une valeur opaque et utilisée uniquement pour la comparaison ; par exemple, pour déterminer si un élément Automation se trouve dans le cache.                                                                                                                       |



 

## <a name="related-tools-and-technologies"></a>Outils et technologies associés

[Inspect](inspect-objects.md) (Inspect.exe) est un outil basé sur Windows que vous pouvez utiliser pour collecter des informations d’UI Automation pour le développement et le débogage du fournisseur et du client. l’inspection est incluse dans le kit de développement logiciel (SDK) Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Considérations sur la sécurité d’UI Automation](uiauto-securityoverview.md)
</dt> </dl>

 

 




