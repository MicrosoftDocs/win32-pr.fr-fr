---
title: Erreur de TabIndex du conteneur ARIA
description: Erreur de TabIndex du conteneur ARIA
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- AriaContainerTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380307"
---
# <a name="aria-container-tabindex-error"></a><span data-ttu-id="78212-104">Erreur de TabIndex du conteneur ARIA</span><span class="sxs-lookup"><span data-stu-id="78212-104">ARIA Container Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="78212-105">Texte</span><span class="sxs-lookup"><span data-stu-id="78212-105">Text</span></span>

<span data-ttu-id="78212-106">L’élément est un conteneur pouvant être actif avec des descendants actifs définis, mais sans valeur **TabIndex** supérieure ou égale à 0.</span><span class="sxs-lookup"><span data-stu-id="78212-106">Element is a focusable container with active descendants defined but without **tabindex** value greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="78212-107">Type</span><span class="sxs-lookup"><span data-stu-id="78212-107">Type</span></span>

<span data-ttu-id="78212-108">Error</span><span class="sxs-lookup"><span data-stu-id="78212-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="78212-109">Description</span><span class="sxs-lookup"><span data-stu-id="78212-109">Description</span></span>

<span data-ttu-id="78212-110">Cette erreur s’applique aux éléments qui ont l’attribut **Aria-activedescendant** , qui ne sont pas désactivés et dont l’attribut **TabIndex** n’est pas défini sur une valeur supérieure ou égale à 0.</span><span class="sxs-lookup"><span data-stu-id="78212-110">This error applies to elements that have the **aria-activedescendant** attribute, are not disabled, and do not have the **tabindex** attribute set to a value that is greater than or equal to 0.</span></span> <span data-ttu-id="78212-111">Ces éléments doivent être dans l’ordre de tabulation, car ils sont chargés de gérer les événements de clavier pour leurs éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="78212-111">These elements must be in tab order because they are responsible for handling keyboard events for their child elements.</span></span>

<span data-ttu-id="78212-112">Pour corriger cette erreur, affectez à l’attribut **TabIndex** une valeur supérieure ou égale à 0.</span><span class="sxs-lookup"><span data-stu-id="78212-112">To fix this error, set the **tabindex** attribute to a value that is greater than or equal to 0.</span></span>

## <a name="example"></a><span data-ttu-id="78212-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="78212-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
       <div role="option" id="listbox1-1" class="selected">Item 1</div> 
       <div role="option" id="listbox1-2">Item 2</div> 

       <div role="option" id="listbox1-3">Item 3</div>
      ... 
<div>
```



## <a name="related-topics"></a><span data-ttu-id="78212-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78212-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78212-115">Erreur TabIndex du rôle de conteneur ARIA (sans descendant actif)</span><span class="sxs-lookup"><span data-stu-id="78212-115">ARIA Container Role (without active descendant) Tabindex Error</span></span>](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




