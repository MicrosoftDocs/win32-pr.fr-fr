---
title: Alternatives à l’annotation dynamique
description: Alternatives à l’annotation dynamique
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af7582ec0fa3f317a0fabbdde0474c6a2e4d0b361062243d7518edf317477ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122429"
---
# <a name="alternatives-to-dynamic-annotation"></a>Alternatives à l’annotation dynamique

Il existe d’autres façons de fournir une prise en charge de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) personnalisée pour les éléments d’interface utilisateur et, dans certains cas, il s’agit de la solution correcte. Avant l’annotation dynamique, ces techniques alternatives étaient les seules options disponibles pour les développeurs. Elles incluent l’implémentation de l’ensemble de l’interface **IAccessible** et des techniques de programmation.

## <a name="implementing-all-of-the-iaccessible-interface"></a>Implémentation de l’ensemble de l’interface IAccessible

Une autre technique consiste à implémenter l’ensemble de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Cette approche est souvent nécessaire pour les contrôles personnalisés ou des éléments d’interface utilisateur radicalement différents. Toutefois, les coûts de développement et de test sont suffisamment importants pour être évités, sauf si cela est véritablement nécessaire. Si l’objectif est de modifier une seule propriété, le coût est difficile à justifier.

## <a name="programmatic-techniques"></a>Techniques de programmation

Une autre option consiste à utiliser des techniques de sous-classe et d’habillage pour modifier les informations exposées pour une propriété spécifique. Il s’agit de la technique que l’annotation dynamique est destinée à remplacer. Pour remplacer une seule propriété à l’aide de la sous-classe et de l’encapsulation, le développeur doit effectuer les étapes suivantes :

1.  Sous-classe le HWND de l’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
2.  Interceptez le message [**WM \_ GETOBJECT**](wm-getobject.md) pour la valeur IParam/objid correcte.
3.  Transférez le message [**WM \_ GETOBJECT**](wm-getobject.md) à la classe de base à l’aide de la fonction [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) . Si la valeur zéro est retournée, appelez [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); Sinon, appelez [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) sur la valeur retournée pour obtenir le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) natif du contrôle.
4.  Créer une classe wrapper, qui implémente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et encapsule le pointeur d’interface **IAccessible** retourné à partir de l’étape précédente. Cette classe wrapper envoie toutes les méthodes et propriétés au pointeur d’interface **IAccessible** d’origine, à l’exception de celles qui doivent être remplacées. Cela implique l’écriture d’un code de transfert pour toutes les propriétés et méthodes de l’interface **IAccessible** , quel que soit le nombre réellement remplacé.

En outre, les développeurs doivent vérifier les conditions suivantes :

-   La méthode ou la propriété substituée doit gérer uniquement les ID enfants requis et transférer toutes les autres vers le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) d’origine.
-   L’encapsulage doit également transférer les interfaces [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) et [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) uniquement si l’objet d’origine les prend en charge.
-   Le décompte de références doit être géré correctement, en particulier si d’autres interfaces sont prises en charge.
-   Les valeurs de retour [**IDispatch**](idispatch-interface.md) doivent être gérées correctement, en particulier avec la méthode [**ITypeInfo :: Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) , qui doit être appelée avec un pointeur d’interface vers l’interface de wrapper, et non un pointeur vers l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) d’origine.

Ces techniques nécessitent une quantité considérable de travail, même si une seule ou deux propriétés doivent être remplacées. La majorité du code résultant s’intéresse à la sous-classe et à l’encapsulation, et seule une petite fraction fournit les informations remplacées.

Toutefois, il existe des scénarios dans lesquels ces techniques sont nécessaires. Par exemple, si vous apportez des modifications structurelles pour créer un élément d’interface utilisateur d’espace réservé, vous devez utiliser ces techniques plutôt que des annotations dynamiques.

## <a name="fixing-names-derived-from-labels"></a>Correction des noms dérivés d’étiquettes

Certains contrôles communs Microsoft Win32, tels que le contrôle zone d’édition, sont presque toujours utilisés avec une étiquette (une entrée LTEXT dans le fichier de ressources) ou une zone de groupe (GROUPBOX dans le fichier de ressources). Microsoft Active Accessibility dérive automatiquement la propriété Name du contrôle à partir de son étiquette. pour ces contrôles, le texte de la fenêtre (affiché dans Microsoft Visual Studio comme propriété Name ou ID) est ignoré, car il est généralement généré automatiquement et rarement très descriptif. par exemple, « IDC \_ Edit1 ».

Si l’interface utilisateur de l’application n’est pas conçue correctement, Microsoft Active Accessibility peut ne pas être en mesure de définir le nom correctement. Pour être associé à un contrôle, la zone d’étiquette ou de groupe doit être placée immédiatement avant le contrôle dynamique dans l’ordre de tabulation.

l’ordre de tabulation peut être modifié à l’aide de l’outil de Visual Studio (dans le menu **Format** lorsque l’éditeur de ressources est ouvert) ou en modifiant directement le fichier de ressources.

L’exemple suivant illustre la description d’un fichier de ressources d’une boîte de dialogue qui contient deux zones d’édition étiquetées.


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



Dans cet exemple, les étiquettes et les contrôles ne sont pas répertoriés dans l’ordre de tabulation correct. Par conséquent, Microsoft Active Accessibility affecte le nom « Last Name » à la zone d’édition de nom et n’a aucun nom dans la zone de modification Last-Name.

L’exemple suivant illustre la liste des ressources correcte. Notez également que les touches de raccourci ont été désignées dans les étiquettes.


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



Lorsque les contrôles ont des étiquettes supplémentaires, telles que les valeurs minimale et maximale d’un TrackBar, ces étiquettes doivent être placées après le contrôle dans l’ordre de tabulation. L’étiquette principale du contrôle doit apparaître immédiatement avant le contrôle lui-même.

## <a name="naming-controls-without-labels"></a>Nommer des contrôles sans étiquettes

Il n’est pas toujours possible ou souhaitable d’avoir une étiquette visible pour chaque contrôle. Toutefois, vous pouvez toujours fournir un nom pour le contrôle en ajoutant une étiquette invisible. Comme toujours, l’étiquette invisible doit immédiatement précéder le contrôle dans l’ordre de tabulation.

si vous utilisez l’éditeur de ressources dans Microsoft Visual Studio .net, vous pouvez définir la propriété Visible sur false. Pour rendre l’étiquette invisible quand vous modifiez le fichier de ressources (. RC), ajoutez non WS \_ visible ou à la partie de style du contrôle Label, comme indiqué dans l’exemple suivant.


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



Notez que toute touche de raccourci désignée fonctionne même si l’étiquette est invisible.

 

 