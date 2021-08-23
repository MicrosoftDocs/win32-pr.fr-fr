---
title: Client, objet (référence de l’élément d’interface utilisateur MSAA)
description: La zone cliente est la partie d’une fenêtre dans laquelle l’application affiche la sortie, par exemple du texte ou des graphiques. Par exemple, une application de publication de bureau affiche la page active d’un document dans la zone cliente.
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33190ebd1013c92a58ecc64b07993a5a5ae1cd842e50c88691295114a128074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645059"
---
# <a name="client-object-msaa-ui-element-reference"></a>Client, objet (référence de l’élément d’interface utilisateur MSAA)

La zone cliente est la partie d’une fenêtre dans laquelle l’application affiche la sortie, par exemple du texte ou des graphiques. Par exemple, une application de publication de bureau affiche la page active d’un document dans la zone cliente.

Les développeurs d’applications serveur sont responsables de la création d’objets accessibles qui fournissent des informations sur le contenu de la zone cliente de l’application.

Si une application cliente demande des informations sur un élément d’interface utilisateur personnalisé dans une application, et l’élément d’interface utilisateur personnalisé qui ne prend pas en charge l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , Microsoft Active Accessibility crée un objet accessible par défaut avec des informations minimales.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

La zone cliente prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

La zone cliente prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Envoie le message [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) pour récupérer le texte de la fenêtre.                                                                                                                                                                                                                                                                                                                                                                                |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété de **rôle** est [**client de \_ système \_ de rôle**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

