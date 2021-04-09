---
title: LISTBOX, contrôle (menus et autres ressources)
description: Définit les contrôles couramment utilisés pour une boîte de dialogue ou une fenêtre. Le contrôle est un rectangle qui contient une liste de chaînes (telles que des noms de fichiers) à partir desquelles l’utilisateur peut sélectionner.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Menus du contrôle LISTBOX et autres ressources
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101608"
---
# <a name="listbox-control"></a><span data-ttu-id="29d37-105">LISTBOX, contrôle</span><span class="sxs-lookup"><span data-stu-id="29d37-105">LISTBOX control</span></span>

<span data-ttu-id="29d37-106">Définit les contrôles couramment utilisés pour une boîte de dialogue ou une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="29d37-106">Defines commonly used controls for a dialog box or window.</span></span> <span data-ttu-id="29d37-107">Le contrôle est un rectangle qui contient une liste de chaînes (telles que des noms de fichiers) à partir desquelles l’utilisateur peut sélectionner.</span><span class="sxs-lookup"><span data-stu-id="29d37-107">The control is a rectangle containing a list of strings (such as filenames) from which the user can select.</span></span>

<span data-ttu-id="29d37-108">L’instruction **ListBox** , qui peut uniquement être utilisée dans une instruction [**DIALOGEX**](dialogex-resource.md) ou **Window** , définit l’identificateur, les dimensions et les attributs d’une fenêtre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="29d37-108">The **LISTBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) or **WINDOW** statement, defines the identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="29d37-109"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="29d37-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="29d37-110">Styles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="29d37-110">Control styles.</span></span> <span data-ttu-id="29d37-111">Cette valeur peut être une combinaison des styles de classe de zone de liste et de l’un des styles suivants : **WS \_ Border** et **WS \_ VSCROLL**.</span><span class="sxs-lookup"><span data-stu-id="29d37-111">This value can be a combination of the list-box class styles and any of the following styles: **WS\_BORDER** and **WS\_VSCROLL**.</span></span>

<span data-ttu-id="29d37-112">Si vous ne spécifiez pas de style, le style par défaut est `LBS_NOTIFY | WS_BORDER` .</span><span class="sxs-lookup"><span data-stu-id="29d37-112">If you do not specify a style, the default style is `LBS_NOTIFY | WS_BORDER`.</span></span>

</dd> </dl>

<span data-ttu-id="29d37-113">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="29d37-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="29d37-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="29d37-114">Examples</span></span>

<span data-ttu-id="29d37-115">Cet exemple définit un contrôle de zone de liste dont l’identificateur est 101 :</span><span class="sxs-lookup"><span data-stu-id="29d37-115">This example defines a list-box control whose identifier is 101:</span></span>

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="29d37-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29d37-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d37-117">**COMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="29d37-117">**COMBOBOX**</span></span>](combobox-control.md)
</dt> <dt>

[<span data-ttu-id="29d37-118">Zones de liste</span><span class="sxs-lookup"><span data-stu-id="29d37-118">List Boxes</span></span>](../controls/about-list-boxes.md)
</dt> </dl>

 

 