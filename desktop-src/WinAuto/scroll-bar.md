---
title: Barre de défilement (référence des éléments d’interface utilisateur MSAA)
description: Les barres de défilement permettent à un utilisateur de choisir la direction et la distance pour faire défiler les informations dans une fenêtre ou une zone de liste associée. Le nom de la classe de fenêtre pour une barre de défilement est \ 0034 ; BARRE DE DÉFILEMENT \ 0034 ;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031801"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a>Barre de défilement (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **barre de défilement** à des fins de référence des éléments d’interface utilisateur MSAA. La création d’objets de **barre de défilement** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Les barres de défilement permettent à un utilisateur de choisir la direction et la distance pour faire défiler les informations dans une fenêtre ou une zone de liste associée. Le nom de la classe de fenêtre d’une barre de défilement est « SCROLLBAR ».

Le contenu des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) varie selon que la barre de défilement est verticale ou horizontale et sur laquelle des parties suivantes de la barre de défilement sont interrogées par le client :

-   Barre de défilement elle-même
-   Bouton flèche haut ou droite
-   Bouton de flèche bas ou gauche
-   La case de défilement (Thumb)
-   La page précédente ou la région de la page droite
-   La page suivante ou la zone de page de gauche

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Une barre de défilement prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction): l’objet de barre de défilement lui-même et le curseur de défilement ne prennent pas en charge la méthode **accDoDefaultAction** .

    Pour les autres parties de la barre de défilement sur une barre de défilement verticale, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) appelle [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec le message [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll) avec *wParam* défini sur les valeurs suivantes.

    

    | Bouton/région       | Valeur        |
    |---------------------|--------------|
    | Bouton de flèche haut    | \_gamme SB   |
    | Bouton de flèche bas | SB \_ LINEDOWN |
    | Zone de page précédente      | SB \_ PG PRÉC   |
    | Zone de page suivante    | SB \_ PG. |

    

     

    Pour les autres parties de la barre de défilement sur une barre de défilement horizontale, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) appelle [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec le message [**WM \_ HSCROLL**](/windows/desktop/Controls/wm-hscroll) avec *wParam* défini sur les valeurs suivantes.

    

    | Bouton/région      | Valeur         |
    |--------------------|---------------|
    | Bouton de direction gauche  | \_LINELEFT SB  |
    | Bouton flèche droite | \_LINERIGHT SB |
    | Zone de gauche de la page   | \_PAGELEFT SB  |
    | Région de droite de la page  | \_ÉPINGLÉE SB |

    

     

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Une barre de défilement prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**obtenir \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la propriété **ChildCount** de l’objet de barre de défilement est cinq. Pour les autres parties de la barre de défilement, la propriété **ChildCount** est égale à zéro.
-   [**Obtient \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction): l’objet de barre de défilement lui-même et le curseur de défilement ne prennent pas en charge la propriété **DefaultAction** . La propriété **DefaultAction** pour les boutons fléchés et les zones ombrées de chaque côté du curseur de défilement est « Press ».
-   [**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)— la propriété **Description** dépend de la partie de la barre de défilement qui est interrogée.

    Les parties d’une barre de défilement verticale présentent les descriptions suivantes.

    

    | Partie                | Description                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | Barre de défilement elle-même   | « Utilisé pour modifier la zone d’affichage verticale »                                          |
    | Bouton de flèche haut    | "Déplace la position verticale d’une ligne vers le haut"                                           |
    | Bouton de flèche bas | « Déplace la position verticale d’une ligne vers le dessous »                                         |
    | Défilement de curseur        | « Indique la position verticale actuelle et peut être glissée pour la modifier directement » |
    | Zone de page précédente      | "Déplace la position verticale de quelques lignes"                                  |
    | Zone de page suivante    | « Indique la position verticale actuelle et peut être glissée pour la modifier directement » |

    

     

    Les parties d’une barre de défilement horizontale ont les descriptions suivantes.

    

    | Partie               | Description                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | Barre de défilement elle-même  | « Utilisé pour modifier la zone d’affichage horizontale »                                          |
    | Bouton de direction gauche  | « Déplace la position horizontale d’une colonne vers la gauche »                                       |
    | Bouton flèche droite | 'Déplace la position horizontale d’une colonne vers la droite "                                      |
    | Défilement de curseur       | « Indique la position horizontale actuelle et peut être glissée pour la modifier directement » |
    | Zone de gauche de la page   | "Déplace la position horizontale de deux colonnes"                              |
    | Région de droite de la page  | « Indique la position verticale actuelle et peut être glissée pour la modifier directement »   |

    

     

-   [**Obtient \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**Obtient \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la propriété **Name** dépend de la partie de la barre de défilement qui est interrogée.

    Les parties d’une barre de défilement verticale portent les noms suivants.

    | Partie                | Nom        |
    |---------------------|-------------|
    | Fenêtre barre de défilement   | Barr  |
    | Bouton de flèche haut    | « Aligner vers le haut »   |
    | Bouton de flèche bas | « Ligne inférieure » |
    | Défilement de curseur        | Endroit  |
    | Zone de page précédente      | « Page précédente »   |
    | Zone de page suivante    | « Page suivante » |

    

     

    Les parties d’une barre de défilement horizontale portent les noms suivants.

    

    | Partie               | Nom           |
    |--------------------|----------------|
    | Fenêtre barre de défilement  | Horizontal   |
    | Bouton de direction gauche  | « Colonne à gauche »  |
    | Bouton flèche droite | « Colonne à droite » |
    | Défilement de curseur       | Endroit     |
    | Région de droite de la page  | « Page droite »   |
    | Zone de gauche de la page   | « Page gauche »    |

    

     

-   [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)— la propriété **parente** des boutons fléchés, le curseur de défilement et la zone ombrée de chaque côté du curseur sont la fenêtre de la barre de défilement. La propriété **parent** de la fenêtre de la barre de défilement est une fenêtre ( \_ fenêtre système de rôle \_ ) qui entoure le contrôle et qui a les mêmes nom de propriété de **nom** et de classe de fenêtre.
-   [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propriété **role** dépend de la partie de la barre de défilement qui est interrogée. Les parties d’une barre de défilement ont les rôles suivants. 

    | Partie                                                  | Role                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | Barre de défilement elle-même                                     | [**\_ScrollBar système de rôle \_**](object-roles.md)   |
    | Boutons haut, bas, gauche et flèche droite              | [**\_PUSHBUTTON système de rôle \_**](object-roles.md) |
    | Défilement de curseur                                          | [**\_indicateur de système de rôle \_**](object-roles.md)   |
    | Zones de page précédente, page suivante, page de gauche et page de droite | [**\_PUSHBUTTON système de rôle \_**](object-roles.md) |

    

     

-   [**obtenir \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la propriété **State** de chaque composant de barre de défilement comprend une combinaison des [valeurs](object-state-constants.md)suivantes.

    | State                                                                                 | Valeur                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**système d’état \_ \_ invisible**](object-state-constants.md)     | Pour la barre de défilement elle-même, cela indique que la barre de défilement verticale ou horizontale spécifiée n’existe pas. Pour les zones page précédente ou page suivante, cela indique que le curseur est positionné de telle sorte que la région n’existe pas. |
    | [**système d’état \_ \_ hors écran**](object-state-constants.md)     | Pour la barre de défilement elle-même, cela indique que la fenêtre est dimensionnée de telle sorte que la barre de défilement verticale ou horizontale spécifiée ne soit pas actuellement affichée.                                                                         |
    | [**système d’état \_ \_ enfoncé**](object-state-constants.md)         | Le bouton fléché ou la région de page est enfoncé.                                                                                                                                                                                 |
    | [**système d’état \_ \_ non disponible**](object-state-constants.md) | Le composant est désactivé.                                                                                                                                                                                                  |

    

     

-   [**obtenir \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la propriété **valeur** de la fenêtre barre de défilement indique la position de la barre de défilement et est une chaîne qui contient un entier compris entre « 0 » et « 100 ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 