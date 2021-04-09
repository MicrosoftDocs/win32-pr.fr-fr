---
title: Alternatives à l’annotation dynamique
description: Alternatives à l’annotation dynamique
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101884"
---
# <a name="alternatives-to-dynamic-annotation"></a><span data-ttu-id="cbdb1-103">Alternatives à l’annotation dynamique</span><span class="sxs-lookup"><span data-stu-id="cbdb1-103">Alternatives to Dynamic Annotation</span></span>

<span data-ttu-id="cbdb1-104">Il existe d’autres façons de fournir une prise en charge de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) personnalisée pour les éléments d’interface utilisateur et, dans certains cas, il s’agit de la solution correcte.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-104">There are other ways to provide customized [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support for UI elements, and in some cases, they are the correct solution.</span></span> <span data-ttu-id="cbdb1-105">Avant l’annotation dynamique, ces techniques alternatives étaient les seules options disponibles pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-105">Prior to Dynamic Annotation, these alternative techniques were the only options available to developers.</span></span> <span data-ttu-id="cbdb1-106">Elles incluent l’implémentation de l’ensemble de l’interface **IAccessible** et des techniques de programmation.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-106">They include implementing all of the **IAccessible** interface and programmatic techniques.</span></span>

## <a name="implementing-all-of-the-iaccessible-interface"></a><span data-ttu-id="cbdb1-107">Implémentation de l’ensemble de l’interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="cbdb1-107">Implementing All of the IAccessible Interface</span></span>

<span data-ttu-id="cbdb1-108">Une autre technique consiste à implémenter l’ensemble de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="cbdb1-108">One alternative technique is to implement all of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="cbdb1-109">Cette approche est souvent nécessaire pour les contrôles personnalisés ou des éléments d’interface utilisateur radicalement différents. Toutefois, les coûts de développement et de test sont suffisamment importants pour être évités, sauf si cela est véritablement nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-109">This approach is often necessary for custom controls or radically different UI elements; however, the development and test costs are significant enough that it should be avoided unless truly necessary.</span></span> <span data-ttu-id="cbdb1-110">Si l’objectif est de modifier une seule propriété, le coût est difficile à justifier.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-110">If the goal is to modify a single property, the cost is difficult to justify.</span></span>

## <a name="programmatic-techniques"></a><span data-ttu-id="cbdb1-111">Techniques de programmation</span><span class="sxs-lookup"><span data-stu-id="cbdb1-111">Programmatic Techniques</span></span>

<span data-ttu-id="cbdb1-112">Une autre option consiste à utiliser des techniques de sous-classe et d’habillage pour modifier les informations exposées pour une propriété spécifique.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-112">Another option is to use subclassing and wrapping techniques to modify the information being exposed for a specific property.</span></span> <span data-ttu-id="cbdb1-113">Il s’agit de la technique que l’annotation dynamique est destinée à remplacer.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-113">This is the technique that Dynamic Annotation is intended to replace.</span></span> <span data-ttu-id="cbdb1-114">Pour remplacer une seule propriété à l’aide de la sous-classe et de l’encapsulation, le développeur doit effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cbdb1-114">To override a single property by using subclassing and wrapping, the developer must perform the following steps:</span></span>

1.  <span data-ttu-id="cbdb1-115">Sous-classe le HWND de l’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="cbdb1-115">Subclass the HWND of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object.</span></span>
2.  <span data-ttu-id="cbdb1-116">Interceptez le message [**WM \_ GETOBJECT**](wm-getobject.md) pour la valeur IParam/objid correcte.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-116">Intercept the [**WM\_GETOBJECT**](wm-getobject.md) message for the correct IParam/OBJID value.</span></span>
3.  <span data-ttu-id="cbdb1-117">Transférez le message [**WM \_ GETOBJECT**](wm-getobject.md) à la classe de base à l’aide de la fonction [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cbdb1-117">Forward the [**WM\_GETOBJECT**](wm-getobject.md) message to the base class using the [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) function.</span></span> <span data-ttu-id="cbdb1-118">Si la valeur zéro est retournée, appelez [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); Sinon, appelez [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) sur la valeur retournée pour obtenir le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) natif du contrôle.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-118">If zero is returned, call [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); otherwise, call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) on the returned value to obtain the control's native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
4.  <span data-ttu-id="cbdb1-119">Créer une classe wrapper, qui implémente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et encapsule le pointeur d’interface **IAccessible** retourné à partir de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-119">Create a wrapper class, which implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and wraps the **IAccessible** interface pointer returned from the previous step.</span></span> <span data-ttu-id="cbdb1-120">Cette classe wrapper envoie toutes les méthodes et propriétés au pointeur d’interface **IAccessible** d’origine, à l’exception de celles qui doivent être remplacées.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-120">This wrapper class sends all methods and properties to the original **IAccessible** interface pointer, except those that are to be overridden.</span></span> <span data-ttu-id="cbdb1-121">Cela implique l’écriture d’un code de transfert pour toutes les propriétés et méthodes de l’interface **IAccessible** , quel que soit le nombre réellement remplacé.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-121">This involves writing forwarding code for all of the **IAccessible** interface's 21 properties and methods, regardless of how many are actually overridden.</span></span>

