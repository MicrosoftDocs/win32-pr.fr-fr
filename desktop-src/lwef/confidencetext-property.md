---
title: Propriété ConfidenceText
description: Propriété ConfidenceText
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381880"
---
# <a name="confidencetext-property"></a><span data-ttu-id="dc65c-103">Propriété ConfidenceText</span><span class="sxs-lookup"><span data-stu-id="dc65c-103">ConfidenceText Property</span></span>

<span data-ttu-id="dc65c-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc65c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="dc65c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="dc65c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="dc65c-106">Retourne ou définit le **ConfidenceText** du client qui apparaît dans l’info-bulle d’écoute.</span><span class="sxs-lookup"><span data-stu-id="dc65c-106">Returns or sets the client's **ConfidenceText** that appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="dc65c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="dc65c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="dc65c-108">\* agent ***. Caractères («*** CharacterID ***»). Commandes («*** name \***»)**.  \[ ConfidenceText  =  *chaîne*\]</span><span class="sxs-lookup"><span data-stu-id="dc65c-108">\*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.**ConfidenceText**\[ = *string*\]</span></span>



| <span data-ttu-id="dc65c-109">Partie</span><span class="sxs-lookup"><span data-stu-id="dc65c-109">Part</span></span>     | <span data-ttu-id="dc65c-110">Description</span><span class="sxs-lookup"><span data-stu-id="dc65c-110">Description</span></span>                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc65c-111">*string*</span><span class="sxs-lookup"><span data-stu-id="dc65c-111">*string*</span></span> | <span data-ttu-id="dc65c-112">Expression de chaîne qui prend la valeur du texte de **ConfidenceText** pour la [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="dc65c-112">A string expression that evaluates to the text for the **ConfidenceText** for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc65c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="dc65c-113">Remarks</span></span>

<span data-ttu-id="dc65c-114">Lorsque la valeur de confiance renvoyée pour la meilleure correspondance (UserInput. Confidence) ne dépasse pas le paramètre de [**confiance**](confidence-property.md) , le serveur affiche le texte fourni dans **ConfidenceText** dans le Conseil d’écoute.</span><span class="sxs-lookup"><span data-stu-id="dc65c-114">When the returned confidence value of the best match (UserInput.Confidence) does not exceed the [**Confidence**](confidence-property.md) setting, the server displays the text supplied in **ConfidenceText** in the Listening Tip.</span></span>

 

 