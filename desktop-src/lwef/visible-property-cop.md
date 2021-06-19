---
title: Visible, propriété (objet Command)
description: En savoir plus sur la propriété visible de l’objet Command, qui retourne ou définit si la commande est visible dans le menu contextuel du caractère.
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4efec1ad8a97d6412a560a81836273b93ebf2b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396244"
---
# <a name="visible-property-command-object"></a><span data-ttu-id="319fa-103">Visible, propriété (objet Command)</span><span class="sxs-lookup"><span data-stu-id="319fa-103">Visible Property (Command Object)</span></span>

<span data-ttu-id="319fa-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="319fa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="319fa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="319fa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="319fa-106">Retourne ou définit une valeur indiquant si la [**commande**](/windows/desktop/lwef/the-command-object) est visible dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="319fa-106">Returns or sets whether the [**Command**](/windows/desktop/lwef/the-command-object) is visible in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="319fa-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="319fa-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="319fa-108">\*agent \***. Caractères (**«\* CharacterID *»**). Commandes (**«* name \*» \* *).* \*  \[  =  *Valeur booléenne* visible\]</span><span class="sxs-lookup"><span data-stu-id="319fa-108">*agent\***.Characters(**"* CharacterID *"**).Commands(**"* name *"\*\*).Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="319fa-109">Partie</span><span class="sxs-lookup"><span data-stu-id="319fa-109">Part</span></span>      | <span data-ttu-id="319fa-110">Description</span><span class="sxs-lookup"><span data-stu-id="319fa-110">Description</span></span>                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="319fa-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="319fa-111">*boolean*</span></span> | <span data-ttu-id="319fa-112">Expression booléenne spécifiant si la légende de la [**commande**](/windows/desktop/lwef/the-command-object)s’affiche dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="319fa-112">A Boolean expression specifying whether the [**Command**](/windows/desktop/lwef/the-command-object)'s caption appears in the character's pop-up menu.</span></span><br/> <span data-ttu-id="319fa-113">**True** (valeur par défaut) la légende s’affiche.</span><span class="sxs-lookup"><span data-stu-id="319fa-113">**True** (Default) The caption appears.</span></span><br/> <span data-ttu-id="319fa-114">**Valeur false** La légende n’apparaît pas.</span><span class="sxs-lookup"><span data-stu-id="319fa-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="319fa-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="319fa-115">Remarks</span></span>

<span data-ttu-id="319fa-116">Affectez à cette propriété la **valeur false** lorsque vous souhaitez inclure une entrée vocale pour vos propres interfaces sans les faire apparaître dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="319fa-116">Set this property to **False** when you want to include voice input for your own interfaces without having them appear in the pop-up menu for the character.</span></span> <span data-ttu-id="319fa-117">Si vous définissez la propriété [**Caption**](caption-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) sur la chaîne vide (""), le texte de légende n’apparaît pas dans le menu contextuel (par exemple, une ligne vide), quel que soit son paramètre de propriété [**visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="319fa-117">If you set a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md) property to the empty string (""), the caption text will not appear in the pop-up menu (for example, as a blank line), regardless of its [**Visible**](visible-property.md) property setting.</span></span>

<span data-ttu-id="319fa-118">Le paramètre de propriété [**visible**](visible-property.md) de la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) parent d’un objet de [**commande**](/windows/desktop/lwef/the-command-object) n’affecte pas le paramètre de propriété **visible** de la **commande**.</span><span class="sxs-lookup"><span data-stu-id="319fa-118">The [**Visible**](visible-property.md) property setting of a [**Command**](/windows/desktop/lwef/the-command-object) object's parent [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection does not affect the **Visible** property setting of the **Command**.</span></span>

 

