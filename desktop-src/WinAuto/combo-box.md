---
title: Zone de liste déroulante (référence des éléments d’interface utilisateur MSAA)
description: Une zone de liste modifiable est une zone de liste associée à un contrôle statique ou à un contrôle d’édition qui affiche dans la zone de liste l’élément actuellement sélectionné.
ms.assetid: 3fb2c0b0-507f-4520-845b-b3fbfd9e7b60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce42bb3b0316b0fb2668fed23564b8f904fc793
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520904"
---
# <a name="combo-box-msaa-ui-element-reference"></a>Zone de liste déroulante (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **zone de liste déroulante** à des fins de référence des éléments d’interface utilisateur MSAA. La création d’objets de **zone de liste déroulante** dans diverses infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Une zone de liste modifiable est une zone de liste associée à un contrôle statique ou à un contrôle d’édition qui affiche dans la zone de liste l’élément actuellement sélectionné. La partie zone de liste du contrôle est affichée en permanence ou uniquement lorsque l’utilisateur sélectionne la flèche de déroulement (qui est un bouton de commande) à côté du contrôle. Si le champ de sélection est un contrôle d’édition, l’utilisateur peut entrer des informations qui ne sont pas dans la liste ; dans le cas contraire, l’utilisateur ne peut sélectionner que les éléments de la liste.

Le nom de la classe de fenêtre pour une zone de liste déroulante est « COMBOBOX ».

Le contenu des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dépend de l’une des parties suivantes de la zone de liste déroulante interrogée par le client :

-   Fenêtre de zone de liste déroulante
-   Contrôle d’édition ou contrôle de texte statique
-   La flèche déroulante (qui est un bouton de commande)
-   Zone de liste
-   Éléments de liste dans la zone de liste

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Les zones de liste déroulante prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Les zones de liste déroulante prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**obtenir \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)— le tableau suivant montre la valeur du nombre d’enfants pour les différentes parties de la zone de liste déroulante. 

    | Partie de zone de liste déroulante   | ChildCount               |
    |------------------|--------------------------|
    | Fenêtre de zone de liste déroulante | 3                        |
    | Contrôle Edit     | 0                        |
    | Flèche déroulante  | 0                        |
    | Zone de liste         | Nombre d’éléments de liste |
    | Élément de liste        | 0                        |

    

     

-   [**obtenir \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)— le tableau suivant présente la propriété **DefaultAction** pour les différentes parties d’une zone de liste déroulante. 

    | Partie de zone de liste déroulante   | Nœud                                                  |
    |------------------|----------------------------------------------------------------|
    | Fenêtre de zone de liste déroulante | None                                                           |
    | Contrôle Edit     | None                                                           |
    | Flèche déroulante  | « Ouvrir » ou « fermer » en fonction de l’état de la liste déroulante |
    | Zone de liste         | None                                                           |
    | Élément de liste        | « Double-clic »                                                 |

    

     

-   [**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**Obtient \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**Obtient \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**obtenir \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)— le tableau suivant présente la propriété **KeyboardShortcut** pour les différentes parties d’une zone de liste déroulante. 

    | Partie de zone de liste déroulante   | KeyboardShortcut               |
    |------------------|--------------------------------|
    | Fenêtre de zone de liste déroulante | Clé d’accès de l’étiquette associée |
    | Contrôle Edit     | None                           |
    | Flèche déroulante  | « Alt + flèche bas »               |
    | Zone de liste         | None                           |
    | Élément de liste        | None                           |

    

     

    La clé d’accès d’une zone de liste déroulante est le caractère souligné dans le texte d’un contrôle de texte statique associé qui étiquette la zone de liste déroulante. Par exemple, dans une boîte de dialogue Ouvrir standard qui ouvre des fichiers, par exemple dans Microsoft WordPad, la zone de liste déroulante intitulée « fichiers de type : » a le **KeyboardShortcut** « Alt + t ».

-   [**obtenir \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)— le tableau suivant présente la propriété **Name** pour les différentes parties d’une zone de liste déroulante. 

    | Partie de zone de liste déroulante   | Nom                                                           |
    |------------------|----------------------------------------------------------------|
    | Fenêtre de zone de liste déroulante | Contrôle de texte statique utilisé comme étiquette                            |
    | Contrôle Edit     | Contrôle de texte statique utilisé comme étiquette                            |
    | Flèche déroulante  | « Ouvrir » ou « fermer » en fonction de l’état de la liste déroulante |
    | Zone de liste         | Étiquette associée                                               |
    | Élément de liste        | Texte de l’élément de liste                                          |

    

     

    La propriété de **nom** d’une zone de liste déroulante, son contrôle d’édition enfant et sa zone de liste enfant sont le texte d’un contrôle de texte statique associé qui étiquette la zone de liste déroulante. Par exemple, dans une boîte de dialogue Ouvrir standard qui ouvre des fichiers, par exemple dans WordPad, les propriétés de **nom** pour les deux zones de liste déroulante sont « regarder dans : » et « fichiers de type : ».

