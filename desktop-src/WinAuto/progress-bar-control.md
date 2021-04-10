---
title: Contrôle de barre de progression (référence des éléments d’interface utilisateur MSAA)
description: Les contrôles de barre de progression indiquent la progression d’une opération longue, par exemple le téléchargement d’un fichier à partir d’Internet. En général, la progression est exprimée sous la forme d’un pourcentage compris entre zéro (0) et 100 (100).
ms.assetid: 9165d00e-b3f3-41cd-812c-cd39313460fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9bbd9a648ee1c4d4f112577c8e41a5983f69038
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197143"
---
# <a name="progress-bar-control-msaa-ui-element-reference"></a>Contrôle de barre de progression (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **contrôle de barre de progression** à des fins de référence d’élément d’interface utilisateur MSAA. La procédure de création d’objets de **contrôle de barre de progression** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Les contrôles de barre de progression indiquent la progression d’une opération longue, par exemple le téléchargement d’un fichier à partir d’Internet. En général, la progression est exprimée sous la forme d’un pourcentage compris entre zéro (0) et 100 (100).

Le nom de la classe de fenêtre pour un contrôle de barre de progression est la \_ classe Progress, qui est définie comme « msctls \_ Progress » dans commctrl. h.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Les contrôles de barre de progression prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Les contrôles de barre de progression prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propriété **ChildCount** est égale à zéro.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propriété **KeyboardShortcut** est la clé d’accès de la barre de progression, qui est un caractère souligné dans le texte de l’étiquette de la barre de progression. La chaîne retournée contient le caractère clé d’accès ajouté à la chaîne « ALT + ».                                                                                                                                                                                                                                 |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propriété **Name** est le texte d’un contrôle de texte statique qui étiquette la barre de progression.                                                                                                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.                                                                                                                                                                                                                                                              |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété **role** est [**le \_ \_ composant PROGRESSBAR du système de rôle**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                      |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |
| [**Obtient \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La propriété **value** est une chaîne comprise entre « 0% » et « 100% » qui décrit la progression.                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





