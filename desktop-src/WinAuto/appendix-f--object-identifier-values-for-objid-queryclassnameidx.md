---
title: Annexe F valeurs de l’identificateur d’objet pour OBJID_QUERYCLASSNAMEIDX
description: Lorsque OLEACC envoie un \_ message WM GETOBJECT avec le paramètre lParam défini sur OBJIDQUERYCLASSNAMEIDX, un grand nombre d’utilisateurs standard ou de contrôles communs (COMCTL) retournent l’une des valeurs suivantes.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106543415"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a><span data-ttu-id="adf70-103">Annexe F : valeurs de l’identificateur d’objet pour OBJID \_ QUERYCLASSNAMEIDX</span><span class="sxs-lookup"><span data-stu-id="adf70-103">Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX</span></span>

<span data-ttu-id="adf70-104">Lorsque OLEACC envoie un message [**WM \_ GETOBJECT**](wm-getobject.md) avec le paramètre *lParam* défini sur OBJIDQUERYCLASSNAMEIDX, un grand nombre d’utilisateurs standard ou de contrôles communs (COMCTL) retournent l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="adf70-104">When OLEACC sends a [**WM\_GETOBJECT**](wm-getobject.md) message with the *lParam* parameter set to OBJIDQUERYCLASSNAMEIDX, many standard USER or common controls (COMCTL) return one of the following values.</span></span>



| <span data-ttu-id="adf70-105">UTILISATEUR ou contrôle commun</span><span class="sxs-lookup"><span data-stu-id="adf70-105">USER or common control</span></span> | <span data-ttu-id="adf70-106">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="adf70-106">Return value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="adf70-107">ListBox</span><span class="sxs-lookup"><span data-stu-id="adf70-107">Listbox</span></span>                | <span data-ttu-id="adf70-108">65536 + 0</span><span class="sxs-lookup"><span data-stu-id="adf70-108">65536+0</span></span>      |
| <span data-ttu-id="adf70-109">Bouton</span><span class="sxs-lookup"><span data-stu-id="adf70-109">Button</span></span>                 | <span data-ttu-id="adf70-110">65536 + 2</span><span class="sxs-lookup"><span data-stu-id="adf70-110">65536+2</span></span>      |
| <span data-ttu-id="adf70-111">statique</span><span class="sxs-lookup"><span data-stu-id="adf70-111">Static</span></span>                 | <span data-ttu-id="adf70-112">65536 + 3</span><span class="sxs-lookup"><span data-stu-id="adf70-112">65536+3</span></span>      |
| <span data-ttu-id="adf70-113">Modifier</span><span class="sxs-lookup"><span data-stu-id="adf70-113">Edit</span></span>                   | <span data-ttu-id="adf70-114">65536 + 4</span><span class="sxs-lookup"><span data-stu-id="adf70-114">65536+4</span></span>      |
| <span data-ttu-id="adf70-115">Combobox</span><span class="sxs-lookup"><span data-stu-id="adf70-115">Combobox</span></span>               | <span data-ttu-id="adf70-116">65536 + 5</span><span class="sxs-lookup"><span data-stu-id="adf70-116">65536+5</span></span>      |
| <span data-ttu-id="adf70-117">Scrollbar</span><span class="sxs-lookup"><span data-stu-id="adf70-117">Scrollbar</span></span>              | <span data-ttu-id="adf70-118">65536 + 10</span><span class="sxs-lookup"><span data-stu-id="adf70-118">65536+10</span></span>     |
| <span data-ttu-id="adf70-119">Statut</span><span class="sxs-lookup"><span data-stu-id="adf70-119">Status</span></span>                 | <span data-ttu-id="adf70-120">65536 + 11</span><span class="sxs-lookup"><span data-stu-id="adf70-120">65536+11</span></span>     |
| <span data-ttu-id="adf70-121">Barre d’outils</span><span class="sxs-lookup"><span data-stu-id="adf70-121">Toolbar</span></span>                | <span data-ttu-id="adf70-122">65536 + 12</span><span class="sxs-lookup"><span data-stu-id="adf70-122">65536+12</span></span>     |
| <span data-ttu-id="adf70-123">Progress</span><span class="sxs-lookup"><span data-stu-id="adf70-123">Progress</span></span>               | <span data-ttu-id="adf70-124">65536 + 13</span><span class="sxs-lookup"><span data-stu-id="adf70-124">65536+13</span></span>     |
| <span data-ttu-id="adf70-125">Immobile</span><span class="sxs-lookup"><span data-stu-id="adf70-125">Animate</span></span>                | <span data-ttu-id="adf70-126">65536 + 14</span><span class="sxs-lookup"><span data-stu-id="adf70-126">65536+14</span></span>     |
| <span data-ttu-id="adf70-127">Onglet</span><span class="sxs-lookup"><span data-stu-id="adf70-127">Tab</span></span>                    | <span data-ttu-id="adf70-128">65536 + 15</span><span class="sxs-lookup"><span data-stu-id="adf70-128">65536+15</span></span>     |
| <span data-ttu-id="adf70-129">Touche d’accès rapide</span><span class="sxs-lookup"><span data-stu-id="adf70-129">Hotkey</span></span>                 | <span data-ttu-id="adf70-130">65536 + 16</span><span class="sxs-lookup"><span data-stu-id="adf70-130">65536+16</span></span>     |
| <span data-ttu-id="adf70-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="adf70-131">Header</span></span>                 | <span data-ttu-id="adf70-132">65536 + 17</span><span class="sxs-lookup"><span data-stu-id="adf70-132">65536+17</span></span>     |
| <span data-ttu-id="adf70-133">TrackBar</span><span class="sxs-lookup"><span data-stu-id="adf70-133">Trackbar</span></span>               | <span data-ttu-id="adf70-134">65536 + 18</span><span class="sxs-lookup"><span data-stu-id="adf70-134">65536+18</span></span>     |
| <span data-ttu-id="adf70-135">Liste</span><span class="sxs-lookup"><span data-stu-id="adf70-135">Listview</span></span>               | <span data-ttu-id="adf70-136">65536 + 19</span><span class="sxs-lookup"><span data-stu-id="adf70-136">65536+19</span></span>     |
| <span data-ttu-id="adf70-137">UpDown</span><span class="sxs-lookup"><span data-stu-id="adf70-137">Updown</span></span>                 | <span data-ttu-id="adf70-138">65536 + 22</span><span class="sxs-lookup"><span data-stu-id="adf70-138">65536+22</span></span>     |
| <span data-ttu-id="adf70-139">Info-bulles</span><span class="sxs-lookup"><span data-stu-id="adf70-139">ToolTips</span></span>               | <span data-ttu-id="adf70-140">65536 + 24</span><span class="sxs-lookup"><span data-stu-id="adf70-140">65536+24</span></span>     |
| <span data-ttu-id="adf70-141">TreeView</span><span class="sxs-lookup"><span data-stu-id="adf70-141">Treeview</span></span>               | <span data-ttu-id="adf70-142">65536 + 25</span><span class="sxs-lookup"><span data-stu-id="adf70-142">65536+25</span></span>     |
| <span data-ttu-id="adf70-143">RichEdit</span><span class="sxs-lookup"><span data-stu-id="adf70-143">RichEdit</span></span>               | <span data-ttu-id="adf70-144">65536 + 28</span><span class="sxs-lookup"><span data-stu-id="adf70-144">65536+28</span></span>     |



 

