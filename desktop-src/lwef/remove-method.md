---
title: Remove (méthode)
description: Remove (méthode)
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7fc80954a1ffe218ba38405a551e5f000dc76
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315137"
---
# <a name="remove-method"></a><span data-ttu-id="ebcba-103">Remove (méthode)</span><span class="sxs-lookup"><span data-stu-id="ebcba-103">Remove Method</span></span>

<span data-ttu-id="ebcba-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ebcba-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ebcba-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="ebcba-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ebcba-106">Supprime un objet [**Command**](/windows/desktop/lwef/the-command-object) de la collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="ebcba-106">Removes a [**Command**](/windows/desktop/lwef/the-command-object) object from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="ebcba-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="ebcba-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ebcba-108">*agent ***. Caractères («*** CharacterID ***»). Commands. Remove*** Name*</span><span class="sxs-lookup"><span data-stu-id="ebcba-108">*agent ***.Characters ("*** CharacterID ***").Commands.Remove*** Name*</span></span>



| <span data-ttu-id="ebcba-109">Partie</span><span class="sxs-lookup"><span data-stu-id="ebcba-109">Part</span></span>   | <span data-ttu-id="ebcba-110">Description</span><span class="sxs-lookup"><span data-stu-id="ebcba-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="ebcba-111">*Nom*</span><span class="sxs-lookup"><span data-stu-id="ebcba-111">*Name*</span></span> | <span data-ttu-id="ebcba-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ebcba-112">Required.</span></span> <span data-ttu-id="ebcba-113">Valeur de chaîne correspondant à l’ID de la commande.</span><span class="sxs-lookup"><span data-stu-id="ebcba-113">A string value corresponding to the ID for the command.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebcba-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ebcba-114">Remarks</span></span>

<span data-ttu-id="ebcba-115">Lorsqu’un objet [**Command**](/windows/desktop/lwef/the-command-object) est supprimé de la collection, il n’apparaît plus lorsque le menu contextuel du caractère s’affiche ou dans la fenêtre commandes lorsque votre application cliente est en entrée active.</span><span class="sxs-lookup"><span data-stu-id="ebcba-115">When a [**Command**](/windows/desktop/lwef/the-command-object) object is removed from the collection, it no longer appears when the character's pop-up menu is displayed or in the Commands Window when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="ebcba-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebcba-116">See Also</span></span>

[<span data-ttu-id="ebcba-117">**RemoveAll, méthode**</span><span class="sxs-lookup"><span data-stu-id="ebcba-117">**RemoveAll method**</span></span>](removeall-method.md)


 

 