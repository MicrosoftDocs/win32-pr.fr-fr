---
title: Caret (référence des éléments de l’interface utilisateur MSAA)
description: Le signe insertion est une ligne, un bloc ou un bitmap clignotant dans la zone cliente d’une fenêtre ou dans un contrôle qui accepte les entrées au clavier.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103841830"
---
# <a name="caret-msaa-ui-element-reference"></a><span data-ttu-id="6ddd8-103">Caret (référence des éléments de l’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="6ddd8-103">Caret (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="6ddd8-104">Cette rubrique décrit les signes de référence des éléments d’interface utilisateur MSAA.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-104">This topic describes carets for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="6ddd8-105">L’utilisation des signes d’insertion dans différentes infrastructures d’interface utilisateur n’est pas décrite ici.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-105">How to use carets in various UI frameworks is not described here.</span></span> <span data-ttu-id="6ddd8-106">Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="6ddd8-107">Le signe insertion est une ligne, un bloc ou un bitmap clignotant dans la zone cliente d’une fenêtre ou dans un contrôle qui accepte les entrées au clavier.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-107">The caret is a flashing line, block, or bitmap in the client area of a window or in a control that accepts keyboard input.</span></span> <span data-ttu-id="6ddd8-108">Elle indique l’endroit où le texte ou les graphiques sont insérés.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-108">It indicates the place at which text or graphics are inserted.</span></span> <span data-ttu-id="6ddd8-109">Étant donné qu’une seule fenêtre à la fois a le focus clavier, il n’y a qu’un seul signe insertion dans le système.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-109">Because only one window at a time has the keyboard focus, there is only one caret in the system.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="6ddd8-110">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="6ddd8-110">IAccessible Methods</span></span>

<span data-ttu-id="6ddd8-111">Le signe insertion prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ddd8-111">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="6ddd8-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="6ddd8-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="6ddd8-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="6ddd8-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="6ddd8-114">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="6ddd8-114">IAccessible Properties</span></span>

<span data-ttu-id="6ddd8-115">Le signe insertion prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ddd8-115">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ddd8-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="6ddd8-116">Property</span></span></th>
<th><span data-ttu-id="6ddd8-117">Commentaires</span><span class="sxs-lookup"><span data-stu-id="6ddd8-117">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ddd8-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ddd8-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="6ddd8-119">La propriété <strong>ChildCount</strong> est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-119">The <strong>ChildCount</strong> property is zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ddd8-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ddd8-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span></span></td>
<td><span data-ttu-id="6ddd8-121">La propriété <strong>Name</strong> est &quot; Edit &quot; .</span><span class="sxs-lookup"><span data-stu-id="6ddd8-121">The <strong>Name</strong> property is &quot;Edit&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ddd8-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ddd8-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span></span></td>
<td><span data-ttu-id="6ddd8-123">La propriété de <strong>rôle</strong> est <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-123">The <strong>Role</strong> property is <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ddd8-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ddd8-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span></span></td>
<td><span data-ttu-id="6ddd8-125">Les valeurs possibles pour la propriété <strong>State</strong> sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ddd8-125">Possible values for the <strong>State</strong> property include:</span></span>
<ul>
<li><span data-ttu-id="6ddd8-126">Zéro, ce qui signifie que le signe insertion est visible</span><span class="sxs-lookup"><span data-stu-id="6ddd8-126">Zero, which means the caret is visible</span></span></li>
<li><span data-ttu-id="6ddd8-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span><span class="sxs-lookup"><span data-stu-id="6ddd8-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="6ddd8-128">Notes</span><span class="sxs-lookup"><span data-stu-id="6ddd8-128">Notes</span></span>

-   <span data-ttu-id="6ddd8-129">Contrairement à d’autres éléments d’interface utilisateur, l’objet caret n’a pas de handle de fenêtre associé.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-129">Unlike other UI elements, the caret object does not have an associated window handle.</span></span> <span data-ttu-id="6ddd8-130">Pour obtenir l’accès à l’objet Caret, les clients doivent définir un [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) et attendre que l’objet caret génère des événements.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-130">To obtain access to the caret object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the caret object to generate events.</span></span>
-   <span data-ttu-id="6ddd8-131">L’objet caret dans le contrôle RichEdit fourni par Riched20.dll (qui est utilisé dans les éditeurs de texte tels que Microsoft WordPad dans Windows 98) n’envoie pas de [winEvents](winevents-infrastructure.md) lorsque sa position est modifiée pendant la sélection de texte.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-131">The caret object in the rich edit control provided by Riched20.dll (which is used in text editors such as Microsoft WordPad in Windows 98) does not send any [WinEvents](winevents-infrastructure.md) when its position is changed during text selection.</span></span> <span data-ttu-id="6ddd8-132">Quand les utilisateurs appuient sur la touche Maj et les touches de direction pour sélectionner du texte, l’objet caret ne déclenche pas l' [**objet d’événement \_ \_ LOCATIONCHANGE**](event-constants.md) WinEvent.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-132">When users press SHIFT and arrow keys to select text, the caret object does not trigger the [**EVENT\_OBJECT\_LOCATIONCHANGE**](event-constants.md) WinEvent.</span></span> <span data-ttu-id="6ddd8-133">De même, lorsque la sélection est définie par programme par le biais de messages Rich Edit, l’objet caret n’envoie aucun événement pour indiquer sa nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-133">Similarly, when the selection is set programmatically through rich edit messages, the caret object does not send any events to indicate its new position.</span></span>

    <span data-ttu-id="6ddd8-134">Toutes les applications qui utilisent Riched20.dll présentent ce problème.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-134">All applications that use Riched20.dll exhibit this problem.</span></span> <span data-ttu-id="6ddd8-135">Les applications qui utilisent des versions antérieures du contrôle RichEdit envoient correctement les événements en fonction de la sélection.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-135">Applications using earlier versions of the rich edit control correctly send events based on the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ddd8-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ddd8-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ddd8-137">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="6ddd8-137">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




