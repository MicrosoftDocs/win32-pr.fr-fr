---
title: Propriété Top (objet Characters)
description: En savoir plus sur la propriété Top (objet Characters). Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396344"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="5cdd6-104">Propriété Top (objet Characters)</span><span class="sxs-lookup"><span data-stu-id="5cdd6-104">Top Property (Characters Object)</span></span>

<span data-ttu-id="5cdd6-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5cdd6-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5cdd6-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="5cdd6-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5cdd6-107">Retourne ou définit le bord supérieur du frame du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="5cdd6-107">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="5cdd6-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="5cdd6-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5cdd6-109">\*agent \***. Caractères («**_CharacterID_\*_»)._ \*  \[  =  *Valeur* supérieure\]</span><span class="sxs-lookup"><span data-stu-id="5cdd6-109">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="5cdd6-110">Partie</span><span class="sxs-lookup"><span data-stu-id="5cdd6-110">Part</span></span>    | <span data-ttu-id="5cdd6-111">Description</span><span class="sxs-lookup"><span data-stu-id="5cdd6-111">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="5cdd6-112">*value*</span><span class="sxs-lookup"><span data-stu-id="5cdd6-112">*value*</span></span> | <span data-ttu-id="5cdd6-113">Entier long qui spécifie le bord supérieur du caractère.</span><span class="sxs-lookup"><span data-stu-id="5cdd6-113">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cdd6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5cdd6-114">Remarks</span></span>

<span data-ttu-id="5cdd6-115">La propriété **Top** est toujours exprimée en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="5cdd6-115">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="5cdd6-116">Le paramètre de cette propriété s’applique à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="5cdd6-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="5cdd6-117">Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur les dimensions externes du cadre d’animation rectangulaire utilisé lorsque le caractère a été compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="5cdd6-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="5cdd6-118">Utilisez la méthode [**MoveTo**](moveto-method.md) pour modifier l’emplacement du caractère.</span><span class="sxs-lookup"><span data-stu-id="5cdd6-118">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="5cdd6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cdd6-119">See Also</span></span>

<span data-ttu-id="5cdd6-120">[**Propriété Left**](left-property.md), [ **méthode MoveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="5cdd6-120">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




