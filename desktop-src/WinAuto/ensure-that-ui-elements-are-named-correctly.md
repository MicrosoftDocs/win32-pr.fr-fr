---
title: S’assurer que les éléments d’interface utilisateur sont correctement nommés
description: Cette rubrique décrit la méthode correcte pour spécifier les noms des éléments d’interface utilisateur dans vos applications Microsoft Win32 afin que Microsoft Active Accessibility puisse exposer avec précision les noms aux applications clientes par le biais du IAccessible \ 32 ; Propriété Name.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c047228159e011ffa9a0842f1748ee07e6af4a49ff296ae8ed65b494b8c53f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052763"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a>S’assurer que les éléments d’interface utilisateur sont correctement nommés

Cette rubrique décrit la méthode correcte pour spécifier les noms des éléments d’interface utilisateur dans vos applications Microsoft Win32 afin que Microsoft Active Accessibility puisse exposer avec précision les noms aux applications clientes via la [propriété de nom](name-property.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

Les informations contenues dans cette section s’appliquent uniquement à Microsoft Active Accessibility. Elle ne s’applique pas aux applications qui utilisent Microsoft UI Automation ou à celles basées sur des langages de balisage tels que HTML, DHTML (Dynamic HTML) ou XML.

-   [Vue d'ensemble](#overview)
-   [Comment des noms incorrects provoquent des problèmes](#how-incorrect-naming-causes-problems)
-   [Comment MSAA obtient la propriété Name](#how-msaa-gets-the-name-property)
-   [Comment rechercher et corriger les problèmes de nom](#how-to-find-and-correct-naming-problems)
-   [Comment nommer correctement un TrackBar](#how-to-correctly-name-a-trackbar)
-   [Comment utiliser des étiquettes invisibles pour nommer des contrôles](#how-to-use-invisible-labels-to-name-controls)
-   [Comment utiliser l’annotation directe pour spécifier la propriété Name](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [Étapes pour l’annotation de la propriété Name](#steps-for-annotating-the-name-property)
    -   [Exemple d’annotation de la propriété Name](#example-of-annotating-the-name-property)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Dans Microsoft Active Accessibility, chaque élément d’interface utilisateur d’une application est représenté par un objet qui expose l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Les applications clientes utilisent les propriétés et les méthodes de l’interface **IAccessible** pour interagir avec l’élément d’interface utilisateur et pour récupérer des informations à leur sujet. L’une des propriétés les plus importantes exposées par l’interface **IAccessible** est la [propriété Name](name-property.md). Les applications clientes s’appuient sur la propriété Name pour rechercher, identifier ou annoncer un élément d’interface utilisateur à l’utilisateur. Si Microsoft Active Accessibility ne peut pas exposer correctement la propriété Name d’un élément d’interface utilisateur particulier, les applications clientes ne peuvent pas présenter cet élément d’interface utilisateur à l’utilisateur, et l’élément d’interface utilisateur est inaccessible aux utilisateurs handicapés.

## <a name="how-incorrect-naming-causes-problems"></a>Comment des noms incorrects provoquent des problèmes

Pour illustrer les problèmes causés par une dénomination incorrecte des éléments d’interface utilisateur, prenez en compte le formulaire d’entrée de nom présenté dans l’illustration suivante.

![illustration d’un formulaire simple pour entrer le prénom et le nom](images/incorrect-form.png)

Bien que les éléments de l’interface utilisateur du formulaire semblent OK, l’implémentation par programmation est incorrecte. Pour un client Microsoft Active Accessibility, tel qu’un lecteur d’écran, la [propriété Name](name-property.md) du contrôle d’édition Top est « Last Name : », et la propriété Name du contrôle d’édition Bottom est une chaîne vide (""). Le lecteur d’écran lit le contrôle d’édition du haut comme « Last Name », bien que l’utilisateur soit supposé taper dans le prénom. Le lecteur d’écran lira le deuxième contrôle d’édition en tant que « no name », de sorte que l’utilisateur n’aura aucune idée de type dans le deuxième contrôle d’édition. Le lecteur d’écran ne peut pas aider l’utilisateur à entrer des données dans ce formulaire simple.

Un autre problème au niveau du formulaire est qu’aucune touche de raccourci n’est assignée à l’un ou l’autre des contrôles d’édition. L’utilisateur est contraint d’utiliser l’onglet pour les contrôles ou d’utiliser la souris.

Les sections suivantes expliquent la source de ces problèmes et fournissent des instructions pour les corriger.

## <a name="how-msaa-gets-the-name-property"></a>Comment MSAA obtient la propriété Name

Microsoft Active Accessibility obtient la chaîne de [propriété de nom](name-property.md) à partir de différents emplacements en fonction du type de l’élément d’interface utilisateur. Pour la plupart des éléments d’interface utilisateur associés à du texte de fenêtre, Microsoft Active Accessibility utilise le texte de la fenêtre comme chaîne de propriété de nom. Les contrôles tels que les boutons, les éléments de menu et les info-bulles sont des exemples de ce type d’élément d’interface utilisateur.

Pour les contrôles suivants, Microsoft Active Accessibility ignore le texte de la fenêtre et cherche à la place une étiquette de texte statique (ou une étiquette de zone de groupe) qui précède immédiatement le contrôle dans l’ordre de tabulation.

-   Zones de liste modifiable
-   Sélecteurs de date et d’heure
-   Contrôles Edit et Rich Edit
-   Contrôles d’adresse IP
-   Zones de liste
-   Affichages de liste
-   Barres de progression
-   Barres
-   Contrôles statiques dotés de l' \_ icône SS ou du \_ style bitmap SS
-   Trackbars
-   Arborescences

Si les contrôles précédents ne sont pas accompagnés d’étiquettes de texte statiques, ou si les étiquettes ne sont pas implémentées correctement, Microsoft Active Accessibility ne peut pas fournir la [propriété de nom](name-property.md) correcte aux applications clientes.

La plupart des contrôles précédents disposent en fait d’un texte de fenêtre associé. L’éditeur de ressources génère automatiquement le texte de la fenêtre, qui se compose d’une chaîne générique telle que « Edit1 » ou « ListBox3 ». Bien que les développeurs puissent remplacer le texte de fenêtre généré par du texte plus explicite, le plus jamais. Étant donné que le texte de la fenêtre générée n’a aucune signification pour l’utilisateur, Microsoft Active Accessibility l’ignore et utilise à la place l’étiquette de texte statique qui l’accompagne.

## <a name="how-to-find-and-correct-naming-problems"></a>Comment rechercher et corriger les problèmes de nom

Dans le formulaire d’entrée de nom qui s’affiche dans la manière dont les noms incorrects provoquent des problèmes, la cause de ces problèmes est que l’ordre de tabulation des contrôles est incorrect. L’examen de l’interface utilisateur avec un outil de test tel que l' [inspection](inspect-objects.md) révèle les problèmes de la hiérarchie d’objets. La capture d’écran suivante montre la hiérarchie d’objets rompus du formulaire de saisie de nom tel qu’il apparaît dans inspecter.

![capture d’écran de l’outil d’inspection montrant une hiérarchie d’objets incorrecte du formulaire de saisie de nom](images/incorrect-object-hierarchy.png)

Dans la capture d’écran précédente, vous remarquerez que la hiérarchie d’objets ne correspond pas à la structure des contrôles tels qu’ils apparaissent dans l’interface utilisateur du formulaire d’entrée de nom. Notez également que l' [inspection](inspect-objects.md) a affecté le nom incorrect au dernier élément (il s’agit du contrôle d’édition pour entrer le prénom et doit être un nom nommé « First Name : »). Enfin, Notez que l’inspection n’a pas pu trouver de nom pour le dernier élément (il s’agit du contrôle d’édition pour entrer le nom de famille et doit avoir le nom « Last Name : ».

L’exemple suivant montre le contenu du fichier de ressources pour le formulaire d’entrée de nom. Notez que l’ordre de tabulation n’est pas cohérent avec la structure logique des contrôles tels qu’ils apparaissent dans l’interface utilisateur. Notez également qu’aucune touche de raccourci n’est spécifiée pour les deux contrôles d’édition.

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

Pour résoudre les problèmes liés au formulaire d’entrée de nom, le fichier de ressources (. RC) doit être modifié pour spécifier des raccourcis clavier et les contrôles doivent être placés dans l’ordre suivant :

1.  Étiquette de texte statique « &First Name : ».
2.  Le contrôle d’édition pour l’entrée du prénom (IDC \_ Edit1).
3.  Étiquette de texte statique « &nom : ».
4.  Le contrôle d’édition pour la saisie du nom (IDC \_ Edit2).
5.  Bouton de commande par défaut « OK ».

L’exemple suivant montre le fichier de ressources corrigé pour le formulaire d’entrée de nom :

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

Pour apporter des corrections à un fichier de ressources, vous pouvez modifier directement le fichier ou utiliser l’outil d’ordre de tabulation dans Microsoft Visual Studio. vous pouvez accéder à l’outil d’ordre de tabulation dans Visual Studio soit en appuyant sur CTRL + D, soit en sélectionnant **ordre de tabulation** dans le menu **Format** .

Après avoir corrigé et reconstruit l’application, l’interface utilisateur du formulaire de saisie des noms est identique à celle qui était auparavant utilisée. Toutefois, Microsoft Active Accessibility fournira à présent les propriétés de nom correctes aux applications clientes et définira le focus correctement quand l’utilisateur appuie sur les raccourcis clavier ALT + F ou ALT + L. En outre, l' [inspection](inspect-objects.md) affiche la hiérarchie d’objets correcte, comme le montre la capture d’écran suivante.

![capture d’écran de l’outil Explorateur accessible montrant une hiérarchie d’objets correcte du formulaire d’entrée de nom](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a>Comment nommer correctement un TrackBar

Lors de la définition d’un TrackBar (ou d’un curseur), assurez-vous que l’étiquette de texte statique principale pour la barre de défilement s’affiche avant le TrackBar et que les étiquettes de texte statique pour les plages minimale et maximale apparaissent après le TrackBar. N’oubliez pas que Microsoft Active Accessibility utilise l’étiquette de texte statique qui précède immédiatement un contrôle comme [propriété de nom](name-property.md) pour le contrôle. Le fait de placer l’étiquette de texte statique principale juste avant le TrackBar, et les autres étiquettes ultérieures, garantit que Microsoft Active Accessibility fournit la propriété de nom correcte à un client.

L’illustration suivante montre un TrackBar typique avec une étiquette de texte statique principale appelée « Speed » et des étiquettes de texte statiques pour les plages minimum (« min ») et maximum (« max »).

![illustration d’un contrôle TrackBar qui a une étiquette principale et des étiquettes pour les plages minimale et maximale](images/speed-trackbar.png)

L’exemple suivant illustre la façon correcte de définir un TrackBar et ses étiquettes de texte statiques dans le fichier de ressources :

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a>Comment utiliser des étiquettes invisibles pour nommer des contrôles

Il n’est pas toujours possible ou souhaitable d’avoir une étiquette visible pour chaque contrôle. Par exemple, l’ajout d’étiquettes peut parfois entraîner des modifications indésirables dans l’apparence de l’interface utilisateur. Dans ce cas, vous pouvez utiliser des étiquettes invisibles. Microsoft Active Accessibility récupère toujours le texte associé à une étiquette invisible, mais l’étiquette n’apparaît pas dans l’interface utilisateur visuel ou en interfère avec celle-ci.

Comme avec les étiquettes visibles, une étiquette invisible doit immédiatement précéder le contrôle dans l’ordre de tabulation. Pour rendre une étiquette invisible dans un fichier de ressources (. RC), ajoutez `NOT WS_VISIBLE` ou `|~WS_VISIBLE` à la partie de style du contrôle de texte statique. si vous utilisez l’éditeur de ressources dans Visual Studio, vous pouvez définir la propriété Visible sur false.

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a>Comment utiliser l’annotation directe pour spécifier la propriété Name

les proxys par défaut inclus dans le composant d’exécution Microsoft Active Accessibility, Oleacc.dll fournissent automatiquement un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour tous les contrôles de Windows standard. si vous personnalisez un contrôle de Windows standard, les proxies par défaut font de leur mieux pour fournir avec précision toutes les propriétés **IAccessible** pour votre contrôle personnalisé. Vous devez tester minutieusement un contrôle personnalisé pour vous assurer que les proxies par défaut fournissent des valeurs de propriété précises et complètes. Si le test révèle des valeurs de propriété inexactes ou incomplètes, vous pourrez peut-être utiliser la technique d’annotation dynamique appelée annotation directe pour fournir des valeurs de propriété correctes et ajouter celles qui sont manquantes.

Notez que l’annotation dynamique n’est pas seulement pour les contrôles pris en charge par les proxies Microsoft Active Accessibility. Vous pouvez également l’utiliser pour modifier ou fournir des propriétés pour tout contrôle qui fournit sa propre implémentation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

Cette section se concentre sur l’utilisation de l’annotation directe pour fournir une valeur correcte pour la [propriété Name](name-property.md) de l’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour un contrôle. Vous pouvez utiliser l’annotation directe pour fournir également d’autres valeurs de propriétés. En outre, d’autres techniques d’annotation dynamique à côté des annotations directes sont disponibles, et les fonctionnalités et fonctionnalités de l’API d’annotation dynamique s’étendent bien au-delà de ce qui est décrit dans cette section. Pour plus d’informations sur les annotations dynamiques, consultez [API d’annotation dynamique](dynamic-annotation-api.md).

### <a name="steps-for-annotating-the-name-property"></a>Étapes pour l’annotation de la propriété Name

L’utilisation de l’annotation directe pour modifier la [propriété Name](name-property.md) d’un contrôle implique les étapes suivantes.

1.  Incluez les fichiers d’en-tête suivants :
    -   Initguid. h
    -   Oleacc. h

    > [!Note]  
    > Pour définir des GUID, vous devez inclure Initguid. h avant oleacc. h dans le même fichier.

     

2.  Initialisez la bibliothèque COM (Component Object Model) en appelant la fonction [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) , en général pendant le processus d’initialisation de l’application.
3.  Peu après la création du contrôle cible (en général, pendant le message [WM \_ INITDIALOG](../dlgbox/wm-initdialog.md) ), créez une instance du gestionnaire d’annotations et obtenez un pointeur vers son pointeur [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
4.  Annotez la [propriété Name](name-property.md) du contrôle cible à l’aide de la méthode [**IAccPropServices :: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) .

5.  Libère le pointeur [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
6.  Avant de détruire le contrôle cible (en général, lors de la gestion du message [WM \_ Destroy](../winmsg/wm-destroy.md) ), créez une instance du gestionnaire d’annotations et obtenez un pointeur vers son interface [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
7.  Utilisez la méthode [**IAccPropServices :: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) pour effacer les annotations de [propriété de nom](name-property.md) du contrôle cible.
8.  Libère le pointeur [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
9.  Avant de quitter votre application (en général, lors du traitement du message [WM \_ Destroy](../winmsg/wm-destroy.md) ), libérez la bibliothèque com en appelant la fonction [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .

La fonction [**IAccPropServices :: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) accepte cinq paramètres. Les trois premiers,*HWND*, *idObject* et *idChild*, s’associent pour identifier le contrôle. Le quatrième paramètre, *idProp*, spécifie l’identificateur de la propriété à modifier. Pour modifier la [propriété Name](name-property.md), définissez *idProp* sur **propid \_ ACC \_ nom**. (Pour obtenir la liste des autres propriétés que vous pouvez définir via l’annotation directe, consultez [utilisation de l’annotation directe](using-direct-annotation.md).) Le dernier paramètre de **SetHwndPropStr**, *Str*, est la nouvelle chaîne à utiliser comme propriété Name.

### <a name="example-of-annotating-the-name-property"></a>Exemple d’annotation de la propriété Name

L’exemple de code suivant montre comment utiliser l’annotation directe pour modifier la [propriété Name](name-property.md) de l’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour un contrôle. Pour simplifier les choses, l’exemple utilise une chaîne codée en dur (« New Control Name ») pour définir la propriété Name. Les chaînes codées en dur ne doivent pas être utilisées dans la version finale de votre application, car elles ne peuvent pas être localisées. Au lieu de cela, chargez toujours des chaînes à partir de votre fichier de ressources. En outre, l’exemple n’affiche pas les appels aux fonctions [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[API d’annotation dynamique](dynamic-annotation-api.md)
</dt> <dt>

[Fourniture de la propriété Name](providing-the-name-property.md)
</dt> <dt>

[Outils de test](testing-tools.md)
</dt> </dl>

 

 