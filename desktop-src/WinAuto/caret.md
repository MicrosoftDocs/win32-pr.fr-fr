---
title: Caret (référence des éléments de l’interface utilisateur MSAA)
description: Le signe insertion est une ligne, un bloc ou un bitmap clignotant dans la zone cliente d’une fenêtre ou dans un contrôle qui accepte les entrées au clavier.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103841830"
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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Commentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></td>
<td>La propriété <strong>ChildCount</strong> est égale à zéro.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></td>
<td>La propriété <strong>Name</strong> est &quot; Edit &quot; .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></td>
<td>La propriété de <strong>rôle</strong> est <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></td>
<td>Les valeurs possibles pour la propriété <strong>State</strong> sont les suivantes :
<ul>
<li>Zéro, ce qui signifie que le signe insertion est visible</li>
<li><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Notes

-   Contrairement à d’autres éléments d’interface utilisateur, l’objet caret n’a pas de handle de fenêtre associé. Pour obtenir l’accès à l’objet Caret, les clients doivent définir un [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) et attendre que l’objet caret génère des événements.
-   L’objet caret dans le contrôle RichEdit fourni par Riched20.dll (qui est utilisé dans les éditeurs de texte tels que Microsoft WordPad dans Windows 98) n’envoie pas de [winEvents](winevents-infrastructure.md) lorsque sa position est modifiée pendant la sélection de texte. Quand les utilisateurs appuient sur la touche Maj et les touches de direction pour sélectionner du texte, l’objet caret ne déclenche pas l' [**objet d’événement \_ \_ LOCATIONCHANGE**](event-constants.md) WinEvent. De même, lorsque la sélection est définie par programme par le biais de messages Rich Edit, l’objet caret n’envoie aucun événement pour indiquer sa nouvelle position.

    Toutes les applications qui utilisent Riched20.dll présentent ce problème. Les applications qui utilisent des versions antérieures du contrôle RichEdit envoient correctement les événements en fonction de la sélection.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




