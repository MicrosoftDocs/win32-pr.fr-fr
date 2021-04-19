---
title: Command. KeyTip, propriété
description: Représente la touche d’interfaut pour un contrôle.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Propriété Command. KeyTip Windows, ruban
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518107"
---
# <a name="commandkeytip-property"></a><span data-ttu-id="c2773-104">Command. KeyTip, propriété</span><span class="sxs-lookup"><span data-stu-id="c2773-104">Command.Keytip property</span></span>

<span data-ttu-id="c2773-105">Représente la touche d’interfaut pour un contrôle.</span><span class="sxs-lookup"><span data-stu-id="c2773-105">Represents the keytip for a control.</span></span>

## <a name="usage"></a><span data-ttu-id="c2773-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="c2773-106">Usage</span></span>

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a><span data-ttu-id="c2773-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="c2773-107">Attributes</span></span>

<span data-ttu-id="c2773-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="c2773-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c2773-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c2773-109">Child elements</span></span>



| <span data-ttu-id="c2773-110">Élément</span><span class="sxs-lookup"><span data-stu-id="c2773-110">Element</span></span>                                                   | <span data-ttu-id="c2773-111">Description</span><span class="sxs-lookup"><span data-stu-id="c2773-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="c2773-112">**String**</span><span class="sxs-lookup"><span data-stu-id="c2773-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="c2773-113">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="c2773-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c2773-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c2773-114">Parent elements</span></span>



| <span data-ttu-id="c2773-115">Élément</span><span class="sxs-lookup"><span data-stu-id="c2773-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="c2773-116">**Commande**</span><span class="sxs-lookup"><span data-stu-id="c2773-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c2773-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c2773-117">Remarks</span></span>

<span data-ttu-id="c2773-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="c2773-118">Optional.</span></span>

<span data-ttu-id="c2773-119">Peut se produire au plus une fois pour chaque élément de [**commande**](windowsribbon-element-command.md) .</span><span class="sxs-lookup"><span data-stu-id="c2773-119">May occur at most once for each [**Command**](windowsribbon-element-command.md) element.</span></span>

<span data-ttu-id="c2773-120">**Command. KeyTip** peut contenir une valeur de type *XS : String* limitée à toute séquence de caractères Unicode, y compris un espace blanc.</span><span class="sxs-lookup"><span data-stu-id="c2773-120">**Command.Keytip** can contain a value of type *xs:string* constrained to any sequence of Unicode characters, including white space.</span></span>

<span data-ttu-id="c2773-121">Une **commande. KeyTip** peut commencer par un nombre uniquement lorsqu’elle est associée à un contrôle dans un [onglet](windowsribbon-controls-tab.md) ou la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="c2773-121">A **Command.Keytip** can begin with a number only when associated with a control within a [Tab](windowsribbon-controls-tab.md) or the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="c2773-122">Pour afficher les touches d’affichage qui sont valides pour l’état actuel du ruban, maintenez la touche ALT enfoncée.</span><span class="sxs-lookup"><span data-stu-id="c2773-122">To display the keytips that are valid for the current state of the ribbon, press and hold the ALT key.</span></span> <span data-ttu-id="c2773-123">La capture d’écran suivante montre les info-bulles initiales qui s’affichent dans Microsoft Paint pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c2773-123">The following screen shot shows the initial, or first level, keytips that are displayed in Microsoft Paint for Windows 7.</span></span> <span data-ttu-id="c2773-124">Une fois qu’un KeyTip de premier niveau a été sélectionné, seules les touches de deuxième niveau sont affichées.</span><span class="sxs-lookup"><span data-stu-id="c2773-124">After a first-level keytip has been selected, only second-level keytips are displayed.</span></span>

![touches accélératrices de premier niveau dans Microsoft Paint pour Windows 7](images/properties/ui-pkey-label-keytips.png)

