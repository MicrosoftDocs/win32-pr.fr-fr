---
title: Propriétés et méthodes de sélection et de focus
description: À l’instar de nombreux éléments des applications exécutées sur les systèmes d’exploitation Microsoft Windows, les objets accessibles sélectionnent et reçoivent le focus clavier. Ces attributs permettent aux utilisateurs d’interagir avec des éléments d’application, de modifier des valeurs et de les manipuler.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5eee361707ec4876245eef5b0eb352f8dfd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728429"
---
# <a name="selection-and-focus-properties-and-methods"></a><span data-ttu-id="9a586-104">Propriétés et méthodes de sélection et de focus</span><span class="sxs-lookup"><span data-stu-id="9a586-104">Selection and Focus Properties and Methods</span></span>

<span data-ttu-id="9a586-105">À l’instar de nombreux éléments des applications exécutées sur les systèmes d’exploitation Microsoft Windows, les objets accessibles *sélectionnent* et reçoivent *le focus* clavier.</span><span class="sxs-lookup"><span data-stu-id="9a586-105">Like many elements in applications running on Microsoft Windows operating systems, accessible objects *select* and receive keyboard *focus*.</span></span> <span data-ttu-id="9a586-106">Ces attributs permettent aux utilisateurs d’interagir avec des éléments d’application, de modifier des valeurs et de les manipuler.</span><span class="sxs-lookup"><span data-stu-id="9a586-106">These attributes enable users to interact with application elements, change values, and otherwise manipulate them.</span></span>

<span data-ttu-id="9a586-107">Il existe quelques différences clés entre la sélection des objets et le focus de l’objet :</span><span class="sxs-lookup"><span data-stu-id="9a586-107">There are some key differences between object selection and object focus:</span></span>

-   <span data-ttu-id="9a586-108">Un objet ayant le focus est l’objet de l’ensemble du système d’exploitation qui reçoit l’entrée au clavier.</span><span class="sxs-lookup"><span data-stu-id="9a586-108">A focused object is the one object in the entire operating system that receives keyboard input.</span></span> <span data-ttu-id="9a586-109">L’objet avec le focus clavier est soit la fenêtre active, soit un objet enfant de la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="9a586-109">The object with the keyboard focus is either the active window or a child object of the active window.</span></span>
-   <span data-ttu-id="9a586-110">Un objet sélectionné est marqué pour participer à un type d’opération de groupe.</span><span class="sxs-lookup"><span data-stu-id="9a586-110">A selected object is marked to participate in some type of group operation.</span></span>

<span data-ttu-id="9a586-111">Par exemple, un utilisateur peut sélectionner plusieurs éléments dans un contrôle List-View, mais le focus est donné à un seul objet dans le système à la fois.</span><span class="sxs-lookup"><span data-stu-id="9a586-111">For example, a user can select several items in a list-view control, but the focus is given only to one object in the system at a time.</span></span> <span data-ttu-id="9a586-112">Notez que les éléments ayant le focus proviennent d’une sélection d’éléments.</span><span class="sxs-lookup"><span data-stu-id="9a586-112">Note that focused items are from a selection of items.</span></span>

<span data-ttu-id="9a586-113">Les clients déterminent si un objet ou un élément enfant accessible particulier a le focus en appelant [**IAccessible :: obtenir \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span><span class="sxs-lookup"><span data-stu-id="9a586-113">Clients determine whether a particular accessible object or child element has the focus by calling [**IAccessible::get\_accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span></span> <span data-ttu-id="9a586-114">Les clients déterminent si un objet est sélectionné, ou les enfants d’un objet accessible, en appelant [**IAccessible :: obtenir \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span><span class="sxs-lookup"><span data-stu-id="9a586-114">Clients determine whether an object is selected, or which children within an accessible object are selected, by calling [**IAccessible::get\_accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span></span> <span data-ttu-id="9a586-115">Pour les objets tels que les contrôles de vue de liste dans lesquels plusieurs enfants sont sélectionnés, l’objet parent doit prendre en charge l’interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) , qui permet aux clients d’énumérer les enfants sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="9a586-115">For objects such as list-view controls in which more than one child is selected, the parent object must support the [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface, which allows clients to enumerate the selected children.</span></span>

## <a name="events-triggered-in-menus"></a><span data-ttu-id="9a586-116">Événements déclenchés dans les menus</span><span class="sxs-lookup"><span data-stu-id="9a586-116">Events Triggered in Menus</span></span>

<span data-ttu-id="9a586-117">Microsoft Active Accessibility expose les menus standard créés avec les API de menu et les fichiers de ressources de Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="9a586-117">Microsoft Active Accessibility exposes standard menus created with the Microsoft Win32 menu APIs and resource files.</span></span> <span data-ttu-id="9a586-118">Pour être cohérente avec les menus standard, les serveurs avec des menus personnalisés déclenchent [**\_ \_ le focus**](event-constants.md)de l’objet d’événement, et non l’objet d’événement, lorsqu’un utilisateur met en surbrillance un élément de menu. [**\_ \_**](event-constants.md)</span><span class="sxs-lookup"><span data-stu-id="9a586-118">To be consistent with standard menus, servers with custom menus trigger [**EVENT\_OBJECT\_FOCUS**](event-constants.md), not [**EVENT\_OBJECT\_SELECTION**](event-constants.md), when a user highlights a menu item.</span></span>

> [!Note]  
> <span data-ttu-id="9a586-119">Microsoft Active Accessibility ne prend pas en charge la sélection du texte contenu dans les contrôles Edit et Rich Edit, car le texte est exposé sous la forme d’une chaîne unique dans la propriété [**value**](value-property.md) de ces contrôles.</span><span class="sxs-lookup"><span data-stu-id="9a586-119">Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a single string in the [**Value**](value-property.md) property for these controls.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="9a586-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9a586-120">In this section</span></span>

-   [<span data-ttu-id="9a586-121">Sélection des objets enfants</span><span class="sxs-lookup"><span data-stu-id="9a586-121">Selecting Child Objects</span></span>](selecting-child-objects.md)

 

 