<span data-ttu-id="cbdb1-122">En outre, les développeurs doivent vérifier les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="cbdb1-122">Also, developers must verify the following conditions:</span></span>

-   <span data-ttu-id="cbdb1-123">La méthode ou la propriété substituée doit gérer uniquement les ID enfants requis et transférer toutes les autres vers le pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) d’origine.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-123">The overridden method or property must only handle the required child IDs, and forward all others to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
-   <span data-ttu-id="cbdb1-124">L’encapsulage doit également transférer les interfaces [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) et [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) uniquement si l’objet d’origine les prend en charge.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-124">Wrapping must also forward [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) and [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) interfaces only if the original object supports them.</span></span>
-   <span data-ttu-id="cbdb1-125">Le décompte de références doit être géré correctement, en particulier si d’autres interfaces sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-125">Reference counting must be handled correctly, especially if other interfaces are supported.</span></span>
-   <span data-ttu-id="cbdb1-126">Les valeurs de retour [**IDispatch**](idispatch-interface.md) doivent être gérées correctement, en particulier avec la méthode [**ITypeInfo :: Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) , qui doit être appelée avec un pointeur d’interface vers l’interface de wrapper, et non un pointeur vers l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) d’origine.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-126">[**IDispatch**](idispatch-interface.md) return values must be handled correctly, especially with the [**ITypeInfo::Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) method, which must be called with an interface pointer to the wrapper interface, not a pointer to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span>

<span data-ttu-id="cbdb1-127">Ces techniques nécessitent une quantité considérable de travail, même si une seule ou deux propriétés doivent être remplacées.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-127">These techniques require a considerable amount of work, even if only one or two properties need to be overridden.</span></span> <span data-ttu-id="cbdb1-128">La majorité du code résultant s’intéresse à la sous-classe et à l’encapsulation, et seule une petite fraction fournit les informations remplacées.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-128">The majority of the resulting code is concerned with subclassing and wrapping, and only a small fraction is actually providing the overridden information.</span></span>

<span data-ttu-id="cbdb1-129">Toutefois, il existe des scénarios dans lesquels ces techniques sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-129">However, there are scenarios in which these techniques are needed.</span></span> <span data-ttu-id="cbdb1-130">Par exemple, si vous apportez des modifications structurelles pour créer un élément d’interface utilisateur d’espace réservé, vous devez utiliser ces techniques plutôt que des annotations dynamiques.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-130">For example, if you are making structural changes to create a placeholder UI element, then you should use these techniques rather than Dynamic Annotation.</span></span>

## <a name="fixing-names-derived-from-labels"></a><span data-ttu-id="cbdb1-131">Correction des noms dérivés d’étiquettes</span><span class="sxs-lookup"><span data-stu-id="cbdb1-131">Fixing Names Derived from Labels</span></span>

<span data-ttu-id="cbdb1-132">Certains contrôles communs Microsoft Win32, tels que le contrôle zone d’édition, sont presque toujours utilisés avec une étiquette (une entrée LTEXT dans le fichier de ressources) ou une zone de groupe (GROUPBOX dans le fichier de ressources).</span><span class="sxs-lookup"><span data-stu-id="cbdb1-132">Some Microsoft Win32 common controls, such as the edit box control, are nearly always used with a label (an LTEXT entry in the resource file) or a group box (GROUPBOX in the resource file).</span></span> <span data-ttu-id="cbdb1-133">Microsoft Active Accessibility dérive automatiquement la propriété Name du contrôle à partir de son étiquette.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-133">Microsoft Active Accessibility automatically derives the name property of the control from its label.</span></span> <span data-ttu-id="cbdb1-134">Pour ces contrôles, le texte de la fenêtre (affiché dans Microsoft Visual Studio comme propriété Name ou ID) est ignoré, car il est généralement généré automatiquement et rarement très descriptif. par exemple, « IDC \_ Edit1 ».</span><span class="sxs-lookup"><span data-stu-id="cbdb1-134">For such controls, the window text (shown in Microsoft Visual Studio as the Name or ID property) is ignored, because it is usually autogenerated and seldom very descriptive; for example, "IDC\_EDIT1".</span></span>