<span data-ttu-id="c2773-126">**Command. KeyTip** agit comme touche de raccourci pour une commande, sauf si cette commande est exposée par le biais d’un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="c2773-126">**Command.Keytip** acts as the keyboard accelerator for a command unless that command is exposed through a menu item.</span></span> <span data-ttu-id="c2773-127">Dans ce cas, le Framework ignore la valeur **Command. KeyTip** et utilise à la place un caractère précédé d’un signe & comme spécifié par [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [l' \_ \_ étiquette de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="c2773-127">In this case, the framework ignores the **Command.Keytip** value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="c2773-128">Si aucune esperluette n’est spécifiée par la **commande. LabelTitle** ou l' \_ \_ étiquette de nom de l’interface utilisateur, aucune touche d’accès ou touche d’accès rapide n’est exposée.</span><span class="sxs-lookup"><span data-stu-id="c2773-128">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="c2773-129">Si aucune valeur n’est fournie pour **Command. KeyTip**, l’élément enfant [**String**](windowsribbon-element-string.md) est requis.</span><span class="sxs-lookup"><span data-stu-id="c2773-129">If no value is supplied for **Command.Keytip**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="c2773-130">Si **Command. KeyTip** contient à la fois une valeur et un élément enfant de [**chaîne**](windowsribbon-element-string.md) , la **chaîne** est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="c2773-130">If **Command.Keytip** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="c2773-131">Par défaut, le Framework utilise les lettres suivantes pour générer automatiquement des touches d’info-bulle :</span><span class="sxs-lookup"><span data-stu-id="c2773-131">By default, the following letters are used by the framework to automatically generate keytips:</span></span>

-   <span data-ttu-id="c2773-132">**F** est assigné au menu de l' [application](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="c2773-132">**F** is assigned to the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="c2773-133">**Y** est assigné à toute commande qui n’a pas de KeyTip spécifié par l’application.</span><span class="sxs-lookup"><span data-stu-id="c2773-133">**Y** is assigned to any command that does not have a keytip specified by the application.</span></span>
-   <span data-ttu-id="c2773-134">**Z** est assigné à chaque contrôle de [groupe](windowsribbon-controls-group.md) et ne peut pas être personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c2773-134">**Z** is assigned to each [Group](windowsribbon-controls-group.md) control and cannot be customized.</span></span> <span data-ttu-id="c2773-135">Un KeyTip de groupe s’affiche uniquement lorsque le [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) du contrôle spécifie une option de taille de **menu contextuel** .</span><span class="sxs-lookup"><span data-stu-id="c2773-135">A Group keytip is displayed only when the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) for the control specifies a **Popup** size option.</span></span> <span data-ttu-id="c2773-136">Pour plus d’informations, consultez [Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="c2773-136">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

> [!Note]  
> <span data-ttu-id="c2773-137">Aucune de ces lettres n’est réservée par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="c2773-137">None of these letters are reserved by the framework.</span></span> <span data-ttu-id="c2773-138">Chaque peut être assigné à une ou plusieurs commandes selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="c2773-138">Each can be assigned to one or more commands as required.</span></span>

 

<span data-ttu-id="c2773-139">Le Framework résout les conflits KeyTip des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2773-139">The framework resolves keytip conflicts in the following ways:</span></span>

-   <span data-ttu-id="c2773-140">Si un ou plusieurs contrôles [onglet](windowsribbon-controls-tab.md) sont associés au même KeyTip, un nombre est ajouté à chaque KeyTip, en commençant à 1, et en accroissant de façon séquentielle (2,3,...) pour chaque contrôle dans l’ordre de déclaration.</span><span class="sxs-lookup"><span data-stu-id="c2773-140">If one or more [Tab](windowsribbon-controls-tab.md) controls are associated with the same keytip, a number is appended to each keytip, starting at 1, and increasing sequentially (2, 3,...) for each control in the order of declaration.</span></span> <span data-ttu-id="c2773-141">Si des contrôles onglet se voient attribuer la lettre F comme touche d’activation, le menu de l' [application](windowsribbon-controls-applicationmenu.md) reçoit la touche F1 avec les touches accélératrices restantes ajustées comme décrit.</span><span class="sxs-lookup"><span data-stu-id="c2773-141">If any Tab controls are assigned the letter F as a keytip, the [Application Menu](windowsribbon-controls-applicationmenu.md) is assigned F1 with the remaining keytips adjusted as described.</span></span>
-   <span data-ttu-id="c2773-142">Lorsqu’il est associé à un contrôle unique dans un [onglet](windowsribbon-controls-tab.md), le KeyTip F est valide à la fois pour le menu de l' [application](windowsribbon-controls-applicationmenu.md)et le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c2773-142">When associated with a single control within a [Tab](windowsribbon-controls-tab.md), the keytip F is valid for both the control and the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="c2773-143">Le menu d’application par défaut KeyTip n’est pas modifié, mais la priorité est donnée au contrôle sous l’onglet actif.</span><span class="sxs-lookup"><span data-stu-id="c2773-143">The default Application Menu keytip is not changed, but precedence is given to the control on the active tab.</span></span>
-   <span data-ttu-id="c2773-144">Si un ou plusieurs contrôles d’un [onglet](windowsribbon-controls-tab.md) sont associés au même KeyTip, le Framework refactorise automatiquement les touches d’info-bulle de ces contrôles, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="c2773-144">If one or more controls within a [Tab](windowsribbon-controls-tab.md) are associated with the same keytip, the framework automatically refactors the keytips of those controls, as described previously.</span></span>

> [!Note]  
> <span data-ttu-id="c2773-145">Une légère variation de la couleur du texte est utilisée pour mettre en surbrillance les touches réfactorisées dans une implémentation de ruban standard.</span><span class="sxs-lookup"><span data-stu-id="c2773-145">A slight variation in text color is used to highlight refactored keytips in a standard ribbon implementation.</span></span> <span data-ttu-id="c2773-146">Pour une implémentation de ruban non standard où la couleur du ruban a été personnalisée, ce comportement de l’infrastructure est substitué et toutes les touches sont affichées avec la même couleur de texte.</span><span class="sxs-lookup"><span data-stu-id="c2773-146">For a nonstandard ribbon implementation where the ribbon color has been customized, this framework behavior is overridden and all keytips are displayed with the same text color.</span></span> <span data-ttu-id="c2773-147">Pour plus d’informations, consultez [Personnalisation des couleurs du ruban](ribbon-color.md).</span><span class="sxs-lookup"><span data-stu-id="c2773-147">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>

 

<span data-ttu-id="c2773-148">La longueur maximale est illimitée.</span><span class="sxs-lookup"><span data-stu-id="c2773-148">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="c2773-149">Exemples</span><span class="sxs-lookup"><span data-stu-id="c2773-149">Examples</span></span>

<span data-ttu-id="c2773-150">L’exemple suivant illustre le balisage pour un élément [**Command**](windowsribbon-element-command.md) avec une déclaration **Command. KeyTip** .</span><span class="sxs-lookup"><span data-stu-id="c2773-150">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Keytip** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="c2773-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2773-151">Requirements</span></span>



| <span data-ttu-id="c2773-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2773-152">Requirement</span></span> | <span data-ttu-id="c2773-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2773-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c2773-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2773-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c2773-155">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2773-155">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c2773-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2773-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c2773-157">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2773-157">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2773-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2773-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2773-159">KeyTip de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="c2773-159">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





