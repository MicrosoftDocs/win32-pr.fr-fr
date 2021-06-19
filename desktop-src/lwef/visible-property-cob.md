---
title: Visible, propriété (objet Characters)
description: En savoir plus sur la propriété visible de l’objet Characters, qui retourne une valeur booléenne indiquant si le caractère est visible.
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7358cd87a7fb3232b22cef33cbee5f2609708875
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396304"
---
# <a name="visible-property-characters-object"></a><span data-ttu-id="17078-103">Visible, propriété (objet Characters)</span><span class="sxs-lookup"><span data-stu-id="17078-103">Visible Property (Characters Object)</span></span>

<span data-ttu-id="17078-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="17078-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="17078-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="17078-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="17078-106">Retourne une valeur booléenne indiquant si le caractère est visible.</span><span class="sxs-lookup"><span data-stu-id="17078-106">Returns a Boolean indicating whether the character is visible.</span></span>

</dd> <dt>

<span data-ttu-id="17078-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="17078-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="17078-108">\*agent \***. Caractères (**"\* CharacterID *" \* *). Visible**</span><span class="sxs-lookup"><span data-stu-id="17078-108">*agent\***.Characters(**"* CharacterID *"\*\*).Visible*\*</span></span>



| <span data-ttu-id="17078-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="17078-109">Value</span></span> | <span data-ttu-id="17078-110">Description</span><span class="sxs-lookup"><span data-stu-id="17078-110">Description</span></span>                            |
|-------|----------------------------------------|
| <span data-ttu-id="17078-111">True</span><span class="sxs-lookup"><span data-stu-id="17078-111">True</span></span>  | <span data-ttu-id="17078-112">Le caractère est affiché.</span><span class="sxs-lookup"><span data-stu-id="17078-112">The character is displayed.</span></span>            |
| <span data-ttu-id="17078-113">False</span><span class="sxs-lookup"><span data-stu-id="17078-113">False</span></span> | <span data-ttu-id="17078-114">Le caractère est masqué (non visible).</span><span class="sxs-lookup"><span data-stu-id="17078-114">The character is hidden (not visible).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17078-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="17078-115">Remarks</span></span>

<span data-ttu-id="17078-116">Cette propriété indique si le frame du caractère est affiché.</span><span class="sxs-lookup"><span data-stu-id="17078-116">This property indicates whether the character's frame is being displayed.</span></span> <span data-ttu-id="17078-117">Cela ne signifie pas nécessairement qu’il y a une image à l’écran.</span><span class="sxs-lookup"><span data-stu-id="17078-117">It does not necessarily mean that there is an image on the screen.</span></span> <span data-ttu-id="17078-118">Par exemple, cette propriété retourne la **valeur true** même si le caractère est positionné en dehors de la zone d’affichage visible ou lorsque le frame de caractères actuel ne contient aucune image.</span><span class="sxs-lookup"><span data-stu-id="17078-118">For example, this property returns **True** even when the character is positioned off the visible display area or when the current character frame contains no images.</span></span> <span data-ttu-id="17078-119">Le paramètre de cette propriété s’applique à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="17078-119">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="17078-120">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="17078-120">This property is read-only.</span></span> <span data-ttu-id="17078-121">Pour rendre un caractère visible ou masqué, utilisez les méthodes d' [**affichage**](show-method.md) ou de [**masquage**](https://www.bing.com/search?q=**Hide**) .</span><span class="sxs-lookup"><span data-stu-id="17078-121">To make a character visible or hidden, use the [**Show**](show-method.md) or [**Hide**](https://www.bing.com/search?q=**Hide**) methods.</span></span>

 

 




