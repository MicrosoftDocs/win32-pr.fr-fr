---
title: Contrôle RTEXT
description: Définit un contrôle de texte aligné à droite.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Menus du contrôle RTEXT et autres ressources
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463134"
---
# <a name="rtext-control"></a><span data-ttu-id="94b87-104">Contrôle RTEXT</span><span class="sxs-lookup"><span data-stu-id="94b87-104">RTEXT control</span></span>

<span data-ttu-id="94b87-105">Définit un contrôle de texte aligné à droite.</span><span class="sxs-lookup"><span data-stu-id="94b87-105">Defines a right-aligned text control.</span></span> <span data-ttu-id="94b87-106">Le contrôle est un rectangle simple qui affiche le texte donné aligné à droite dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="94b87-106">The control is a simple rectangle displaying the given text right-aligned in the rectangle.</span></span> <span data-ttu-id="94b87-107">Le texte est mis en forme avant d’être affiché.</span><span class="sxs-lookup"><span data-stu-id="94b87-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="94b87-108">Les mots qui s’étendent au-delà de la fin d’une ligne sont automatiquement renvoyés au début de la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="94b87-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="94b87-109">Les mots qui sont plus longs que la largeur du contrôle sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="94b87-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="94b87-110">L’instruction **rtext** , qui peut être utilisée uniquement dans une instruction [**DIALOGEX**](dialogex-resource.md) , définit le texte, l’identificateur, les dimensions et les attributs du contrôle.</span><span class="sxs-lookup"><span data-stu-id="94b87-110">The **RTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="94b87-111"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="94b87-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="94b87-112">Styles pour le contrôle de texte, qui peut être n’importe quelle combinaison des éléments suivants : **WS \_ TABSTOP** et **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="94b87-112">Styles for the text control, which can be any combination of the following: **WS\_TABSTOP** and **WS\_GROUP**.</span></span>

<span data-ttu-id="94b87-113">Si vous ne spécifiez pas de style, le style par défaut est `SS_RIGHT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="94b87-113">If you do not specify a style, the default style is `SS_RIGHT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="94b87-114">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="94b87-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="94b87-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="94b87-115">Examples</span></span>

<span data-ttu-id="94b87-116">L’exemple suivant illustre l’utilisation de l’instruction **rtext** :</span><span class="sxs-lookup"><span data-stu-id="94b87-116">The following example demonstrates the use of the **RTEXT** statement:</span></span>

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="94b87-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94b87-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b87-118">**RÉGULATION**</span><span class="sxs-lookup"><span data-stu-id="94b87-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="94b87-119">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="94b87-119">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="94b87-120">Contrôles d’édition</span><span class="sxs-lookup"><span data-stu-id="94b87-120">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="94b87-121">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="94b87-121">**LTEXT**</span></span>](ltext-control.md)
</dt> </dl>

 

 