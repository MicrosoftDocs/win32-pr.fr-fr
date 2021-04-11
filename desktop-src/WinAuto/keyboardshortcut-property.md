---
title: Propriété KeyboardShortcut
description: La propriété KeyboardShortcut décrit une touche ou une combinaison de touches qui active un objet accessible spécifié.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196801"
---
# <a name="keyboardshortcut-property"></a><span data-ttu-id="134b8-103">Propriété KeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="134b8-103">KeyboardShortcut Property</span></span>

<span data-ttu-id="134b8-104">La propriété **KeyboardShortcut** décrit une touche ou une combinaison de touches qui active un objet accessible spécifié.</span><span class="sxs-lookup"><span data-stu-id="134b8-104">The **KeyboardShortcut** property describes a key or key combination that activates a specified accessible object.</span></span>

<span data-ttu-id="134b8-105">La propriété **KeyboardShortcut** est récupérée en appelant [**IAccessible :: obten \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span><span class="sxs-lookup"><span data-stu-id="134b8-105">The **KeyboardShortcut** property is retrieved by calling [**IAccessible::get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span></span>

<span data-ttu-id="134b8-106">La chaîne Récupérée décrit une *touche de raccourci* (également appelée raccourci clavier) ou une *touche d’accès* *rapide*(également appelée « *mnémonique*»).</span><span class="sxs-lookup"><span data-stu-id="134b8-106">The retrieved string describes a *shortcut key* (also called a *keyboard accelerator*) or an *access key* (also called a *mnemonic*).</span></span> <span data-ttu-id="134b8-107">Une touche d’accès est un caractère souligné dans le texte d’un menu, d’un élément de menu ou d’une étiquette d’un contrôle tel qu’un bouton de commande.</span><span class="sxs-lookup"><span data-stu-id="134b8-107">An access key is an underlined character in the text of a menu, menu item, or label of a control such as a push button.</span></span>

<span data-ttu-id="134b8-108">La chaîne Récupérée doit contenir le nom de la clé avec la ou les touches de modification.</span><span class="sxs-lookup"><span data-stu-id="134b8-108">The retrieved string must contain the name of the key along with the modifier key or keys.</span></span> <span data-ttu-id="134b8-109">La chaîne doit être au format suivant afin que les clients puissent l’analyser facilement : \[ \[ touche de modification \] + \[ ... \] + \] nom de clé.</span><span class="sxs-lookup"><span data-stu-id="134b8-109">The string must be in the following format so that clients can easily parse it: \[\[modifier key\]+\[...\]+\] key name.</span></span>

<span data-ttu-id="134b8-110">Voici quelques exemples : ALT + F, CTRL + ALT + 4, WIN + F1, CTRL + ALT + MAJ + retour arrière ou retour arrière.</span><span class="sxs-lookup"><span data-stu-id="134b8-110">Examples include ALT+F, CTRL+ALT+4, WIN+F1, CTRL+ALT+SHIFT+BACKSPACE, or simply BACKSPACE.</span></span>

<span data-ttu-id="134b8-111">Le tableau suivant répertorie les touches de modification.</span><span class="sxs-lookup"><span data-stu-id="134b8-111">The following table lists modifier keys.</span></span>



| <span data-ttu-id="134b8-112">Touche de modification</span><span class="sxs-lookup"><span data-stu-id="134b8-112">Modifier key</span></span> | <span data-ttu-id="134b8-113">Description</span><span class="sxs-lookup"><span data-stu-id="134b8-113">Description</span></span>                        |
|--------------|------------------------------------|
| <span data-ttu-id="134b8-114">Alt</span><span class="sxs-lookup"><span data-stu-id="134b8-114">ALT</span></span>          | <span data-ttu-id="134b8-115">Autre touche de modification</span><span class="sxs-lookup"><span data-stu-id="134b8-115">Alternate modifier key</span></span>             |
| <span data-ttu-id="134b8-116">CTRL</span><span class="sxs-lookup"><span data-stu-id="134b8-116">CTRL</span></span>         | <span data-ttu-id="134b8-117">Touche de modification de contrôle</span><span class="sxs-lookup"><span data-stu-id="134b8-117">Control modifier key</span></span>               |
| <span data-ttu-id="134b8-118">MAJUSCULE</span><span class="sxs-lookup"><span data-stu-id="134b8-118">SHIFT</span></span>        | <span data-ttu-id="134b8-119">Touche de modification MAJ</span><span class="sxs-lookup"><span data-stu-id="134b8-119">Shift modifier key</span></span>                 |
| <span data-ttu-id="134b8-120">GAGN</span><span class="sxs-lookup"><span data-stu-id="134b8-120">WIN</span></span>          | <span data-ttu-id="134b8-121">Touche Windows</span><span class="sxs-lookup"><span data-stu-id="134b8-121">Windows logo key</span></span>                   |
| <span data-ttu-id="134b8-122">FN</span><span class="sxs-lookup"><span data-stu-id="134b8-122">FN</span></span>           | <span data-ttu-id="134b8-123">Touche de fonction sur les ordinateurs portables</span><span class="sxs-lookup"><span data-stu-id="134b8-123">Function key on portable computers</span></span> |



 

<span data-ttu-id="134b8-124">Ne Localisez pas les chaînes de raccourcis clavier.</span><span class="sxs-lookup"><span data-stu-id="134b8-124">Do not localize keyboard shortcut strings.</span></span>

## <a name="handling-objects-that-have-both-key-types"></a><span data-ttu-id="134b8-125">Gestion des objets qui ont les deux types de clés</span><span class="sxs-lookup"><span data-stu-id="134b8-125">Handling Objects That Have Both Key Types</span></span>

<span data-ttu-id="134b8-126">Si un objet a à la fois une touche de raccourci et une touche d’accès rapide, la propriété **KeyboardShortcut** retourne la clé d’accès.</span><span class="sxs-lookup"><span data-stu-id="134b8-126">If an object has both a shortcut key and an access key, the **KeyboardShortcut** property returns the access key.</span></span> <span data-ttu-id="134b8-127">La touche d’accès est celle qu’un utilisateur aurait appuyé lorsque l’objet ou le parent de l’objet a le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="134b8-127">The access key is the one a user would press when the object or the object's parent has the keyboard focus.</span></span> <span data-ttu-id="134b8-128">Par exemple, l’élément de menu **Imprimer** peut avoir à la fois une touche de raccourci (Ctrl + P) et une touche d’accès rapide (P).</span><span class="sxs-lookup"><span data-stu-id="134b8-128">For example, the **Print** menu item might have both a shortcut key (CTRL+P) and an access key (P).</span></span> <span data-ttu-id="134b8-129">Si un utilisateur appuie sur CTRL + P alors que le menu est actif, rien ne se produit.</span><span class="sxs-lookup"><span data-stu-id="134b8-129">If a user presses CTRL+P while the menu is active, nothing happens.</span></span> <span data-ttu-id="134b8-130">Toutefois, si un utilisateur appuie sur P alors que le menu est actif, il appelle la boîte de dialogue **Imprimer** de l’application.</span><span class="sxs-lookup"><span data-stu-id="134b8-130">But if a user presses P while the menu is active, it invokes the application's **Print** dialog box.</span></span> <span data-ttu-id="134b8-131">Dans ce cas, la propriété **KeyboardShortcut** est « P » pour refléter ce que l’utilisateur doit appuyer lorsque le menu a le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="134b8-131">In this case, the **KeyboardShortcut** property is "P" to reflect what the user must press when the menu has the keyboard focus.</span></span>

 

 




