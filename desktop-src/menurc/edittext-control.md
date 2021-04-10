---
title: EDITTEXT, contrôle
description: Définit un contrôle d’édition appartenant à la classe d’édition.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- Menus du contrôle EDITTEXT et autres ressources
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725877"
---
# <a name="edittext-control"></a><span data-ttu-id="e9086-104">EDITTEXT, contrôle</span><span class="sxs-lookup"><span data-stu-id="e9086-104">EDITTEXT control</span></span>

<span data-ttu-id="e9086-105">Définit un contrôle d’édition appartenant à la classe d’édition.</span><span class="sxs-lookup"><span data-stu-id="e9086-105">Defines an edit control belonging to the EDIT class.</span></span> <span data-ttu-id="e9086-106">Il crée une zone rectangulaire dans laquelle l’utilisateur peut taper et modifier du texte.</span><span class="sxs-lookup"><span data-stu-id="e9086-106">It creates a rectangular region in which the user can type and edit text.</span></span> <span data-ttu-id="e9086-107">Le contrôle affiche un curseur quand l’utilisateur clique sur la souris.</span><span class="sxs-lookup"><span data-stu-id="e9086-107">The control displays a cursor when the user clicks the mouse in it.</span></span> <span data-ttu-id="e9086-108">L’utilisateur peut ensuite utiliser le clavier pour entrer du texte ou modifier le texte existant.</span><span class="sxs-lookup"><span data-stu-id="e9086-108">The user can then use the keyboard to enter text or edit the existing text.</span></span> <span data-ttu-id="e9086-109">La modification des clés inclut les touches retour arrière et supprimer.</span><span class="sxs-lookup"><span data-stu-id="e9086-109">Editing keys include the BACKSPACE and DELETE keys.</span></span> <span data-ttu-id="e9086-110">L’utilisateur peut également utiliser la souris pour sélectionner les caractères à supprimer ou pour sélectionner l’emplacement d’insertion de nouveaux caractères.</span><span class="sxs-lookup"><span data-stu-id="e9086-110">The user can also use the mouse to select characters to be deleted or to select the place to insert new characters.</span></span>

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="e9086-111"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="e9086-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="e9086-112">Styles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="e9086-112">Control styles.</span></span> <span data-ttu-id="e9086-113">Cette valeur peut être une combinaison des styles de modification de classe et des styles suivants **: WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL**, **WS \_ HSCROLL** et **WS \_ désactivé**.</span><span class="sxs-lookup"><span data-stu-id="e9086-113">This value can be a combination of the edit class styles and the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, **WS\_HSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="e9086-114">Si vous ne spécifiez pas de style, le style par défaut est `ES_LEFT | WS_BORDER | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="e9086-114">If you do not specify a style, the default style is `ES_LEFT | WS_BORDER | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="e9086-115">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e9086-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e9086-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="e9086-116">Examples</span></span>

<span data-ttu-id="e9086-117">L’exemple suivant illustre l’utilisation de l’instruction **EDITTEXT** :</span><span class="sxs-lookup"><span data-stu-id="e9086-117">The following example demonstrates the use of the **EDITTEXT** statement:</span></span>

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="e9086-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9086-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9086-119">Contrôles d’édition</span><span class="sxs-lookup"><span data-stu-id="e9086-119">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> </dl>

 

 