<span data-ttu-id="adf70-145">Seuls les contrôles communs utilisateur et Windows (COMCTL) retournent l’une des valeurs de la table.</span><span class="sxs-lookup"><span data-stu-id="adf70-145">Only USER and Windows common controls (COMCTL) will return one of the values from the table.</span></span> <span data-ttu-id="adf70-146">Si une fenêtre retourne 0 en réponse à ce message, la fenêtre peut être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="adf70-146">If a window returns 0 in response to this message, the window may be one of the following:</span></span>

-   <span data-ttu-id="adf70-147">Un contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="adf70-147">A custom control</span></span>
-   <span data-ttu-id="adf70-148">Contrôle autre que l’un des contrôles du tableau précédent</span><span class="sxs-lookup"><span data-stu-id="adf70-148">A control other than one of the controls in the previous table</span></span>
-   <span data-ttu-id="adf70-149">Une ancienne version d’un contrôle système qui ne reconnaît pas le message [**WM de \_ GETOBJECT**](wm-getobject.md)</span><span class="sxs-lookup"><span data-stu-id="adf70-149">An old version of a system control that does not recognize the [**WM\_GETOBJECT**](wm-getobject.md) message</span></span>

<span data-ttu-id="adf70-150">Si une fenêtre retourne la valeur 0, les clients devront peut-être utiliser [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) ou [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname).</span><span class="sxs-lookup"><span data-stu-id="adf70-150">If a window returns 0, clients may need to use [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) or [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname).</span></span> <span data-ttu-id="adf70-151">Vous pouvez utiliser ces fonctions pour déterminer le type de contrôle en fonction du nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="adf70-151">You can use these functions to determine the type of control based on class name.</span></span>

<span data-ttu-id="adf70-152">En général, les clients peuvent utiliser les informations fournies par OLEACC.</span><span class="sxs-lookup"><span data-stu-id="adf70-152">In general, clients can use the information provided by OLEACC.</span></span>

 

 