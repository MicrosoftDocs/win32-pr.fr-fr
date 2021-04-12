---
title: Utilisation de l’annotation de mappage de valeur
description: Pour obtenir un exemple de code, consultez exemple d’annotation de mappage de valeur.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382011"
---
# <a name="using-value-map-annotation"></a><span data-ttu-id="e2a30-103">Utilisation de l’annotation de mappage de valeur</span><span class="sxs-lookup"><span data-stu-id="e2a30-103">Using Value Map Annotation</span></span>

<span data-ttu-id="e2a30-104">**Pour créer une carte de valeur**</span><span class="sxs-lookup"><span data-stu-id="e2a30-104">**To create a value map**</span></span>

1.  <span data-ttu-id="e2a30-105">**Créez une chaîne de mappage.**</span><span class="sxs-lookup"><span data-stu-id="e2a30-105">**Create a mapping string.**</span></span>

    <span data-ttu-id="e2a30-106">Une chaîne de mappage est une liste de valeurs numériques d’un contrôle correspondant à une chaîne explicite en Unicode.</span><span class="sxs-lookup"><span data-stu-id="e2a30-106">A mapping string is a list of a control's numeric values corresponding to a human-readable string in Unicode.</span></span> <span data-ttu-id="e2a30-107">Il commence par « A : » suivi d’un nombre qui indique le type d’index utilisé.</span><span class="sxs-lookup"><span data-stu-id="e2a30-107">It starts with "A:" followed by a number that indicates the type of index used.</span></span> <span data-ttu-id="e2a30-108">Seuls les index d’images sont pris en charge ; par conséquent, le type d’index est toujours 0.</span><span class="sxs-lookup"><span data-stu-id="e2a30-108">Only image indexes are supported; therefore the index type is always 0.</span></span>

    <span data-ttu-id="e2a30-109">La chaîne est suivie par les paires : index : résultat.</span><span class="sxs-lookup"><span data-stu-id="e2a30-109">The string is followed by :index:result pairs.</span></span> <span data-ttu-id="e2a30-110">L’index est un nombre qui représente un index d’image pour une List-View ou une vue d’arborescence, ou la valeur d’un contrôle Slider.</span><span class="sxs-lookup"><span data-stu-id="e2a30-110">The "index" is a number representing an image index for a List-View or Tree-View, or the value for a slider control.</span></span>

    <span data-ttu-id="e2a30-111">La valeur obtenue est un nombre obtenu lorsque vous mappez la propriété de rôle ou d’État pour un contrôle d’affichage de liste ou d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="e2a30-111">The resulting value is a number obtained when you map the Role or State property for a list view or tree view control.</span></span> <span data-ttu-id="e2a30-112">Ces nombres sont exprimés en décimal ou hexadécimal avec un préfixe « 0x ».</span><span class="sxs-lookup"><span data-stu-id="e2a30-112">Such numbers are expressed in decimal or hexadecimal with an "0x" prefix.</span></span>

    <span data-ttu-id="e2a30-113">La chaîne de mappage se termine toujours par un signe deux-points («  : ») final.</span><span class="sxs-lookup"><span data-stu-id="e2a30-113">The mapping string is always terminated with a final colon (":").</span></span>

    <span data-ttu-id="e2a30-114">Voici un exemple de carte d’annotation pour les propriétés d’État et de rôle d’une case à cocher dans un affichage de liste ou un contrôle d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="e2a30-114">The following is an example of an annotation map for the State and Role properties of a check box in a list view or tree view control.</span></span> <span data-ttu-id="e2a30-115">Il y a deux éléments dans la vue qui représentent des cases à cocher, et chacun contient des images correspondant à l’état coché et non vérifié.</span><span class="sxs-lookup"><span data-stu-id="e2a30-115">There are two items in the view that represent check boxes, and each has images corresponding to the checked and unchecked state.</span></span>

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    <span data-ttu-id="e2a30-116">Pour connaître les valeurs de rôle et d’état valides, consultez la section [rôles d’objet](object-roles.md) et [constantes d’état d’objet](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e2a30-116">For valid Role and State values, see [Object Roles](object-roles.md) and [Object State Constants](object-state-constants.md).</span></span>

    <span data-ttu-id="e2a30-117">La valeur d’index peut être négative quand vous mappez des propriétés pour un contrôle Slider.</span><span class="sxs-lookup"><span data-stu-id="e2a30-117">The index value may be negative when you map properties for a slider control.</span></span>

    <span data-ttu-id="e2a30-118">Lorsque vous mappez une propriété de valeur ou de description, le résultat est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="e2a30-118">When you map a Value or Description property, the result is a string.</span></span> <span data-ttu-id="e2a30-119">Les chaînes ne sont pas placées entre guillemets et les deux-points agissent comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="e2a30-119">Strings are not quoted and the colons act as delimiters.</span></span>

    <span data-ttu-id="e2a30-120">Pour plus d’informations, consultez format de la [table des annotations](value-map-annotation.md).</span><span class="sxs-lookup"><span data-stu-id="e2a30-120">For more information, see [Annotation Map Format](value-map-annotation.md).</span></span>

2.  <span data-ttu-id="e2a30-121">**Créez le gestionnaire d’annotations et obtenez un pointeur vers son** interface [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**.**</span><span class="sxs-lookup"><span data-stu-id="e2a30-121">**Create the annotation manager and obtain a pointer to its**[**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**interface.**</span></span>

    <span data-ttu-id="e2a30-122">Voici un exemple de création du gestionnaire d’annotations.</span><span class="sxs-lookup"><span data-stu-id="e2a30-122">The following is an example of how to create the annotation manager.</span></span>

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  <span data-ttu-id="e2a30-123">**Attachez la chaîne de mappage au contrôle.**</span><span class="sxs-lookup"><span data-stu-id="e2a30-123">**Attach the mapping string to the control.**</span></span>

    <span data-ttu-id="e2a30-124">Appelez [**IAccPropServices :: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), en passant le **HWND** du contrôle et un pointeur vers la chaîne de mappage.</span><span class="sxs-lookup"><span data-stu-id="e2a30-124">Call [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), passing the **HWND** of the control and a pointer to the mapping string.</span></span>

    <span data-ttu-id="e2a30-125">Le paramètre *IdProp* aura l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e2a30-125">The *IdProp* parameter will be one of the following.</span></span>

    

    | <span data-ttu-id="e2a30-126">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e2a30-126">Parameter</span></span>                   | <span data-ttu-id="e2a30-127">Utilisé pour</span><span class="sxs-lookup"><span data-stu-id="e2a30-127">Used for</span></span>                                                |
    |-----------------------------|---------------------------------------------------------|
    | <span data-ttu-id="e2a30-128">MSAAPROPID \_ ROLEMAP</span><span class="sxs-lookup"><span data-stu-id="e2a30-128">MSAAPROPID\_ROLEMAP</span></span>         | <span data-ttu-id="e2a30-129">Pour définir une carte de rôle pour les contrôles d’affichage de liste ou d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="e2a30-129">To set a role map for list view or tree view controls.</span></span>  |
    | <span data-ttu-id="e2a30-130">MSAAPROPID \_ STATEMAP</span><span class="sxs-lookup"><span data-stu-id="e2a30-130">MSAAPROPID\_STATEMAP</span></span>        | <span data-ttu-id="e2a30-131">Pour définir une table d’État pour les contrôles d’affichage de liste ou d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="e2a30-131">To set a state map for list view or tree view controls.</span></span> |
    | <span data-ttu-id="e2a30-132">\_DESCRIPTIONMAP de compte propid \_</span><span class="sxs-lookup"><span data-stu-id="e2a30-132">PROPID\_ACC\_DESCRIPTIONMAP</span></span> | <span data-ttu-id="e2a30-133">Pour définir une carte de description pour la vue liste ou les arborescences.</span><span class="sxs-lookup"><span data-stu-id="e2a30-133">To set a description map for list view or tree views.</span></span>   |
    | <span data-ttu-id="e2a30-134">MSAAPROPID \_ VALUEMAP</span><span class="sxs-lookup"><span data-stu-id="e2a30-134">MSAAPROPID\_VALUEMAP</span></span>        | <span data-ttu-id="e2a30-135">Pour définir une carte de valeur sur les contrôles Slider.</span><span class="sxs-lookup"><span data-stu-id="e2a30-135">To set a value map on slider controls.</span></span>                  |

    

     

4.  <span data-ttu-id="e2a30-136">**Nettoyage.**</span><span class="sxs-lookup"><span data-stu-id="e2a30-136">**Clean up.**</span></span>

    <span data-ttu-id="e2a30-137">Avant de détruire les contrôles annotés de mappage de valeur (par exemple, lors de la gestion de [WM \_ Destroy](../winmsg/wm-destroy.md)), vous devez effacer les propriétés précédemment inscrites et libérer le gestionnaire d’annotations.</span><span class="sxs-lookup"><span data-stu-id="e2a30-137">Before you destroy any value map annotated controls (for example, when handling [WM\_DESTROY](../winmsg/wm-destroy.md)), you must clear previously registered properties and release the annotation manager.</span></span>

    <span data-ttu-id="e2a30-138">Pour ce faire, appelez [**IAccPropServices :: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) si nécessaire, puis libérez votre pointeur vers [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span><span class="sxs-lookup"><span data-stu-id="e2a30-138">To do this, call [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) as appropriate and release your pointer to [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span></span>

<span data-ttu-id="e2a30-139">Pour obtenir un exemple de code, consultez [exemple d’annotation de mappage de valeur](value-map-annotation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e2a30-139">For sample code, see [Value Map Annotation Sample](value-map-annotation-sample.md).</span></span>

 

 