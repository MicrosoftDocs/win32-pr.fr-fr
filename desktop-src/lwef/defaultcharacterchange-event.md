---
title: Événement DefaultCharacterChange
description: Événement DefaultCharacterChange
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380136"
---
# <a name="defaultcharacterchange-event"></a><span data-ttu-id="5aac3-103">Événement DefaultCharacterChange</span><span class="sxs-lookup"><span data-stu-id="5aac3-103">DefaultCharacterChange Event</span></span>

<span data-ttu-id="5aac3-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5aac3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5aac3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="5aac3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5aac3-106">Se produit lorsque l’utilisateur modifie le caractère par défaut.</span><span class="sxs-lookup"><span data-stu-id="5aac3-106">Occurs when the user changes the default character.</span></span>

</dd> <dt>

<span data-ttu-id="5aac3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="5aac3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5aac3-108">**Sous** - *agent. \* \* \* DefaultCharacterChange* \*  **(GUID ByVal** \*\* \* *)*\*</span><span class="sxs-lookup"><span data-stu-id="5aac3-108">**Sub** *agent.\*\*\*DefaultCharacterChange*\* **(ByVal** *GUID\*\*\*)*\*</span></span>



| <span data-ttu-id="5aac3-109">Partie</span><span class="sxs-lookup"><span data-stu-id="5aac3-109">Part</span></span>   | <span data-ttu-id="5aac3-110">Description</span><span class="sxs-lookup"><span data-stu-id="5aac3-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="5aac3-111">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5aac3-111">*GUID*</span></span> | <span data-ttu-id="5aac3-112">Retourne l’identificateur unique du caractère.</span><span class="sxs-lookup"><span data-stu-id="5aac3-112">Returns the unique identifier for the character.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="5aac3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5aac3-113">Remarks</span></span>

<span data-ttu-id="5aac3-114">Cet événement indique que l’utilisateur a modifié le caractère affecté comme caractère par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5aac3-114">This event indicates when the user has changed the character assigned as the user's default character.</span></span> <span data-ttu-id="5aac3-115">Le serveur l’envoie uniquement aux clients qui ont chargé le caractère par défaut.</span><span class="sxs-lookup"><span data-stu-id="5aac3-115">The server sends this only to clients that have loaded the default character.</span></span>

<span data-ttu-id="5aac3-116">Lorsque le nouveau caractère apparaît, il suppose la même taille que toute instance déjà chargée du caractère ou le caractère par défaut précédent (dans cet ordre).</span><span class="sxs-lookup"><span data-stu-id="5aac3-116">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

### <a name="see-also"></a><span data-ttu-id="5aac3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5aac3-117">See Also</span></span>

<span data-ttu-id="5aac3-118">[**Méthode ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md), [ **méthode Load**](load-method.md)</span><span class="sxs-lookup"><span data-stu-id="5aac3-118">[**ShowDefaultCharacterProperties method**](showdefaultcharacterproperties-method.md), [**Load method**](load-method.md)</span></span>


 

 