<span data-ttu-id="cbdb1-135">Si l’interface utilisateur de l’application n’est pas conçue correctement, Microsoft Active Accessibility peut ne pas être en mesure de définir le nom correctement.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-135">If the user interface of the application is not designed correctly, Microsoft Active Accessibility might not be able to set the name correctly.</span></span> <span data-ttu-id="cbdb1-136">Pour être associé à un contrôle, la zone d’étiquette ou de groupe doit être placée immédiatement avant le contrôle dynamique dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-136">To be associated with a control, the label or group box must be placed immediately before the dynamic control in the tab order.</span></span>

<span data-ttu-id="cbdb1-137">L’ordre de tabulation peut être modifié à l’aide de l’outil dans Visual Studio (dans le menu **format** lorsque l’éditeur de ressources est ouvert) ou en modifiant directement le fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-137">Tab order can be changed by using the tool in Visual Studio (on the **Format** menu when the resource editor is open) or by directly editing the resource file.</span></span>

<span data-ttu-id="cbdb1-138">L’exemple suivant illustre la description d’un fichier de ressources d’une boîte de dialogue qui contient deux zones d’édition étiquetées.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-138">The following example shows a resource file's description of a dialog box that contains two labeled edit boxes.</span></span>


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



<span data-ttu-id="cbdb1-139">Dans cet exemple, les étiquettes et les contrôles ne sont pas répertoriés dans l’ordre de tabulation correct.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-139">In this example, the labels and controls are not listed in the correct tab order.</span></span> <span data-ttu-id="cbdb1-140">Par conséquent, Microsoft Active Accessibility affecte le nom « Last Name » à la zone d’édition de nom et n’a aucun nom dans la zone de modification Last-Name.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-140">As a result, Microsoft Active Accessibility assigns the name "Last Name" to the first-name edit box, and no name at all to the last-name edit box.</span></span>

<span data-ttu-id="cbdb1-141">L’exemple suivant illustre la liste des ressources correcte.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-141">The following example shows the correct resource listing.</span></span> <span data-ttu-id="cbdb1-142">Notez également que les touches de raccourci ont été désignées dans les étiquettes.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-142">Note also that shortcut keys have been designated in the labels.</span></span>


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



<span data-ttu-id="cbdb1-143">Lorsque les contrôles ont des étiquettes supplémentaires, telles que les valeurs minimale et maximale d’un TrackBar, ces étiquettes doivent être placées après le contrôle dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-143">When controls have supplementary labels, such as for minimum and maximum values on a trackbar, these labels should be placed after the control in the tab order.</span></span> <span data-ttu-id="cbdb1-144">L’étiquette principale du contrôle doit apparaître immédiatement avant le contrôle lui-même.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-144">The main label of the control must appear immediately before the control itself.</span></span>

## <a name="naming-controls-without-labels"></a><span data-ttu-id="cbdb1-145">Nommer des contrôles sans étiquettes</span><span class="sxs-lookup"><span data-stu-id="cbdb1-145">Naming Controls Without Labels</span></span>

<span data-ttu-id="cbdb1-146">Il n’est pas toujours possible ou souhaitable d’avoir une étiquette visible pour chaque contrôle.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-146">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="cbdb1-147">Toutefois, vous pouvez toujours fournir un nom pour le contrôle en ajoutant une étiquette invisible.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-147">However, you can still provide a name for the control by adding an invisible label.</span></span> <span data-ttu-id="cbdb1-148">Comme toujours, l’étiquette invisible doit immédiatement précéder le contrôle dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-148">As always, the invisible label must immediately precede the control in the tab order.</span></span>

<span data-ttu-id="cbdb1-149">Si vous utilisez l’éditeur de ressources dans Microsoft Visual Studio .NET, vous pouvez définir la propriété visible sur false.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-149">If you are using the Resource Editor in Microsoft Visual Studio .NET, you can set the Visible property to False.</span></span> <span data-ttu-id="cbdb1-150">Pour rendre l’étiquette invisible quand vous modifiez le fichier de ressources (. RC), ajoutez non WS \_ visible ou à la partie de style du contrôle Label, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-150">To make the label invisible when editing the resource file (.rc), add NOT WS\_VISIBLE or to the style part of the label control, as shown in the following example.</span></span>


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



<span data-ttu-id="cbdb1-151">Notez que toute touche de raccourci désignée fonctionne même si l’étiquette est invisible.</span><span class="sxs-lookup"><span data-stu-id="cbdb1-151">Note that any designated shortcut key works even though the label is invisible.</span></span>

 

 