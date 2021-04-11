---
title: Visible, propriété (objet Commands)
description: Propriété visible
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383739"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="85df8-103">Visible, propriété (objet Commands)</span><span class="sxs-lookup"><span data-stu-id="85df8-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="85df8-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="85df8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="85df8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="85df8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="85df8-106">Retourne ou définit une valeur qui détermine si la légende de la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) s’affiche dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="85df8-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="85df8-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="85df8-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="85df8-108">\*agent \***. Caractères (**"\* CharacterID \*" \* *). Commands.* \*  \[  =  *valeur booléenne* visible\]</span><span class="sxs-lookup"><span data-stu-id="85df8-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="85df8-109">Partie</span><span class="sxs-lookup"><span data-stu-id="85df8-109">Part</span></span>      | <span data-ttu-id="85df8-110">Description</span><span class="sxs-lookup"><span data-stu-id="85df8-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85df8-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="85df8-111">*boolean*</span></span> | <span data-ttu-id="85df8-112">Expression booléenne spécifiant si votre objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) s’affiche dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="85df8-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="85df8-113">**True** La légende s’affiche.</span><span class="sxs-lookup"><span data-stu-id="85df8-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="85df8-114">**Valeur false** La légende n’apparaît pas.</span><span class="sxs-lookup"><span data-stu-id="85df8-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85df8-115">Notes</span><span class="sxs-lookup"><span data-stu-id="85df8-115">Remarks</span></span>

<span data-ttu-id="85df8-116">Pour que la légende apparaisse dans le menu contextuel du caractère lorsque votre application n’est pas le client d’entrée-actif, cette propriété doit avoir la valeur **true** et la propriété [**Caption**](caption-property.md) définie pour votre collection de commandes.</span><span class="sxs-lookup"><span data-stu-id="85df8-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="85df8-117">De plus, cette propriété doit avoir la valeur **true** pour que les commandes de votre collection s’affichent dans le menu contextuel lorsque votre application est en entrée active.</span><span class="sxs-lookup"><span data-stu-id="85df8-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

