---
title: Width, propriété (objet Characters)
description: En savoir plus sur la propriété Width de l’objet Characters, qui retourne ou définit la largeur du cadre pour le caractère spécifié.
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395125"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="28d6f-103">Width, propriété (objet Characters)</span><span class="sxs-lookup"><span data-stu-id="28d6f-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="28d6f-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="28d6f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="28d6f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="28d6f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="28d6f-106">Retourne ou définit la largeur du cadre pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="28d6f-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="28d6f-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="28d6f-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="28d6f-108">\*agent \***. Caractères («**_CharacterID_\*_»)._ \*  \[ =  *Valeur* de largeur\]</span><span class="sxs-lookup"><span data-stu-id="28d6f-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="28d6f-109">Partie</span><span class="sxs-lookup"><span data-stu-id="28d6f-109">Part</span></span>    | <span data-ttu-id="28d6f-110">Description</span><span class="sxs-lookup"><span data-stu-id="28d6f-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="28d6f-111">*value*</span><span class="sxs-lookup"><span data-stu-id="28d6f-111">*value*</span></span> | <span data-ttu-id="28d6f-112">Entier long qui spécifie la largeur du cadre du caractère.</span><span class="sxs-lookup"><span data-stu-id="28d6f-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28d6f-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="28d6f-113">Remarks</span></span>

<span data-ttu-id="28d6f-114">La propriété [**Width**](width-property.md) est toujours exprimée en pixels.</span><span class="sxs-lookup"><span data-stu-id="28d6f-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="28d6f-115">Le paramètre de cette propriété s’applique à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="28d6f-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="28d6f-116">Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur les dimensions externes du cadre d’animation rectangulaire utilisé lorsque le caractère a été compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="28d6f-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




