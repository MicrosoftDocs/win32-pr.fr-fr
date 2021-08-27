---
title: Caret (référence des éléments de l’interface utilisateur MSAA)
description: Le signe insertion est une ligne, un bloc ou un bitmap clignotant dans la zone cliente d’une fenêtre ou dans un contrôle qui accepte les entrées au clavier.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f846940a9180885da84cf8a030672b1473eab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467296"
---
# <a name="caret-msaa-ui-element-reference"></a>Caret (référence des éléments de l’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les signes de référence des éléments d’interface utilisateur MSAA. L’utilisation des signes d’insertion dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Le signe insertion est une ligne, un bloc ou un bitmap clignotant dans la zone cliente d’une fenêtre ou dans un contrôle qui accepte les entrées au clavier. Elle indique l’endroit où le texte ou les graphiques sont insérés. Étant donné qu’une seule fenêtre à la fois a le focus clavier, il n’y a qu’un seul signe insertion dans le système.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Le signe insertion prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Le signe insertion prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :




| Propriété | Commentaires | 
|----------|----------|
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a> | La propriété <strong>ChildCount</strong> est égale à zéro. | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a> | La propriété <strong>Name</strong> est « Edit ». | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a> | La propriété de <strong>rôle</strong> est <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>. | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a> | Les valeurs possibles pour la propriété <strong>State</strong> sont les suivantes :<ul><li>Zéro, ce qui signifie que le signe insertion est visible</li><li><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></li></ul> | 




 

## <a name="notes"></a>Notes

-   Contrairement à d’autres éléments d’interface utilisateur, l’objet caret n’a pas de handle de fenêtre associé. Pour obtenir l’accès à l’objet Caret, les clients doivent définir un [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) et attendre que l’objet caret génère des événements.
-   l’objet caret dans le contrôle rich edit fourni par Riched20.dll (utilisé dans les éditeurs de texte tels que Microsoft WordPad dans Windows 98) n’envoie pas de [WinEvents](winevents-infrastructure.md) lorsque sa position est modifiée pendant la sélection de texte. Quand les utilisateurs appuient sur la touche Maj et les touches de direction pour sélectionner du texte, l’objet caret ne déclenche pas l' [**objet d’événement \_ \_ LOCATIONCHANGE**](event-constants.md) WinEvent. De même, lorsque la sélection est définie par programme par le biais de messages Rich Edit, l’objet caret n’envoie aucun événement pour indiquer sa nouvelle position.

    Toutes les applications qui utilisent Riched20.dll présentent ce problème. Les applications qui utilisent des versions antérieures du contrôle RichEdit envoient correctement les événements en fonction de la sélection.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




