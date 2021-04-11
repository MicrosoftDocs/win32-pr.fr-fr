---
title: Propriété DefaultCommand
description: Propriété DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031165"
---
# <a name="defaultcommand-property"></a><span data-ttu-id="72d05-103">Propriété DefaultCommand</span><span class="sxs-lookup"><span data-stu-id="72d05-103">DefaultCommand Property</span></span>

<span data-ttu-id="72d05-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72d05-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="72d05-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="72d05-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="72d05-106">Retourne ou définit la commande par défaut de l’objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="72d05-106">Returns or sets the default command of the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span>

</dd> <dt>

<span data-ttu-id="72d05-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="72d05-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="72d05-108">Caractères agent. \*\* \*\* \*  \* **(«***CharacterID***»). Chaîne Commands. DefaultCommand** \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="72d05-108">*agent.\*\*\*Characters*\* **("***CharacterID***").Commands.DefaultCommand** \[ = *string*\]</span></span>



| <span data-ttu-id="72d05-109">Partie</span><span class="sxs-lookup"><span data-stu-id="72d05-109">Part</span></span>     | <span data-ttu-id="72d05-110">Description</span><span class="sxs-lookup"><span data-stu-id="72d05-110">Description</span></span>                                                                         |
|----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="72d05-111">*string*</span><span class="sxs-lookup"><span data-stu-id="72d05-111">*string*</span></span> | <span data-ttu-id="72d05-112">Valeur de chaîne identifiant le nom (ID) de la [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="72d05-112">A string value identifying the name (ID) of the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72d05-113">Notes</span><span class="sxs-lookup"><span data-stu-id="72d05-113">Remarks</span></span>

<span data-ttu-id="72d05-114">Cette propriété vous permet de définir une [**commande**](/windows/desktop/lwef/the-command-object) dans votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) comme commande par défaut, en la rendant en gras.</span><span class="sxs-lookup"><span data-stu-id="72d05-114">This property enables you to set a [**Command**](/windows/desktop/lwef/the-command-object) in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection as the default command, rendering it bold.</span></span> <span data-ttu-id="72d05-115">Cela ne modifie pas réellement les événements de gestion des commandes ou de double-clic.</span><span class="sxs-lookup"><span data-stu-id="72d05-115">This does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="72d05-116">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="72d05-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 