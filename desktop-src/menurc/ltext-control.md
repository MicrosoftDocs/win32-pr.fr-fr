---
title: Contrôle LTEXT
description: Définit un contrôle de texte aligné à gauche.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Menus du contrôle LTEXT et autres ressources
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509253"
---
# <a name="ltext-control"></a><span data-ttu-id="a0e6b-104">Contrôle LTEXT</span><span class="sxs-lookup"><span data-stu-id="a0e6b-104">LTEXT control</span></span>

<span data-ttu-id="a0e6b-105">Définit un contrôle de texte aligné à gauche.</span><span class="sxs-lookup"><span data-stu-id="a0e6b-105">Defines a left-aligned text control.</span></span> <span data-ttu-id="a0e6b-106">Le contrôle est un rectangle simple qui affiche le texte spécifié à gauche dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="a0e6b-106">The control is a simple rectangle displaying the given text left-aligned in the rectangle.</span></span> <span data-ttu-id="a0e6b-107">Le texte est mis en forme avant d’être affiché.</span><span class="sxs-lookup"><span data-stu-id="a0e6b-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="a0e6b-108">Les mots qui s’étendent au-delà de la fin d’une ligne sont automatiquement renvoyés au début de la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="a0e6b-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="a0e6b-109">Les mots qui sont plus longs que la largeur du contrôle sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="a0e6b-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="a0e6b-110">L’instruction **LTEXT** , qui peut être utilisée uniquement dans une instruction [**DIALOGEX**](dialogex-resource.md) , définit le texte, l’identificateur, les dimensions et les attributs du contrôle.</span><span class="sxs-lookup"><span data-stu-id="a0e6b-110">The **LTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="a0e6b-111"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="a0e6b-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="a0e6b-112">Styles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="a0e6b-112">Control styles.</span></span> <span data-ttu-id="a0e6b-113">Cette valeur peut être n’importe quelle combinaison du style **\_ RadioButton BS** et des styles suivants : **SS \_ Left**, **WS \_ TABSTOP** et **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="a0e6b-113">This value can be any combination of the **BS\_RADIOBUTTON** style and the following styles: **SS\_LEFT**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="a0e6b-114">Si vous ne spécifiez pas de style, le style par défaut est `SS_LEFT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="a0e6b-114">If you do not specify a style, the default style is `SS_LEFT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="a0e6b-115">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a0e6b-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a0e6b-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="a0e6b-116">Examples</span></span>

<span data-ttu-id="a0e6b-117">Cet exemple définit un contrôle de texte aligné à gauche nommé filename :</span><span class="sxs-lookup"><span data-stu-id="a0e6b-117">This example defines a left-aligned text control that is labeled Filename:</span></span>

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="a0e6b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0e6b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e6b-119">**RÉGULATION**</span><span class="sxs-lookup"><span data-stu-id="a0e6b-119">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="a0e6b-120">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="a0e6b-120">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="a0e6b-121">Contrôles d’édition</span><span class="sxs-lookup"><span data-stu-id="a0e6b-121">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="a0e6b-122">**RTEXT**</span><span class="sxs-lookup"><span data-stu-id="a0e6b-122">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 