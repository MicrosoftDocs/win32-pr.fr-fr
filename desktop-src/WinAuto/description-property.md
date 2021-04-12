---
title: Description, propriété (fonctionnalités d’accessibilité Windows)
description: La propriété Description d’un objet fournit une description textuelle de l’apparence visuelle d’un objet.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464150"
---
# <a name="description-property-windows-accessibility-features"></a>Description, propriété (fonctionnalités d’accessibilité Windows)

> [!Note]  
> La propriété **Description** est souvent utilisée de manière incorrecte et n’est pas prise en charge par Microsoft UI Automation. Les développeurs Microsoft Active Accessibility Server ne doivent pas utiliser cette propriété. Si des informations supplémentaires sont nécessaires pour l’accessibilité et les scénarios d’automatisation, utilisez les propriétés prises en charge par les éléments UI Automation et les modèles de contrôle.

 

La propriété **Description** d’un objet fournit une description textuelle de l’apparence visuelle d’un objet. La description est principalement utilisée pour fournir un contexte plus grand pour les utilisateurs malvoyants ou aveugles, mais elle est également utilisée pour la recherche de contexte ou d’autres applications. Cette propriété peut aider les utilisateurs à comprendre une icône ou l’apparence visuelle globale.

La propriété **Description** est récupérée en appelant [**IAccessible :: \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).

## <a name="when-to-support-the-description-property"></a>Quand prendre en charge la propriété Description

Les serveurs prennent en charge la propriété **Description** si la description n’est pas évidente ou lorsqu’elle n’est pas redondante en fonction des propriétés [**Name**](name-property.md), [**role**](role-property.md), [**State**](state-property.md)et [**value**](value-property.md) de l’objet. Par exemple, un bouton intitulé « OK » n’a pas besoin d’informations supplémentaires, alors qu’un bouton qui affiche une image d’un cactus. Le **nom**, le **rôle** et les propriétés d' [**aide**](help-property.md) d’un tel bouton décrivent son rôle, mais la propriété **Description** transmet des informations moins tangibles. par exemple, « ce bouton affiche une image d’un cactus ».

Un serveur Microsoft Active Accessibility peut ajouter la prise en charge d’UI Automation en utilisant l' [annotation directe](direct-annotation.md), à l’aide de l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , ou en implémentant Microsoft Active Accessibility et UI Automation côte à côte avec les deux implémentations qui gèrent le message [**WM \_ GETOBJECT**](wm-getobject.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’annotation directe](using-direct-annotation.md)
</dt> <dt>

[Interface IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




