---
title: Slider, contrôle (référence des éléments d’interface utilisateur MSAA)
description: Un contrôle Slider, également appelé contrôle TrackBar, permet à un utilisateur de sélectionner une plage de valeurs en déplaçant un curseur. Les contrôles de volume dans le système d'exploitation Windows sont des contrôles Slider.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029782"
---
# <a name="slider-control-msaa-ui-element-reference"></a>Slider, contrôle (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **contrôle Slider** à des fins de référence des éléments d’interface utilisateur MSAA. La création d’objets de **contrôle Slider** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Un contrôle Slider, également appelé contrôle TrackBar, permet à un utilisateur de sélectionner une plage de valeurs en déplaçant un curseur. Les contrôles de volume dans le système d'exploitation Windows sont des contrôles Slider.

Le nom de la classe de fenêtre pour un contrôle Slider est la \_ classe TrackBar, qui est définie comme « msctls \_ TrackBar » dans commctrl. h.

Le contenu des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) varie selon que le curseur est vertical ou horizontal et sur lequel des parties suivantes du contrôle Slider sont interrogées par le client :

-   Fenêtre curseur
-   Curseur curseur
-   Zone grise au-dessus (ou à
-   Zone ombrée en dessous (ou à droite de) curseur de défilement

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Un contrôle Slider prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Un contrôle Slider prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**Obtient \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**Obtient \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**obtenir \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut): la propriété **KeyboardShortcut** est la clé d’accès de la fenêtre du curseur, qui est un caractère souligné dans le texte de l’étiquette du curseur. La chaîne retournée contient le caractère clé d’accès ajouté à la chaîne « ALT + ».
-   [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la propriété **Name** dépend de la partie du curseur interrogée.

    Les parties d’un curseur vertical portent les noms suivants :

    

    | Composant Slider                    | Nom                                |
    |--------------------------------|-------------------------------------|
    | Fenêtre curseur                  | Contrôle de texte statique utilisé comme étiquette |
    | Curseur curseur                   | Endroit                          |
    | Curseur de la zone ombrée au-dessus du curseur | « Page précédente »                           |
    | Zone ombrée en dessous du curseur de curseur | « Page suivante »                         |

    

     

    Les parties d’un curseur horizontal portent les noms suivants :

    

    | Composant Slider                              | Nom                                |
    |------------------------------------------|-------------------------------------|
    | Fenêtre curseur                            | Contrôle de texte statique utilisé comme étiquette |
    | Curseur curseur                             | Endroit                          |
    | Zone ombrée à gauche du curseur de curseur  | « Page gauche »                         |
    | Zone ombrée à droite du curseur de curseur | « Page droite »                        |

    

     

-   [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): la propriété **parente** des boutons fléchés, Scroll Thumb et la zone ombrée de chaque côté du curseur de défilement est la fenêtre de curseur. La propriété **parent** de la fenêtre de curseur est une fenêtre ( [**\_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et qui a les mêmes nom de propriété de **nom** et de classe de fenêtre.
-   [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propriété **role** dépend de la partie du curseur interrogée. 

    | Composant Slider                                     | [Rôle](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | Fenêtre curseur                                   | [**\_curseur système de rôle \_**](object-roles.md)         |
    | Curseur curseur                                    | [**\_indicateur de système de rôle \_**](object-roles.md)   |
    | Zones ombrées de part et d’autre du curseur de curseur | [**\_PUSHBUTTON système de rôle \_**](object-roles.md) |

    

     

-   [**obtenir \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): les [valeurs](object-state-constants.md) de la propriété **State** dépendent de la partie du curseur interrogée. 

    | Composant Slider                                     | Valeurs d’État possibles                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Fenêtre curseur                                   | [**État \_ système \_ d'**](object-state-constants.md) État indisponible système d’État indisponible système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système d’état \| [**\_ \_ centré**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md) |
    | Curseur curseur                                    | Zéro (0), ce qui signifie que l’objet est visible, ou le système d’état [**système état \_ \_**](object-state-constants.md) non disponible système d’état \| [**\_ \_ non disponible**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)                                                                                                                       |
    | Zones ombrées de part et d’autre du curseur de curseur | Zéro (0), ce qui signifie que l’objet est visible, ou le système d’état [**système état \_ \_**](object-state-constants.md) non disponible système d’état \| [**\_ \_ non disponible**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)                                                                                                                       |

    

     

-   [**obtenir \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la propriété **value** de la fenêtre Slider indique la position du curseur et est une chaîne qui contient un entier compris entre « 0 » et « 100 ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barre de défilement**](scroll-bar.md)
</dt> </dl>

 

 




