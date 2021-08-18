---
title: Edit, contrôle (référence des éléments d’interface utilisateur MSAA)
description: Les contrôles Edit permettent à un utilisateur d’afficher et de modifier du texte.
ms.assetid: a42c73f2-4005-4db9-84bc-637c9c4310f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3844dcdf99f925813765ae46494b0ff70345c086f3845304fff0e53d70f07d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829843"
---
# <a name="edit-control-msaa-ui-element-reference"></a>Edit, contrôle (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **contrôle d’édition** à des fins de référence des éléments d’interface utilisateur MSAA. La procédure de création d’objets de **contrôle d’édition** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Les contrôles Edit permettent à un utilisateur d’afficher et de modifier du texte. Les contrôles d’édition sont créés avec de nombreux styles différents, tels que ES \_ multiligne. ce style crée un contrôle d’édition multiligne, tel que la zone cliente de Bloc-notes et ES \_ READONLY, qui crée un contrôle d’édition en lecture seule.

Microsoft Active Accessibility ne fait pas de distinction entre les contrôles d’édition créés avec le nom de classe de fenêtre « EDIT » et les contrôles RichEdit créés avec le nom de classe de fenêtre « RichEdit » ou « RichEdit20A ».

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Les contrôles d’édition prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Les contrôles d’édition prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propriété **KeyboardShortcut** est la clé d’accès du contrôle d’édition, qui est un caractère souligné dans le texte de l’étiquette du contrôle d’édition. Par exemple, dans une boîte de dialogue d’ouverture de fichier standard telle que dans WordPad, le **KeyboardShortcut** pour le contrôle d’édition intitulé « NomFichier : » est « ALT + n ».                                                                                                                                                                                                                                                                                                                                        |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propriété **Name** est le texte d’un contrôle de texte statique qui étiquette le contrôle d’édition. Par exemple, dans une boîte de dialogue d’ouverture de fichier standard telle que dans WordPad, la propriété **nom** du contrôle d’édition est « nom de fichier : ».                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété **role** est [**le \_ \_ texte du système de rôle**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Obtient \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système état \| [**\_ \_ actif**](object-state-constants.md) système État en \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ lecture seule**](object-state-constants.md) état système \| [**\_ \_ protégé**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) système État en lecture normale<br/> |
| [**Obtient \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La propriété **valeur** est une chaîne unique qui contient le texte dans le contrôle d’édition. Toutefois, si le contrôle est protégé par un mot de passe, la propriété **value** renvoie E \_ ACCESSDENIED. Pour les contrôles d’édition multiligne, la chaîne contient un retour chariot et un caractère de saut de ligne à la fin de chaque ligne.                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Remarques

-   Microsoft Active Accessibility ne prend pas en charge la sélection du texte contenu dans les contrôles Edit et Rich Edit, car le texte est exposé sous la forme d’une chaîne dans la propriété **value** de l’objet.
-   le contrôle richedit fourni par Riched20.dll (utilisé dans les éditeurs de texte comme WordPad dans Windows 98) n’envoie pas de WinEvents lorsque la position du signe insertion est modifiée pendant la sélection du texte. Quand les utilisateurs appuient sur la touche Maj et les touches de direction pour sélectionner du texte, l’objet caret ne déclenche pas l' [**objet d’événement \_ \_ LOCATIONCHANGE**](event-constants.md) WinEvent. Lorsque la sélection est définie par programme par le biais de messages Rich Edit, l’objet caret n’envoie aucun événement pour indiquer sa nouvelle position.

    Toutes les applications qui utilisent Riched20.dll présentent ce problème. Les applications qui utilisent des versions antérieures du contrôle RichEdit envoient correctement les événements en fonction de la sélection.

-   La valeur d' **État** pour les contrôles d’édition de mot de passe comprend toujours le système d’état des indicateurs de bits [**\_ \_ protégé**](object-state-constants.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





