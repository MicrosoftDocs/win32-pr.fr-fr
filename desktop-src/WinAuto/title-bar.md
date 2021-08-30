---
title: Barre de titre (référence des éléments d’interface utilisateur MSAA)
description: La barre de titre en haut d’une fenêtre affiche une icône et une ligne de texte définies par l’application.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 620fa8716cb498857cdf12c652b99f409e6e4214
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480125"
---
# <a name="title-bar-msaa-ui-element-reference"></a>Barre de titre (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **barre de titre** à des fins de référence d’élément d’interface utilisateur MSAA. La procédure de création d’objets de **barre de titre** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

La barre de titre en haut d’une fenêtre affiche une icône et une ligne de texte définies par l’application. Le texte spécifie le nom de l’application et indique l’objectif de la fenêtre. La barre de titre permet également à l’utilisateur de déplacer la fenêtre à l’aide d’une souris ou d’un autre dispositif de pointage.

Les barres de titre contiennent au moins trois petits boutons qui permettent de réduire, d’agrandir ou de restaurer et de fermer la fenêtre associée à la barre de titre. Les barres de titre contiennent également un bouton d’aide contextuelle. les Applications qui s’exécutent dans la Far-East version du système d’exploitation Windows peuvent également contenir des boutons de l’éditeur de méthode d’entrée (IME). Microsoft Active Accessibility expose ces boutons en tant qu’éléments enfants de la barre de titre.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Les barres de titre prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Les barres de titre prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :




| Propriété | Commentaires | 
|----------|----------|
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a> | La propriété <strong>ChildCount</strong> est cinq. La propriété <strong>ChildCount</strong> comprend l’éditeur IME et les boutons d’aide contextuelle, même lorsqu’ils ne sont pas affichés. Les boutons qui ne sont pas affichés ont la propriété <strong>State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>. | 
| <strong>get_accDescription</strong> | La propriété <strong>Description</strong> de la barre de titre elle-même est : « affiche le nom de la fenêtre et contient des contrôles pour la manipuler ». Les boutons enfants de la barre de titre présentent les descriptions suivantes :<br /><ul><li>"Déplace la fenêtre hors de</li><li>«Rend la fenêtre complète</li><li>«Place un réduit ou</li><li>« Ferme la fenêtre »</li><li>«Entre ou quitte le contexte-</li><li>« Affiche le clavier quand vous appuyez sur »</li></ul> | 
| <strong>get_accName</strong> | La barre de titre elle-même ne prend pas en charge la propriété <strong>Name</strong> . Les boutons enfants de la barre de titre portent les noms suivants :<ul><li>Icône</li><li>« Agrandir » ou « restaurer »,</li><li>« Fermer »</li><li>« Aide contextuelle »</li><li>DICAUX</li></ul> | 
| <strong>get_accParent</strong> | La propriété <strong>parent</strong> de la barre de titre est la fenêtre d’application principale ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) qui a le même nom de classe de fenêtre définie par l’application que la barre de titre. | 
| <strong>get_accRole</strong> | La propriété de <strong>rôle</strong> est <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>. Les boutons enfants de la barre de titre ont la propriété <strong>Role</strong> <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>. | 
| <strong>get_accState</strong> | La propriété <strong>State</strong> pour la barre de titre et les boutons enfants peuvent être une combinaison d’une ou plusieurs des <a href="object-state-constants.md">valeurs</a>suivantes : <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a><br /> | 
| <strong>get_accValue</strong> | La propriété <strong>valeur</strong> est une chaîne qui est identique au texte affiché dans la barre de titre. | 




 

## <a name="notes"></a>Notes

-   Bien que la barre de titre d’une application ait la propriété **État** indicateur de l’état du système, elle n’a jamais le [**\_ \_ focus**](object-state-constants.md)sur le système d’état de l’indicateur d' **État** . [**\_ \_**](object-state-constants.md) La définition du focus sur un objet de barre de titre est axée sur la fenêtre d’application.
-   Étant donné que l’objet de barre de titre ne prend pas en charge l' [**affichage des \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), les boutons de la barre de titre sont des éléments simples. Ils ne prennent pas en charge l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proprement dit. L’objet barre de titre fournit des informations sur ces boutons enfants.
-   Comme les barres de titre n’obtiennent pas le focus et n’ont pas d’action par défaut, les méthodes [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) et [**\_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) ne sont pas prises en charge pour ce contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





