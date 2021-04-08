---
title: Utilisation des sous-classes Theme
description: Les classes de thème qui représentent des contrôles tels que ComboBox, Edit, ExplorerBar, rebar, TAB et Toolbar peuvent être sous-classées afin de fournir des variations de thème pour ce contrôle particulier.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672898"
---
# <a name="using-theme-subclasses"></a><span data-ttu-id="37693-103">Utilisation des sous-classes Theme</span><span class="sxs-lookup"><span data-stu-id="37693-103">Using Theme Subclasses</span></span>

<span data-ttu-id="37693-104">Les classes de thème qui représentent des contrôles tels que ComboBox, Edit, ExplorerBar, rebar, TAB et Toolbar peuvent être sous-classées afin de fournir des variations de thème pour ce contrôle particulier.</span><span class="sxs-lookup"><span data-stu-id="37693-104">Theme classes that represent controls such as ComboBox, Edit, ExplorerBar, Rebar, Tab, and Toolbar can be subclassed in order to provide theme variations for that particular control.</span></span> <span data-ttu-id="37693-105">Par exemple, la classe **Button** est sous-classée comme afin `Start::Button` de permettre le contrôle du thème appliqué au bouton **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="37693-105">For example, the **Button** class is subclassed as `Start::Button` in order to provide control over the theme applied to the **Start** button.</span></span>

> [!Note]  
> <span data-ttu-id="37693-106">Soyez prudent lorsque vous créez des sous-classes comme celles présentées dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="37693-106">Use caution when you create subclasses like those that are discussed in this topic.</span></span> <span data-ttu-id="37693-107">Étant donné que les sous-classes peuvent être modifiées ou non disponibles dans les versions ultérieures de Windows, nous vous déconseillons de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="37693-107">Because subclasses might be altered or unavailable in subsequent versions of Windows, you are discouraged from using them.</span></span>

 

## <a name="two-ways-to-use-a-theme-subclass"></a><span data-ttu-id="37693-108">Deux façons d’utiliser une sous-classe Theme</span><span class="sxs-lookup"><span data-stu-id="37693-108">Two Ways to Use a Theme Subclass</span></span>

<span data-ttu-id="37693-109">Une application peut utiliser un thème sous-classé de l’une des deux manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="37693-109">An application can use a subclassed theme in one of these two ways:</span></span>

-   <span data-ttu-id="37693-110">Elle peut utiliser la fonction [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) avec une chaîne sous la forme du `subclass::class` paramètre *pszClassList* .</span><span class="sxs-lookup"><span data-stu-id="37693-110">It can use the [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) function with a string of the form `subclass::class` in the *pszClassList* parameter.</span></span>
-   <span data-ttu-id="37693-111">Il peut appeler [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) avec le nom de la sous-classe theme dans le paramètre *pszSubAppName* .</span><span class="sxs-lookup"><span data-stu-id="37693-111">It can call [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) with the theme subclass name in the *pszSubAppName* parameter.</span></span>

## <a name="using-theme-messages-that-set-visual-style"></a><span data-ttu-id="37693-112">Utilisation de messages de thème qui définissent le style visuel</span><span class="sxs-lookup"><span data-stu-id="37693-112">Using Theme Messages That Set Visual Style</span></span>

<span data-ttu-id="37693-113">Certains contrôles, tels que Rebar et Toolbar, fournissent des messages spécifiques que vous pouvez envoyer pour indiquer au contrôle d’utiliser une sous-classe de thème.</span><span class="sxs-lookup"><span data-stu-id="37693-113">Certain controls, such as Rebar and Toolbar, provide specific messages that you can send to instruct the control to use a theme subclass.</span></span> <span data-ttu-id="37693-114">Pour ces contrôles, fournissez un pointeur vers une mémoire tampon qui contient le nom de la sous-classe du thème dans le paramètre *lParam* du message.</span><span class="sxs-lookup"><span data-stu-id="37693-114">For those controls, provide a pointer to a buffer that contains the theme subclass name in the *lParam* parameter of the message.</span></span> <span data-ttu-id="37693-115">Utilisez le message générique [**CCM \_ SETWINDOWTHEME**](ccm-setwindowtheme.md) ou utilisez un variant spécifique comme celui indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="37693-115">Use the generic [**CCM\_SETWINDOWTHEME**](ccm-setwindowtheme.md) message, or use a specific variant like those shown in the following table.</span></span>



