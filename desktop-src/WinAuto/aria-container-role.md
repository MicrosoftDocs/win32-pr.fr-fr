---
title: Erreur de rôle de conteneur ARIA
description: Erreur de rôle de conteneur ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940272"
---
# <a name="aria-container-role-error"></a><span data-ttu-id="a4559-104">Erreur de rôle de conteneur ARIA</span><span class="sxs-lookup"><span data-stu-id="a4559-104">ARIA Container Role Error</span></span>

## <a name="text"></a><span data-ttu-id="a4559-105">Texte</span><span class="sxs-lookup"><span data-stu-id="a4559-105">Text</span></span>

<span data-ttu-id="a4559-106">L’élément avec un **descendant actif** défini n’a pas de rôle de conteneur (**ComboBox**, **Grid**, **ListBox**, **menu**, **BarreMenus**, **RadioGroup**, **Tree**, **contrôle TreeGrid**, **TabList**, **ligne**).</span><span class="sxs-lookup"><span data-stu-id="a4559-106">Element with **active-descendant** defined does not have a container role (**combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tree**, **treegrid**, **tablist**, **row**).</span></span>

## <a name="type"></a><span data-ttu-id="a4559-107">Type</span><span class="sxs-lookup"><span data-stu-id="a4559-107">Type</span></span>

<span data-ttu-id="a4559-108">Error</span><span class="sxs-lookup"><span data-stu-id="a4559-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="a4559-109">Description</span><span class="sxs-lookup"><span data-stu-id="a4559-109">Description</span></span>

<span data-ttu-id="a4559-110">Cette erreur s’applique aux éléments qui ont l’attribut **Aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="a4559-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="a4559-111">Un élément semble être un conteneur avec l’attribut **Aria-activedescendant** défini, mais l’attribut Role de l’élément n’a pas de valeur valide pour un conteneur.</span><span class="sxs-lookup"><span data-stu-id="a4559-111">An element appears to be a container that has the **aria-activedescendant** attribute set, but the element's role attribute doesn’t have a value that is valid for a container.</span></span>

<span data-ttu-id="a4559-112">Pour corriger cette erreur, définissez l’attribut **role** sur une valeur de rôle WAI-ARIA (Rich Internet applications) accessible par le Web Accessibility, qui est valide pour un élément conteneur : **ComboBox**, **Grid**, **ListBox**, **menu**, **BarreMenus**, **RadioGroup**, **TabList**, **Tree** ou **contrôle TreeGrid**.</span><span class="sxs-lookup"><span data-stu-id="a4559-112">To fix this error, set the **role** attribute to a Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value that is valid for a container element: **combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tablist**, **tree**, or **treegrid**.</span></span>

## <a name="example"></a><span data-ttu-id="a4559-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="a4559-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a><span data-ttu-id="a4559-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4559-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4559-115">Erreur de rôle ARIA</span><span class="sxs-lookup"><span data-stu-id="a4559-115">ARIA Role Error</span></span>](aria-role-invalid.md)
</dt> </dl>

 

 




