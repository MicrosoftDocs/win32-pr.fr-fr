---
title: Meilleures pratiques pour l’utilisation de groupes sécurisés
description: De nombreuses méthodes d’interface de Microsoft UI Automation \ 32 ; L’API prend des arguments appelés tableaux sécurisés, du type de données SAFEARRAY. Cette rubrique décrit les meilleures pratiques pour l’utilisation de tableaux sécurisés dans une application UI Automation.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- UI Automation, tableaux sécurisés
- UI Automation, fournisseurs
- UI Automation, clients
- UI Automation, conversion entre types de données
- clients, tableaux sécurisés
- fournisseurs, UI Automation
- tableaux sécurisés
- types de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106540765"
---
# <a name="best-practices-for-using-safe-arrays"></a><span data-ttu-id="ea44b-112">Meilleures pratiques pour l’utilisation de groupes sécurisés</span><span class="sxs-lookup"><span data-stu-id="ea44b-112">Best Practices for Using Safe Arrays</span></span>

<span data-ttu-id="ea44b-113">De nombreuses méthodes d’interface de l’API d’automatisation d’interface utilisateur de Microsoft acceptent des arguments appelés tableaux sécurisés, du type de données [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) .</span><span class="sxs-lookup"><span data-stu-id="ea44b-113">Many interface methods of the Microsoft UI Automation API take arguments called safe arrays, of the [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) data type.</span></span> <span data-ttu-id="ea44b-114">Cette rubrique décrit les meilleures pratiques pour l’utilisation de tableaux sécurisés dans une application UI Automation.</span><span class="sxs-lookup"><span data-stu-id="ea44b-114">This topic describes the best practices for using safe arrays in a UI Automation applications.</span></span>

## <a name="clients"></a><span data-ttu-id="ea44b-115">Clients</span><span class="sxs-lookup"><span data-stu-id="ea44b-115">Clients</span></span>

<span data-ttu-id="ea44b-116">Tous les tableaux sécurisés qui sont utilisés avec les méthodes de l’API du client UI Automation sont des tableaux unidimensionnels de base zéro.</span><span class="sxs-lookup"><span data-stu-id="ea44b-116">All safe arrays that are used with the UI Automation client API methods are zero-based, one-dimensional arrays.</span></span> <span data-ttu-id="ea44b-117">Pour créer un tableau sécurisé pour une méthode de client UI Automation, utilisez la fonction [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) , et pour lire et écrire dans un tableau sécurisé, utilisez les fonctions [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) et [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) .</span><span class="sxs-lookup"><span data-stu-id="ea44b-117">To create a safe array for a UI Automation client method, use the [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) function, and to read from and write to a safe array, use the [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) and [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) functions.</span></span> <span data-ttu-id="ea44b-118">Lorsque vous avez fini d’utiliser un tableau sécurisé, détruisez-le toujours à l’aide de la fonction [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) , que vous ayez créé ou reçu le tableau sécurisé à partir d’une méthode de client UI Automation.</span><span class="sxs-lookup"><span data-stu-id="ea44b-118">When you finish using a safe array, always destroy it by using the [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) function, whether you created the safe array or received it from a UI Automation client method.</span></span>