| <span data-ttu-id="37693-116">Contrôler</span><span class="sxs-lookup"><span data-stu-id="37693-116">Control</span></span>    | <span data-ttu-id="37693-117">Message</span><span class="sxs-lookup"><span data-stu-id="37693-117">Message</span></span>                                             |
|------------|-----------------------------------------------------|
| <span data-ttu-id="37693-118">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="37693-118">Tooltip</span></span>    | [<span data-ttu-id="37693-119">**ATTÉNUATION \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="37693-119">**TTM\_SETWINDOWTHEME**</span></span>](ttm-setwindowtheme.md)   |
| <span data-ttu-id="37693-120">Barre d’outils</span><span class="sxs-lookup"><span data-stu-id="37693-120">Toolbar</span></span>    | [<span data-ttu-id="37693-121">**TO \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="37693-121">**TB\_SETWINDOWTHEME**</span></span>](tb-setwindowtheme.md)     |
| <span data-ttu-id="37693-122">Rebar</span><span class="sxs-lookup"><span data-stu-id="37693-122">Rebar</span></span>      | [<span data-ttu-id="37693-123">**\_SETWINDOWTHEME RB**</span><span class="sxs-lookup"><span data-stu-id="37693-123">**RB\_SETWINDOWTHEME**</span></span>](rb-setwindowtheme.md)     |
| <span data-ttu-id="37693-124">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="37693-124">ComboBoxEx</span></span> | [<span data-ttu-id="37693-125">**CBEM \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="37693-125">**CBEM\_SETWINDOWTHEME**</span></span>](cbem-setwindowtheme.md) |



 

