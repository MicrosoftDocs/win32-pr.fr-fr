---
title: Transform (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de ITransformProvider et ITransformProvider2, y compris des informations sur les propriétés et les méthodes.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- UI Automation, implémenter le modèle de contrôle Transform
- UI Automation, transformation (modèle de contrôle)
- UI Automation, ITransformProvider
- ITransformProvider
- implémentation des modèles de contrôle Transform d’UI Automation
- Transformer les modèles de contrôle
- modèles de contrôle, ITransformProvider
- modèles de contrôle, implémenter une transformation UI Automation
- modèles de contrôle, transformer
- interfaces, ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403980"
---
# <a name="transform-control-pattern"></a>Transform (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) et [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle Transform est utilisé pour prendre en charge les contrôles qui peuvent être déplacés, redimensionnés ou pivotés dans un espace à deux dimensions.

Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **ITransformProvider**](#required-members-for-itransformprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **Transform** , notez les conventions et recommandations suivantes :

-   La prise en charge pour ce modèle de contrôle ne se limite pas aux objets sur le bureau. Ce modèle de contrôle doit également être pris en charge par les enfants d’un objet conteneur si les enfants peuvent être déplacés, redimensionnés et pivotés librement dans les limites du conteneur.
-   Il n’est pas possible de déplacer, redimensionner ni pivoter un objet de manière à ce que son emplacement résultant à l’écran soit complètement en dehors des coordonnées de son conteneur et, par conséquent, inaccessible via le clavier et la souris (par exemple, quand une fenêtre de niveau supérieur est déplacée hors de l’écran ou qu’un objet enfant est déplacé en dehors des limites de la fenêtre d’affichage du conteneur). Dans ce cas, l’objet est placé le plus près possible des coordonnées d’écran demandées avec les coordonnées en haut et à gauche substituées de façon à être incluses dans les limites du conteneur.
-   Pour les systèmes à plusieurs écrans, si un objet est déplacé, redimensionné ou pivoté complètement en dehors des coordonnées d’écran du bureau combiné, l’objet est placé sur le moniteur principal, aussi près que possible des coordonnées demandées.
-   Tous les paramètres et valeurs de propriété sont absolus et indépendants des paramètres régionaux.

## <a name="required-members-for-itransformprovider"></a>Membres requis pour **ITransformProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .



| Membres nécessaires                                         | Type de membre | Notes |
|----------------------------------------------------------|-------------|-------|
| [**CanMove**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | Propriété    | None  |
| [**CanResize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | Propriété    | None  |
| [**CanRotate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | Propriété    | None  |
| [**Activer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | Méthode      | None  |
| [**Redimensionner**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | Méthode      | None  |
| [**Faire pivoter**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | Méthode      | None  |



 

Les propriétés et méthodes supplémentaires suivantes sont requises pour implémenter l’interface [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .



| Membres nécessaires                                              | Type de membre | Notes |
|---------------------------------------------------------------|-------------|-------|
| [**CanZoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | Propriété    | None  |
| [**Zoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | Méthode      | None  |
| [**ZoomByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | Méthode      | None  |
| [**ZoomLevel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | Propriété    | None  |
| [**ZoomMaximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | Propriété    | None  |
| [**ZoomMinimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | Propriété    | None  |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 