-   [**obtenir \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): le tableau suivant montre la valeur parente pour les différentes parties d’une zone de liste déroulante. 

    | Partie de zone de liste déroulante                        | Parent                                                                                                                                                                                                         |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Fenêtre de zone de liste déroulante                      | Fenêtre avec la propriété **role** de la [**\_ \_ fenêtre du système de rôle**](object-roles.md) qui entoure la zone de liste déroulante et a les mêmes propriété **Name** et Name Class Name que la zone de liste déroulante. |
    | Contrôle d’édition (ou contrôle de texte statique) | Fenêtre de zone de liste déroulante.                                                                                                                                                                                          |
    | Flèche déroulante                       | Fenêtre de zone de liste déroulante.                                                                                                                                                                                          |
    | Fenêtre parente de zone de liste                | Fenêtre de zone de liste déroulante. Cette fenêtre entoure la zone de liste.                                                                                                                                                      |
    | Zone de liste                              | Fenêtre parente de la zone de liste.                                                                                                                                                                                    |
    | Élément de liste                             | Zone de liste.                                                                                                                                                                                                  |

    

     

-   [**obtenir \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)— le tableau suivant présente la propriété **role** pour les différentes parties d’une zone de liste déroulante. 

    | Partie de zone de liste déroulante                        | [Rôle](object-roles.md)                                                                                                               |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
    | Fenêtre de zone de liste déroulante                      | [**\_ComboBox système de rôle \_**](object-roles.md)                                                                    |
    | Contrôle d’édition (ou contrôle de texte statique) | [**Rôle \_ \_Texte système**](object-roles.md) ou [ **système de rôle \_ \_ STATICTEXT**](object-roles.md) |
    | Flèche déroulante                       | [**\_PUSHBUTTON système de rôle \_**](object-roles.md)                                                                |
    | Zone de liste                              | [**\_liste des systèmes de rôles \_**](object-roles.md)                                                                            |
    | Élément de liste                             | [**\_ListItem du système de rôle \_**](object-roles.md)                                                                    |

    

     

-   [**obtenir \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)— le tableau suivant présente la propriété **State** pour les différentes parties d’une zone de liste déroulante. 

    | Partie de zone de liste déroulante   | [États possibles](object-state-constants.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
    |------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Fenêtre de zone de liste déroulante | [**État \_ système \_ d'**](object-state-constants.md) État indisponible système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système d’État centré sur le système d’état \| [**\_ \_ centré**](object-state-constants.md) sur \| [**\_ \_ le**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) d’état normal système d’état développé système d’état développé |
    | Contrôle Edit     | [**État \_ système \_ d'**](object-state-constants.md) État indisponible système d’État indisponible système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système d’état \| [**\_ \_ centré**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)                                                                                                                                                                         |
    | Flèche déroulante  | 0, ce qui signifie que le bouton est visible et non enfoncé ; ou système d’État sur lequel le système d’État est [**\_ \_ appuyé**](object-state-constants.md) système d’état \| [**\_ \_ invisible**](object-state-constants.md) \| \_ \_ normal                                                                                                                                                                                                                                                                                                                                                    |
    | Zone de liste         | [**État \_ système \_ d'**](object-state-constants.md) État indisponible système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système d’État centré sur le système d’état \| [**\_ \_ centré**](object-state-constants.md) sur \| [**\_ \_ le**](object-state-constants.md) système d’état \| [**\_ \_ flottant**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)                                                                                      |
    | Élément de liste        | [**État \_ état \_ du système d'**](object-state-constants.md) État du système d’état actif système d’état \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ ciblé**](object-state-constants.md) système d’état sélectionné système d’état \| [**\_ \_ Sélectionner**](object-state-constants.md) le système d’état \| [**\_ \_ sélectionné**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)                                                                                        |

    

     

-   [**obtenir \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)— le tableau suivant présente la propriété **valeur** pour les différentes parties d’une zone de liste déroulante. 

    | Partie de zone de liste déroulante   | Valeur                                |
    |------------------|--------------------------------------|
    | Fenêtre de zone de liste déroulante | Texte de l’élément de liste actuellement sélectionné |
    | Contrôle Edit     | Texte de l’élément de liste actuellement sélectionné |
    | Flèche déroulante  | None                                 |
    | Zone de liste         | None                                 |
    | Élément de liste        | None                                 |

    

     

## <a name="notes"></a>Notes

-   Quand [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) est appelé avec l’indicateur [**NAVDIR \_ Next**](navigation-constants.md) sur la partie de la zone de liste d’une zone de liste déroulante, il accède de manière incorrecte à la fenêtre de la barre d’État lorsqu’il doit retourner **VT \_ vide**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




