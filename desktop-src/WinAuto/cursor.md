---
title: Cursor (référence des éléments d’interface utilisateur MSAA)
description: Un curseur est une petite image dont l’emplacement sur l’écran est contrôlé par un dispositif de pointage, tel qu’une souris, un stylet ou un Trackball. lorsque l’utilisateur déplace le dispositif de pointage, le système d’exploitation Windows déplace le curseur.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124524"
---
# <a name="cursor-msaa-ui-element-reference"></a>Cursor (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les curseurs à des fins de référence des éléments d’interface utilisateur MSAA. L’utilisation de curseurs dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Un curseur est une petite image dont l’emplacement sur l’écran est contrôlé par un dispositif de pointage, tel qu’une souris, un stylet ou un Trackball. lorsque l’utilisateur déplace le dispositif de pointage, le système d’exploitation Windows déplace le curseur.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Un curseur prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Un curseur prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la propriété **ChildCount** est égale à zéro.
-   [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): les développeurs peuvent créer des curseurs personnalisés ou utiliser les curseurs prédéfinis qui sont identifiés par leur ID de curseur. La propriété **Name** du curseur dépend de sa forme et est l’un des éléments suivants : 

    | Forme de curseur     | Nom              |
    |------------------|-------------------|
    | Curseur personnalisé    | Connue         |
    | \_flèche IDC       | "Normal"          |
    | \_pointeur en I IDC       | Modifiés            |
    | \_attente IDC        | Qu'            |
    | Inter. IDC \_       | Représentation         |
    | \_flèche vers le haut IDC     | Les              |
    | \_SIZENWSE IDC    | "Nose size"       |
    | \_SIZENESW IDC    | « Taille NESO »       |
    | \_SIZEWE IDC      | « Taille horizontale » |
    | \_SIZENS IDC      | "Taille verticale"   |
    | \_SIZEALL IDC     | Activer            |
    | IDC \_ non          | Forbidden       |
    | \_APPSTARTING IDC | « Démarrage de l’application »       |
    | \_aide d’IDC        | Sur            |

    

     

-   [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propriété **role** est [**un \_ \_ curseur de système de rôle**](object-roles.md).
-   [**obtenir \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la propriété **State** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes :

    [**État \_ système \_**](object-state-constants.md) d’État invisible du système, \| [ **\_ \_ flottant**](object-state-constants.md)

## <a name="notes"></a>Notes

-   Contrairement à d’autres éléments d’interface utilisateur, l’objet Cursor n’a pas de handle de fenêtre associé. Pour obtenir l’accès à l’objet Cursor, les clients doivent définir un [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) et attendre que l’objet Cursor génère des événements.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




