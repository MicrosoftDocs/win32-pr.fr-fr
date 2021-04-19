---
title: Propriété Top (objet Characters)
description: Top, propriété
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef724c7052ad1d9ba5cb51ea46ccd7647723ed32
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509694"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="a8d29-103">Propriété Top (objet Characters)</span><span class="sxs-lookup"><span data-stu-id="a8d29-103">Top Property (Characters Object)</span></span>

<span data-ttu-id="a8d29-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a8d29-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a8d29-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="a8d29-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a8d29-106">Retourne ou définit le bord supérieur du frame du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="a8d29-106">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="a8d29-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="a8d29-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a8d29-108">\*agent \***. Caractères («**_CharacterID_\*_»)._ \*  \[  =  *Valeur* supérieure\]</span><span class="sxs-lookup"><span data-stu-id="a8d29-108">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="a8d29-109">Partie</span><span class="sxs-lookup"><span data-stu-id="a8d29-109">Part</span></span>    | <span data-ttu-id="a8d29-110">Description</span><span class="sxs-lookup"><span data-stu-id="a8d29-110">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="a8d29-111">*value*</span><span class="sxs-lookup"><span data-stu-id="a8d29-111">*value*</span></span> | <span data-ttu-id="a8d29-112">Entier long qui spécifie le bord supérieur du caractère.</span><span class="sxs-lookup"><span data-stu-id="a8d29-112">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8d29-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a8d29-113">Remarks</span></span>

<span data-ttu-id="a8d29-114">La propriété **Top** est toujours exprimée en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="a8d29-114">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="a8d29-115">Le paramètre de cette propriété s’applique à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="a8d29-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="a8d29-116">Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur les dimensions externes du cadre d’animation rectangulaire utilisé lorsque le caractère a été compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a8d29-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="a8d29-117">Utilisez la méthode [**MoveTo**](moveto-method.md) pour modifier l’emplacement du caractère.</span><span class="sxs-lookup"><span data-stu-id="a8d29-117">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8d29-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8d29-118">See Also</span></span>

<span data-ttu-id="a8d29-119">[**Propriété Left**](left-property.md), [ **méthode MoveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="a8d29-119">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




