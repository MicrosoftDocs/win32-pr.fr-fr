---
title: Calendar, contrôle (référence des éléments d’interface utilisateur MSAA)
description: Les contrôles Calendar offrent un moyen simple et intuitif pour un utilisateur de sélectionner une date à partir d’une interface familière.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839665"
---
# <a name="calendar-control-msaa-ui-element-reference"></a><span data-ttu-id="4138e-103">Calendar, contrôle (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="4138e-103">Calendar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="4138e-104">Cette rubrique décrit les objets de **contrôle de calendrier** à des fins de référence d’élément d’interface utilisateur MSAA.</span><span class="sxs-lookup"><span data-stu-id="4138e-104">This topic describes **Calendar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="4138e-105">La procédure de création d’objets de **contrôle Calendar** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici.</span><span class="sxs-lookup"><span data-stu-id="4138e-105">How to create **Calendar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="4138e-106">Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="4138e-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="4138e-107">Les contrôles Calendar offrent un moyen simple et intuitif pour un utilisateur de sélectionner une date à partir d’une interface familière.</span><span class="sxs-lookup"><span data-stu-id="4138e-107">Calendar controls provide a simple and intuitive way for a user to select a date from a familiar interface.</span></span>

<span data-ttu-id="4138e-108">Le nom de la classe de fenêtre pour un contrôle Month Calendar est la \_ classe calendrier monthcal, qui est définie comme « SysMonthCal32 » dans commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="4138e-108">The window class name for a month calendar control is MONTHCAL\_CLASS, which is defined as "SysMonthCal32" in Commctrl.h.</span></span> <span data-ttu-id="4138e-109">Les informations contenues dans cette rubrique s’appliquent au contrôle Month Calendar dans la version 5 de commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="4138e-109">Information in this topic applies to the month calendar control in version 5 of Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="4138e-110">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="4138e-110">IAccessible Methods</span></span>

<span data-ttu-id="4138e-111">Les contrôles Calendar prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="4138e-111">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="4138e-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="4138e-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="4138e-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="4138e-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="4138e-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="4138e-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="4138e-115">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="4138e-115">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="4138e-116">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="4138e-116">IAccessible Properties</span></span>

<span data-ttu-id="4138e-117">Les contrôles Calendar prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="4138e-117">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="4138e-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="4138e-118">Property</span></span>                                                                 | <span data-ttu-id="4138e-119">Commentaires</span><span class="sxs-lookup"><span data-stu-id="4138e-119">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4138e-120">**Obtient \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="4138e-120">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="4138e-121">La propriété **ChildCount** est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="4138e-121">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="4138e-122">**Obtient \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="4138e-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="4138e-123">**Obtient \_ accName**</span><span class="sxs-lookup"><span data-stu-id="4138e-123">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="4138e-124">La propriété **Name** est obtenue à partir du contrôle texte statique qui étiquette le contrôle calendrier.</span><span class="sxs-lookup"><span data-stu-id="4138e-124">The **Name** property is obtained from the static text control that labels the calendar control.</span></span> <span data-ttu-id="4138e-125">Lors de la création de contrôles, les développeurs de serveur doivent s’assurer qu’un contrôle de texte statique précède immédiatement le contrôle qu’il étiquette dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="4138e-125">When creating controls, server developers must ensure that a static text control immediately precedes the control that it labels within the tab order.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="4138e-126">**Obtient \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="4138e-126">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="4138e-127">La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.</span><span class="sxs-lookup"><span data-stu-id="4138e-127">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="4138e-128">**Obtient \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="4138e-128">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="4138e-129">La propriété de **rôle** est [**client de \_ système \_ de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4138e-129">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="4138e-130">**Obtient \_ accState**</span><span class="sxs-lookup"><span data-stu-id="4138e-130">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="4138e-131">La propriété **State** est une combinaison d’une ou plusieurs des valeurs suivantes [](object-state-constants.md)[**état système \_ état \_**](object-state-constants.md) indisponible système d’état \| [**\_ \_ indisponible**](object-state-constants.md) système d’état \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ focus**](object-state-constants.md) système</span><span class="sxs-lookup"><span data-stu-id="4138e-131">The **State** property is a combination of one or more of the following [values](object-state-constants.md)[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="4138e-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4138e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4138e-133">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="4138e-133">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





