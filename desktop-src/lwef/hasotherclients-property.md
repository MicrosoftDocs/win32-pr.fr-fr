---
title: Propriété HasOtherClients
description: Propriété HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029240"
---
# <a name="hasotherclients-property"></a><span data-ttu-id="863c6-103">Propriété HasOtherClients</span><span class="sxs-lookup"><span data-stu-id="863c6-103">HasOtherClients Property</span></span>

<span data-ttu-id="863c6-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="863c6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="863c6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="863c6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="863c6-106">Retourne une valeur indiquant si le caractère spécifié est utilisé par d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="863c6-106">Returns whether the specified character is in use by other applications.</span></span>

</dd> <dt>

<span data-ttu-id="863c6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="863c6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="863c6-108">*agent*. **Caractères («***CharacterID***»). HasOtherClients**</span><span class="sxs-lookup"><span data-stu-id="863c6-108">*agent*.**Characters("***CharacterID***").HasOtherClients**</span></span>



| <span data-ttu-id="863c6-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="863c6-109">Value</span></span>     | <span data-ttu-id="863c6-110">Description</span><span class="sxs-lookup"><span data-stu-id="863c6-110">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="863c6-111">**True**</span><span class="sxs-lookup"><span data-stu-id="863c6-111">**True**</span></span>  | <span data-ttu-id="863c6-112">Le caractère comporte d’autres clients.</span><span class="sxs-lookup"><span data-stu-id="863c6-112">The character has other clients.</span></span>           |
| <span data-ttu-id="863c6-113">**False**</span><span class="sxs-lookup"><span data-stu-id="863c6-113">**False**</span></span> | <span data-ttu-id="863c6-114">Le caractère n’a pas d’autres clients.</span><span class="sxs-lookup"><span data-stu-id="863c6-114">The character does not have other clients.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="863c6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="863c6-115">Remarks</span></span>

<span data-ttu-id="863c6-116">Vous pouvez utiliser cette propriété pour déterminer si votre application est le seul ou dernier client du caractère, lorsque plusieurs applications partagent le même caractère (a chargé).</span><span class="sxs-lookup"><span data-stu-id="863c6-116">You can use this property to determine whether your application is the only or last client of the character, when more than one application is sharing (has loaded) the same character.</span></span>

 

 