<span data-ttu-id="ea44b-119">Plusieurs méthodes UI Automation, y compris les méthodes de récupération de propriété telles que [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), récupèrent des [**variantes**](/windows/win32/api/oaidl/ns-oaidl-variant)qui peuvent contenir des structures [**point**](/previous-versions//dd162805(v=vs.85)) ou [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) .</span><span class="sxs-lookup"><span data-stu-id="ea44b-119">Several UI Automation methods, including property-retrieval methods such as [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), retrieve [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)s that can contain [**POINT**](/previous-versions//dd162805(v=vs.85)) or [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) structures.</span></span> <span data-ttu-id="ea44b-120">Un **point** est empaqueté dans un **Variant** comme un tableau sécurisé de doubles (VT \_ R8) avec le membre **x** à l’index 0, et le membre **y** à l’index 1.</span><span class="sxs-lookup"><span data-stu-id="ea44b-120">A **POINT** is packed into a **VARIANT** as a safe array of doubles (VT\_R8) with the **x** member at index 0, and the **y** member at index 1.</span></span> <span data-ttu-id="ea44b-121">De même, un **UiaRect** est empaqueté dans un **Variant** comme un tableau sécurisé de doubles avec les membres de **gauche**, de **haut**, de **largeur** et de **hauteur** aux index 0 à 3, respectivement.</span><span class="sxs-lookup"><span data-stu-id="ea44b-121">Similarly, a **UiaRect** is packed into a **VARIANT** as a safe array of doubles with the **left**, **top**, **width**, and **height** members at indexes 0 through 3, respectively.</span></span> <span data-ttu-id="ea44b-122">Pour un tableau de structures **UiaRect** , le tableau Safe contient un tableau séquentiel de quatre doubles pour chaque **UiaRect**.</span><span class="sxs-lookup"><span data-stu-id="ea44b-122">For an array of **UiaRect** structures, the safe array contains a sequential array of four doubles for each **UiaRect**.</span></span> <span data-ttu-id="ea44b-123">Les membres **gauche**, **supérieur**, **largeur** et **hauteur** du premier **UiaRect** occupent l’index 0 à 3, les membres du deuxième rectangle occupent l’index 4 jusqu’à 7, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ea44b-123">The **left**, **top**, **width**, and **height** members of the first **UiaRect** occupy index 0 through 3, the members of the second rectangle occupy index 4 through 7, and so on.</span></span>

<span data-ttu-id="ea44b-124">L’interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) comprend les méthodes suivantes pour la conversion entre [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) et différents autres types de données.</span><span class="sxs-lookup"><span data-stu-id="ea44b-124">The [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface includes the following methods for converting between [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) and various other data types.</span></span>



| <span data-ttu-id="ea44b-125">Méthode</span><span class="sxs-lookup"><span data-stu-id="ea44b-125">Method</span></span>                                                                                               | <span data-ttu-id="ea44b-126">Description</span><span class="sxs-lookup"><span data-stu-id="ea44b-126">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea44b-127">**IUIAutomation::IntNativeArrayToSafeArray**</span><span class="sxs-lookup"><span data-stu-id="ea44b-127">**IUIAutomation::IntNativeArrayToSafeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | <span data-ttu-id="ea44b-128">Convertit un tableau d’entiers en [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="ea44b-128">Converts an array of integers to a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>                                          |
| [<span data-ttu-id="ea44b-129">**IUIAutomation::IntSafeArrayToNativeArray**</span><span class="sxs-lookup"><span data-stu-id="ea44b-129">**IUIAutomation::IntSafeArrayToNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | <span data-ttu-id="ea44b-130">Convertit un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) d’entiers en tableau.</span><span class="sxs-lookup"><span data-stu-id="ea44b-130">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of integers to an array.</span></span>                                          |
| [<span data-ttu-id="ea44b-131">**IUIAutomation::SafeArrayToRectNativeArray**</span><span class="sxs-lookup"><span data-stu-id="ea44b-131">**IUIAutomation::SafeArrayToRectNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | <span data-ttu-id="ea44b-132">Convertit un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) qui contient des coordonnées de rectangle en tableau de type **Rect**.</span><span class="sxs-lookup"><span data-stu-id="ea44b-132">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) that contains rectangle coordinates to an array of type **RECT**.</span></span> |



 

## <a name="providers"></a><span data-ttu-id="ea44b-133">Fournisseurs</span><span class="sxs-lookup"><span data-stu-id="ea44b-133">Providers</span></span>

<span data-ttu-id="ea44b-134">Un fournisseur doit implémenter un certain nombre de méthodes d’interface appelées par UI Automation pour récupérer des informations à partir du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ea44b-134">A provider must implement a number of interface methods that UI Automation calls to retrieve information from the provider.</span></span> <span data-ttu-id="ea44b-135">De nombreuses fois, ces informations se composent d’un tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="ea44b-135">Many times, this information consists of an array of values.</span></span> <span data-ttu-id="ea44b-136">Pour retourner un tableau à UI Automation, le fournisseur doit empaqueter le tableau dans une structure [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) .</span><span class="sxs-lookup"><span data-stu-id="ea44b-136">To return an array to UI Automation, the provider must pack the array into a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) structure.</span></span> <span data-ttu-id="ea44b-137">Les éléments de tableau doivent être du type de données attendu et doivent apparaître dans l’ordre attendu.</span><span class="sxs-lookup"><span data-stu-id="ea44b-137">The array elements must be of the expected data type, and must appear in the expected order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea44b-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea44b-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ea44b-139">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ea44b-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ea44b-140">Vue d'ensemble des propriétés UI Automation</span><span class="sxs-lookup"><span data-stu-id="ea44b-140">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="ea44b-141">Notions de base d’UI Automation</span><span class="sxs-lookup"><span data-stu-id="ea44b-141">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 