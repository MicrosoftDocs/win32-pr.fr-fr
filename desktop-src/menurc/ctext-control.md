---
title: Contrôle CTEXT
description: Définit un contrôle de texte centré.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Menus du contrôle CTEXT et autres ressources
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101553"
---
# <a name="ctext-control"></a><span data-ttu-id="bf924-104">Contrôle CTEXT</span><span class="sxs-lookup"><span data-stu-id="bf924-104">CTEXT control</span></span>

<span data-ttu-id="bf924-105">Définit un contrôle de texte centré.</span><span class="sxs-lookup"><span data-stu-id="bf924-105">Defines a centered-text control.</span></span> <span data-ttu-id="bf924-106">Le contrôle est un rectangle simple qui affiche le texte donné centré dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="bf924-106">The control is a simple rectangle displaying the given text centered in the rectangle.</span></span> <span data-ttu-id="bf924-107">Le texte est mis en forme avant d’être affiché.</span><span class="sxs-lookup"><span data-stu-id="bf924-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="bf924-108">Les mots qui s’étendent au-delà de la fin d’une ligne sont automatiquement renvoyés au début de la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="bf924-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="bf924-109">Les mots qui sont plus longs que la largeur du contrôle sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="bf924-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="bf924-110">L’instruction [**LTEXT**](ltext-control.md) , qui peut être utilisée uniquement dans une instruction REP, définit le texte, l’identificateur, les dimensions et les attributs du contrôle.</span><span class="sxs-lookup"><span data-stu-id="bf924-110">The [**LTEXT**](ltext-control.md) statement, which can be used only in a rep statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="bf924-111"><span id="text"></span><span id="TEXT"></span>*financière*</span><span class="sxs-lookup"><span data-stu-id="bf924-111"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="bf924-112">Texte à centrer dans la zone rectangulaire du contrôle.</span><span class="sxs-lookup"><span data-stu-id="bf924-112">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="bf924-113"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="bf924-113"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="bf924-114">Styles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="bf924-114">Control styles.</span></span> <span data-ttu-id="bf924-115">Cette valeur peut être n’importe quelle combinaison des styles suivants : **SS \_ Center**, **WS \_ TABSTOP** et **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="bf924-115">This value can be any combination of the following styles: **SS\_CENTER**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="bf924-116">Si vous ne spécifiez pas de style, le style par défaut est `SS_CENTER | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="bf924-116">If you do not specify a style, the default style is `SS_CENTER | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="bf924-117">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bf924-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bf924-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="bf924-118">Examples</span></span>

<span data-ttu-id="bf924-119">Cet exemple définit un contrôle de texte centré intitulé filename :</span><span class="sxs-lookup"><span data-stu-id="bf924-119">This example defines a centered-text control that is labeled Filename:</span></span>

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a><span data-ttu-id="bf924-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf924-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf924-121">**RÉGULATION**</span><span class="sxs-lookup"><span data-stu-id="bf924-121">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="bf924-122">Contrôles d’édition</span><span class="sxs-lookup"><span data-stu-id="bf924-122">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="bf924-123">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="bf924-123">**LTEXT**</span></span>](ltext-control.md)
</dt> <dt>

[<span data-ttu-id="bf924-124">**RTEXT**</span><span class="sxs-lookup"><span data-stu-id="bf924-124">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 