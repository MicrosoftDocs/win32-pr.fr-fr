---
title: Count, propriété
description: Count, propriété
ms.assetid: a0375aa9-495d-47be-a3f7-4d5987688555
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 630817a8370a071851216ab03d43493e672b3e0a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842166"
---
# <a name="count-property"></a><span data-ttu-id="7662b-103">Count, propriété</span><span class="sxs-lookup"><span data-stu-id="7662b-103">Count Property</span></span>

<span data-ttu-id="7662b-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7662b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7662b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="7662b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7662b-106">Retourne un entier long (propriété en lecture seule) qui spécifie le nombre d’objets [**Command**](/windows/desktop/lwef/the-command-object) dans la collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="7662b-106">Returns a Long integer (read-only property) that specifies the count of [**Command**](/windows/desktop/lwef/the-command-object) objects in the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="7662b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="7662b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7662b-108">*agent ***. Caractères («*** CharacterID \* \* * »). Commands. Count**</span><span class="sxs-lookup"><span data-stu-id="7662b-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Count*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7662b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="7662b-109">Remarks</span></span>

<span data-ttu-id="7662b-110">**Count** comprend uniquement le nombre d’objets de [**commande**](/windows/desktop/lwef/the-command-object) que vous définissez dans votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="7662b-110">**Count** includes only the number of [**Command**](/windows/desktop/lwef/the-command-object) objects you define in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="7662b-111">Le serveur ou d’autres entrées du client ne sont pas inclus.</span><span class="sxs-lookup"><span data-stu-id="7662b-111">Server or other client entries are not included.</span></span>

 

 