<span data-ttu-id="37693-126">Le tableau suivant répertorie quelques-unes des sous-classes que Windows Vista définit.</span><span class="sxs-lookup"><span data-stu-id="37693-126">The following table lists some of the subclasses that Windows Vista defines.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37693-127">Classe</span><span class="sxs-lookup"><span data-stu-id="37693-127">Class</span></span></th>
<th><span data-ttu-id="37693-128">Sous-classes</span><span class="sxs-lookup"><span data-stu-id="37693-128">Subclasses</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37693-129">Liste déroulante</span><span class="sxs-lookup"><span data-stu-id="37693-129">ComboBox</span></span></td>
<td><ul>
<li><span data-ttu-id="37693-130">Adresse</span><span class="sxs-lookup"><span data-stu-id="37693-130">Address</span></span></li>
<li><span data-ttu-id="37693-131">AddressComposited</span><span class="sxs-lookup"><span data-stu-id="37693-131">AddressComposited</span></span></li>
<li><span data-ttu-id="37693-132">InactiveAddress</span><span class="sxs-lookup"><span data-stu-id="37693-132">InactiveAddress</span></span></li>
<li><span data-ttu-id="37693-133">InactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="37693-133">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="37693-134">MaxAddress</span><span class="sxs-lookup"><span data-stu-id="37693-134">MaxAddress</span></span></li>
<li><span data-ttu-id="37693-135">MaxAddressComposited</span><span class="sxs-lookup"><span data-stu-id="37693-135">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="37693-136">MaxInactiveAddress</span><span class="sxs-lookup"><span data-stu-id="37693-136">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="37693-137">MaxInactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="37693-137">MaxInactiveAddressComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37693-138">Modifier</span><span class="sxs-lookup"><span data-stu-id="37693-138">Edit</span></span></td>
<td><ul>
<li><span data-ttu-id="37693-139">Adresse</span><span class="sxs-lookup"><span data-stu-id="37693-139">Address</span></span></li>
<li><span data-ttu-id="37693-140">AddressComposited</span><span class="sxs-lookup"><span data-stu-id="37693-140">AddressComposited</span></span></li>
<li><span data-ttu-id="37693-141">InactiveAddress</span><span class="sxs-lookup"><span data-stu-id="37693-141">InactiveAddress</span></span></li>
<li><span data-ttu-id="37693-142">InactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="37693-142">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="37693-143">InactiveSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="37693-143">InactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="37693-144">InactiveSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="37693-144">InactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="37693-145">MaxAddress</span><span class="sxs-lookup"><span data-stu-id="37693-145">MaxAddress</span></span></li>
<li><span data-ttu-id="37693-146">MaxAddressComposited</span><span class="sxs-lookup"><span data-stu-id="37693-146">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="37693-147">MaxInactiveAddress</span><span class="sxs-lookup"><span data-stu-id="37693-147">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="37693-148">MaxInactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="37693-148">MaxInactiveAddressComposited</span></span></li>
<li><span data-ttu-id="37693-149">MaxInactiveSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="37693-149">MaxInactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="37693-150">MaxInactiveSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="37693-150">MaxInactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="37693-151">MaxSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="37693-151">MaxSearchBoxEdit</span></span></li>
<li><span data-ttu-id="37693-152">MaxSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="37693-152">MaxSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="37693-153">SearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="37693-153">SearchBoxEdit</span></span></li>
<li><span data-ttu-id="37693-154">SearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="37693-154">SearchBoxEditComposited</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37693-155">Rebar</span><span class="sxs-lookup"><span data-stu-id="37693-155">Rebar</span></span></td>
<td><ul>
<li><span data-ttu-id="37693-156">BrowserTabBar</span><span class="sxs-lookup"><span data-stu-id="37693-156">BrowserTabBar</span></span></li>
<li><span data-ttu-id="37693-157">InactiveNavbar</span><span class="sxs-lookup"><span data-stu-id="37693-157">InactiveNavbar</span></span></li>
<li><span data-ttu-id="37693-158">InactiveNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="37693-158">InactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="37693-159">MaxInactiveNavbar</span><span class="sxs-lookup"><span data-stu-id="37693-159">MaxInactiveNavbar</span></span></li>
<li><span data-ttu-id="37693-160">MaxInactiveNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="37693-160">MaxInactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="37693-161">MaxNavbar</span><span class="sxs-lookup"><span data-stu-id="37693-161">MaxNavbar</span></span></li>
<li><span data-ttu-id="37693-162">MaxNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="37693-162">MaxNavbarComposited</span></span></li>
<li><span data-ttu-id="37693-163">Barre de navigation</span><span class="sxs-lookup"><span data-stu-id="37693-163">Navbar</span></span></li>
<li><span data-ttu-id="37693-164">NavbarComposited</span><span class="sxs-lookup"><span data-stu-id="37693-164">NavbarComposited</span></span></li>
<li><span data-ttu-id="37693-165">NavbarNonTopmost</span><span class="sxs-lookup"><span data-stu-id="37693-165">NavbarNonTopmost</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37693-166">Onglet</span><span class="sxs-lookup"><span data-stu-id="37693-166">Tab</span></span></td>
<td><ul>
<li><span data-ttu-id="37693-167">BrowserTab</span><span class="sxs-lookup"><span data-stu-id="37693-167">BrowserTab</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37693-168">Barre d’outils</span><span class="sxs-lookup"><span data-stu-id="37693-168">Toolbar</span></span></td>
<td><ul>
<li><span data-ttu-id="37693-169">Go</span><span class="sxs-lookup"><span data-stu-id="37693-169">Go</span></span></li>
<li><span data-ttu-id="37693-170">GoComposited</span><span class="sxs-lookup"><span data-stu-id="37693-170">GoComposited</span></span></li>
<li><span data-ttu-id="37693-171">InactiveGo</span><span class="sxs-lookup"><span data-stu-id="37693-171">InactiveGo</span></span></li>
<li><span data-ttu-id="37693-172">InactiveGoComposited</span><span class="sxs-lookup"><span data-stu-id="37693-172">InactiveGoComposited</span></span></li>
<li><span data-ttu-id="37693-173">MaxGo</span><span class="sxs-lookup"><span data-stu-id="37693-173">MaxGo</span></span></li>
<li><span data-ttu-id="37693-174">MaxGoComposited</span><span class="sxs-lookup"><span data-stu-id="37693-174">MaxGoComposited</span></span></li>
<li><span data-ttu-id="37693-175">MaxInactiveGo</span><span class="sxs-lookup"><span data-stu-id="37693-175">MaxInactiveGo</span></span></li>
<li><span data-ttu-id="37693-176">MaxInactiveGoComposited</span><span class="sxs-lookup"><span data-stu-id="37693-176">MaxInactiveGoComposited</span></span></li>
<li><span data-ttu-id="37693-177">Valeur SearchButton</span><span class="sxs-lookup"><span data-stu-id="37693-177">SearchButton</span></span></li>
<li><span data-ttu-id="37693-178">SearchButtonComposited</span><span class="sxs-lookup"><span data-stu-id="37693-178">SearchButtonComposited</span></span></li>
<li><span data-ttu-id="37693-179">Voyage</span><span class="sxs-lookup"><span data-stu-id="37693-179">Travel</span></span></li>
<li><span data-ttu-id="37693-180">TravelComposited</span><span class="sxs-lookup"><span data-stu-id="37693-180">TravelComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a><span data-ttu-id="37693-181">Sous-classes Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="37693-181">Internet Explorer Subclasses</span></span>

