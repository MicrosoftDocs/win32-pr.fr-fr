---
title: Invoke (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IInvokeProvider, y compris des informations sur les méthodes.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- UI Automation, implémenter le modèle de contrôle Invoke
- UI Automation, appeler le modèle de contrôle
- UI Automation, IInvokeProvider
- IInvokeProvider
- implémentation des modèles de contrôle Invoke d’UI Automation
- Appeler des modèles de contrôle
- modèles de contrôle, IInvokeProvider
- modèles de contrôle, implémenter l’appel d’UI Automation
- modèles de contrôle, Invoke
- interfaces, IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518097"
---
# <a name="invoke-control-pattern"></a>Invoke (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), y compris des informations sur les méthodes. Le modèle de contrôle **Invoke** est utilisé pour prendre en charge les contrôles qui ne maintiennent pas l’État lorsqu’ils sont activés, mais qui initialisent ou exécutent une action unique et non ambiguë.

Les contrôles qui maintiennent l’État, tels que les cases à cocher et les cases d’option, doivent implémenter [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) et [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) respectivement. Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IInvokeProvider**](#required-members-for-iinvokeprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **Invoke** , notez les conventions et recommandations suivantes :

-   Les contrôles implémentent [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) si le même comportement n’est pas exposé par le biais d’un autre fournisseur de modèle de contrôle. Par exemple, si la méthode [**IUIAutomationInvokePattern :: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) sur un contrôle exécute la même action que la méthode [**IUIAutomationExpandCollapsePattern :: Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) ou [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) , le contrôle ne doit pas implémenter **IInvokeProvider**.
-   Pour appeler un contrôle, il convient généralement de cliquer, de double-cliquer ou d’appuyer sur Entrée, sur un raccourci clavier prédéfini ou sur une autre combinaison de touches.
-   L’événement **appelé** ([**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)) est déclenché sur un contrôle qui a été activé (en réponse à un contrôle effectuant l’action qui lui est associée). Si possible, l’événement doit être déclenché une fois que le contrôle a terminé l’action et retourné une valeur sans se bloquer. L’événement **appelé** (**UIA \_ Invoke \_ InvokedEventId**) doit être déclenché avant de traiter la requête **Invoke** dans les scénarios suivants :
    -   Il n’est pas possible ou pratique d’attendre que l’action soit terminée.
    -   L’action requiert une intervention de l’utilisateur.
    -   L’action prend du temps et bloque le client pendant un long moment.
-   Si l’appel du contrôle a des effets secondaires significatifs, ces effets secondaires doivent être exposés via la propriété **HelpText** . Par exemple, même si [**IUIAutomationInvokePattern :: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) n’est pas associé à la sélection, **Invoke** peut faire en sorte qu’un autre contrôle soit sélectionné.
-   Les effets de survol (ou de pointage avec la souris) ne constituent généralement pas un événement **appelé** . Toutefois, les contrôles qui exécutent une action (par opposition à un effet visuel) en fonction de l’état de survol doivent prendre en charge le modèle de contrôle **Invoke** .
    > [!Note]  
    > Cette implémentation est considérée comme un problème d’accessibilité si le contrôle ne peut être appelé que suite à un effet secondaire lié à la souris.

     

-   L’appel d’un contrôle est différent de la sélection d’un élément. Toutefois, selon le contrôle, l’appel peut avoir comme effet secondaire la sélection de l’élément. par exemple, l’appel d’un élément de liste de documents Microsoft Word dans le dossier mes Documents sélectionne l’élément et ouvre le document.
-   Un élément peut disparaître de l’arborescence de l’automatisation de l’interface utilisateur de Microsoft immédiatement lors de son appel. La requête d’informations de l’élément fourni par le rappel d’événement peut échouer. La pré-récupération des informations mises en cache est la solution recommandée.
-   Les contrôles peuvent implémenter plusieurs modèles de contrôle. par exemple, le contrôle **Fill Color** dans la barre d’outils Microsoft Excel implémente à la fois les modèles de contrôle Invoke et [ExpandCollapse](uiauto-implementingexpandcollapse.md) . Le modèle de contrôle ExpandCollapse expose le menu et le modèle de contrôle **Invoke** remplit la sélection active avec la couleur choisie.

## <a name="required-members-for-iinvokeprovider"></a>Membres requis pour **IInvokeProvider**

La méthode suivante est requise pour l’implémentation de l’interface [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) .



| Membres nécessaires                                | Type de membre | Notes                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Appeler**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | Méthode      | **Invoke** est un appel asynchrone et doit être retourné immédiatement sans blocage.<br/> Ce comportement est particulièrement critique pour les contrôles qui, directement ou indirectement, lancent une boîte de dialogue modale lorsqu’ils sont appelés. Tout client UI Automation à l’origine de l’événement reste bloqué jusqu’à la fermeture de la boîte de dialogue modale. <br/> |



 

Ce modèle de contrôle n’est associé à aucune propriété ni à aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)
</dt> </dl>

 

 





