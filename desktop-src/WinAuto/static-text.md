---
title: Texte statique (référence des éléments d’interface utilisateur MSAA)
description: Les contrôles de texte statique offrent un moyen pratique d’afficher du texte dans les boîtes de dialogue et d’autres fenêtres. Les contrôles de texte statique servent souvent d’étiquettes pour d’autres contrôles.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840742"
---
# <a name="static-text-msaa-ui-element-reference"></a><span data-ttu-id="95328-104">Texte statique (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="95328-104">Static Text (MSAA UI Element Reference)</span></span>

<span data-ttu-id="95328-105">Les contrôles de texte statique offrent un moyen pratique d’afficher du texte dans les boîtes de dialogue et d’autres fenêtres.</span><span class="sxs-lookup"><span data-stu-id="95328-105">Static text controls provide a convenient way to display text on dialog boxes and other windows.</span></span> <span data-ttu-id="95328-106">Les contrôles de texte statique servent souvent d’étiquettes pour d’autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="95328-106">Static text controls often serve as labels for other controls.</span></span>

<span data-ttu-id="95328-107">Le nom de la classe de fenêtre pour un contrôle de texte statique est « STATIC ».</span><span class="sxs-lookup"><span data-stu-id="95328-107">The window class name for a static text control is "STATIC".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="95328-108">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="95328-108">IAccessible Methods</span></span>

<span data-ttu-id="95328-109">Les contrôles de texte statiques prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="95328-109">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="95328-110">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="95328-110">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="95328-111">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="95328-111">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="95328-112">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="95328-112">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="95328-113">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="95328-113">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="95328-114">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="95328-114">IAccessible Properties</span></span>

<span data-ttu-id="95328-115">Les contrôles de texte statiques prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="95328-115">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="95328-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="95328-116">Property</span></span>                                                                             | <span data-ttu-id="95328-117">Commentaires</span><span class="sxs-lookup"><span data-stu-id="95328-117">Comments</span></span>                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95328-118">**Obtient \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="95328-118">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="95328-119">**Obtient \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="95328-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="95328-120">La propriété **ChildCount** est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="95328-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="95328-121">**Obtient \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="95328-121">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="95328-122">**Obtient \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="95328-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="95328-123">**Obtient \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="95328-123">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="95328-124">**Obtient \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="95328-124">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="95328-125">**Obtient \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="95328-125">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="95328-126">La propriété **KeyboardShortcut** est la clé d’accès, qui est le caractère souligné dans le texte qui active le contrôle associé au texte statique.</span><span class="sxs-lookup"><span data-stu-id="95328-126">The **KeyboardShortcut** property is the access key, which is the underlined character in the text that activates the control associated with the static text.</span></span> <span data-ttu-id="95328-127">La chaîne retournée contient le caractère clé d’accès ajouté à la chaîne « ALT + ».</span><span class="sxs-lookup"><span data-stu-id="95328-127">The returned string contains the access key character appended to the string "Alt+".</span></span>                                           |
| [<span data-ttu-id="95328-128">**Obtient \_ accName**</span><span class="sxs-lookup"><span data-stu-id="95328-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="95328-129">La propriété **Name** est la même que le texte du contrôle de texte statique.</span><span class="sxs-lookup"><span data-stu-id="95328-129">The **Name** property is the same as the text in the static text control.</span></span>                                                                                                                                                                                                                     |
| [<span data-ttu-id="95328-130">**Obtient \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="95328-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="95328-131">La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.</span><span class="sxs-lookup"><span data-stu-id="95328-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                   |
| [<span data-ttu-id="95328-132">**Obtient \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="95328-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="95328-133">La propriété **role** est le [**système de rôle \_ \_ STATICTEXT**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="95328-133">The **Role** property is [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md).</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="95328-134">**Obtient \_ accState**</span><span class="sxs-lookup"><span data-stu-id="95328-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="95328-135">La propriété **State** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : système d’état [**\_ \_ ReadOnly**](object-state-constants.md) système d’état \| [**\_ \_ invisible**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="95328-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) \| [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="95328-136">Notes</span><span class="sxs-lookup"><span data-stu-id="95328-136">Notes</span></span>

-   <span data-ttu-id="95328-137">La méthode [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) retourne DISP \_ E \_ MEMBERNOTFOUND quand elle est appelée avec [**SELFLAG \_ TAKEFOCUS**](selflag.md) sur un objet texte statique.</span><span class="sxs-lookup"><span data-stu-id="95328-137">The [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method returns DISP\_E\_MEMBERNOTFOUND when it is called with [**SELFLAG\_TAKEFOCUS**](selflag.md) on a static text object.</span></span>
-   <span data-ttu-id="95328-138">Les contrôles statiques avec le \_ style d’icône SS retournent des données non valides dans la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="95328-138">Static controls with the SS\_ICON style return invalid data in the **Name** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95328-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95328-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95328-140">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="95328-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





