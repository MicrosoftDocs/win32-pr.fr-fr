---
title: Page, propriété
description: Page, propriété
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379924"
---
# <a name="page-property"></a><span data-ttu-id="39350-103">Page, propriété</span><span class="sxs-lookup"><span data-stu-id="39350-103">Page Property</span></span>

<span data-ttu-id="39350-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="39350-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="39350-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="39350-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="39350-106">Retourne ou définit la page affichée dans la fenêtre de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39350-106">Returns or sets the page displayed in the Microsoft Agent property sheet window.</span></span>

</dd> <dt>

<span data-ttu-id="39350-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="39350-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="39350-108">\*agent \* \* *.* \*  \[  =  *Chaîne* PropertySheet.page\]</span><span class="sxs-lookup"><span data-stu-id="39350-108">*agent\*\*\*.PropertySheet.Page*\* \[ = *string*\]</span></span>



| <span data-ttu-id="39350-109">Partie</span><span class="sxs-lookup"><span data-stu-id="39350-109">Part</span></span>     | <span data-ttu-id="39350-110">Description</span><span class="sxs-lookup"><span data-stu-id="39350-110">Description</span></span>                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39350-111">*string*</span><span class="sxs-lookup"><span data-stu-id="39350-111">*string*</span></span> | <span data-ttu-id="39350-112">Expression de chaîne avec l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="39350-112">A string expression with one of the following values.</span></span> <span data-ttu-id="39350-113">**« Parole »** Affiche la page d’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="39350-113">**"Speech"** Displays the Speech Input page.</span></span><br/> <span data-ttu-id="39350-114">**« Sortie »** Affiche la page sortie.</span><span class="sxs-lookup"><span data-stu-id="39350-114">**"Output"** Displays the Output page.</span></span><br/> <span data-ttu-id="39350-115">**« Copyright »** Affiche la page de copyright.</span><span class="sxs-lookup"><span data-stu-id="39350-115">**"Copyright"** Displays the Copyright page.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39350-116">Notes</span><span class="sxs-lookup"><span data-stu-id="39350-116">Remarks</span></span>

<span data-ttu-id="39350-117">Si aucun moteur de reconnaissance vocale n’est installé, la définition de la valeur **« parole »** de la **page** n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="39350-117">If no speech engine is installed, setting **Page** to **"Speech"** has no effect.</span></span> <span data-ttu-id="39350-118">En outre, la propriété **visible** de la fenêtre doit avoir la valeur **true** pour permettre à l’utilisateur d’afficher la page.</span><span class="sxs-lookup"><span data-stu-id="39350-118">Also, the window's **Visible** property must be set to **True** for the user to see the page.</span></span>

> [!Note]  
> <span data-ttu-id="39350-119">L’utilisateur peut remplacer cette propriété.</span><span class="sxs-lookup"><span data-stu-id="39350-119">The user can override this property.</span></span>

 

 

 