<span data-ttu-id="37693-182">Dans Windows Vista, les sous-classes de certaines classes internes à Windows Internet Explorer et l’Explorateur Windows sont disponibles, même si les classes elles-mêmes ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="37693-182">In Windows Vista, the subclasses of certain classes internal to Windows Internet Explorer and Windows Explorer are available even though the classes themselves are not.</span></span> <span data-ttu-id="37693-183">Le tableau suivant répertorie les sous-classes disponibles.</span><span class="sxs-lookup"><span data-stu-id="37693-183">The following table lists the available subclasses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37693-184">AddressBand</span><span class="sxs-lookup"><span data-stu-id="37693-184">AddressBand</span></span></td>
<td><ul>
<li><span data-ttu-id="37693-185">AB</span><span class="sxs-lookup"><span data-stu-id="37693-185">AB</span></span></li>
<li><span data-ttu-id="37693-186">ABGreen</span><span class="sxs-lookup"><span data-stu-id="37693-186">ABGreen</span></span></li>
<li><span data-ttu-id="37693-187">ABGreenComposited</span><span class="sxs-lookup"><span data-stu-id="37693-187">ABGreenComposited</span></span></li>
<li><span data-ttu-id="37693-188">ABRed</span><span class="sxs-lookup"><span data-stu-id="37693-188">ABRed</span></span></li>
<li><span data-ttu-id="37693-189">ABRedComposited</span><span class="sxs-lookup"><span data-stu-id="37693-189">ABRedComposited</span></span></li>
<li><span data-ttu-id="37693-190">ABYellow</span><span class="sxs-lookup"><span data-stu-id="37693-190">ABYellow</span></span></li>
<li><span data-ttu-id="37693-191">ABYellowComposited</span><span class="sxs-lookup"><span data-stu-id="37693-191">ABYellowComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37693-192">SearchBox</span><span class="sxs-lookup"><span data-stu-id="37693-192">SearchBox</span></span></td>
<td><ul>
<li><span data-ttu-id="37693-193">InactiveSearchBox</span><span class="sxs-lookup"><span data-stu-id="37693-193">InactiveSearchBox</span></span></li>
<li><span data-ttu-id="37693-194">InactiveSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="37693-194">InactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="37693-195">MaxInactiveSearchBox</span><span class="sxs-lookup"><span data-stu-id="37693-195">MaxInactiveSearchBox</span></span></li>
<li><span data-ttu-id="37693-196">MaxInactiveSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="37693-196">MaxInactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="37693-197">MaxSearchBox</span><span class="sxs-lookup"><span data-stu-id="37693-197">MaxSearchBox</span></span></li>
<li><span data-ttu-id="37693-198">MaxSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="37693-198">MaxSearchBoxComposited</span></span></li>
<li><span data-ttu-id="37693-199">SearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="37693-199">SearchBoxComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="37693-200">Le tableau suivant présente les spécificités de ces classes.</span><span class="sxs-lookup"><span data-stu-id="37693-200">The following table shows the specifics of these classes.</span></span>



| <span data-ttu-id="37693-201">Contrôler</span><span class="sxs-lookup"><span data-stu-id="37693-201">Control</span></span>     | <span data-ttu-id="37693-202">Partie</span><span class="sxs-lookup"><span data-stu-id="37693-202">Part</span></span>         | <span data-ttu-id="37693-203">États</span><span class="sxs-lookup"><span data-stu-id="37693-203">States</span></span>                                                 |
|-------------|--------------|--------------------------------------------------------|
| <span data-ttu-id="37693-204">ADDRESSBAND</span><span class="sxs-lookup"><span data-stu-id="37693-204">ADDRESSBAND</span></span> | <span data-ttu-id="37693-205">ABBACKGROUND</span><span class="sxs-lookup"><span data-stu-id="37693-205">ABBACKGROUND</span></span> | <span data-ttu-id="37693-206">NORMAL (0x1), chaud (0X2), désactivé (0x3), ayant le focus (0x4)</span><span class="sxs-lookup"><span data-stu-id="37693-206">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |
| <span data-ttu-id="37693-207">SEARCHBOX</span><span class="sxs-lookup"><span data-stu-id="37693-207">SEARCHBOX</span></span>   | <span data-ttu-id="37693-208">SBBACKGROUND</span><span class="sxs-lookup"><span data-stu-id="37693-208">SBBACKGROUND</span></span> | <span data-ttu-id="37693-209">NORMAL (0x1), chaud (0X2), désactivé (0x3), ayant le focus (0x4)</span><span class="sxs-lookup"><span data-stu-id="37693-209">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |



 

 

 




