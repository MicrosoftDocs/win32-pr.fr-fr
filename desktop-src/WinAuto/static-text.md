---
title: Texte statique (référence des éléments d’interface utilisateur MSAA)
description: Les contrôles de texte statique offrent un moyen pratique d’afficher du texte dans les boîtes de dialogue et d’autres fenêtres. Les contrôles de texte statique servent souvent d’étiquettes pour d’autres contrôles.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da892a102caa8a1af1729bdb4fc2258f461828adf1f7622e8ff5abf8a2a0bc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052487"
---
# <a name="static-text-msaa-ui-element-reference"></a>Texte statique (référence des éléments d’interface utilisateur MSAA)

Les contrôles de texte statique offrent un moyen pratique d’afficher du texte dans les boîtes de dialogue et d’autres fenêtres. Les contrôles de texte statique servent souvent d’étiquettes pour d’autres contrôles.

Le nom de la classe de fenêtre pour un contrôle de texte statique est « STATIC ».

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Les contrôles de texte statiques prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Les contrôles de texte statiques prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propriété **ChildCount** est égale à zéro.                                                                                                                                                                                                                                                          |
| [**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propriété **KeyboardShortcut** est la clé d’accès, qui est le caractère souligné dans le texte qui active le contrôle associé au texte statique. La chaîne retournée contient le caractère clé d’accès ajouté à la chaîne « ALT + ».                                           |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propriété **Name** est la même que le texte du contrôle de texte statique.                                                                                                                                                                                                                     |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.                                                                                   |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété **role** est le [**système de rôle \_ \_ STATICTEXT**](object-roles.md).                                                                                                                                                                                             |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété **State** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : système d’état [**\_ \_ ReadOnly**](object-state-constants.md) système d’état \| [**\_ \_ invisible**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notes

-   La méthode [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) retourne DISP \_ E \_ MEMBERNOTFOUND quand elle est appelée avec [**SELFLAG \_ TAKEFOCUS**](selflag.md) sur un objet texte statique.
-   Les contrôles statiques avec le \_ style d’icône SS retournent des données non valides dans la propriété **Name** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





