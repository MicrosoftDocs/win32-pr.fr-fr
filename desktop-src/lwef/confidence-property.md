---
title: Propriété confidence
description: Propriété confidence
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381817"
---
# <a name="confidence-property"></a><span data-ttu-id="a6a5d-103">Propriété confidence</span><span class="sxs-lookup"><span data-stu-id="a6a5d-103">Confidence Property</span></span>

<span data-ttu-id="a6a5d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a6a5d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a6a5d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="a6a5d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a6a5d-106">Retourne ou définit une valeur indiquant si la **confiance** du client s’affiche dans l’info-bulle d’écoute.</span><span class="sxs-lookup"><span data-stu-id="a6a5d-106">Returns or sets whether the client's **Confidence** appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="a6a5d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="a6a5d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a6a5d-108">\*agent ***. Caractères («*** CharacterID ***»). Commandes («*** name \***»)**. \* \*\* \*  \[  =  *numéro* de confiance\]</span><span class="sxs-lookup"><span data-stu-id="a6a5d-108">*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.\*\*Confidence*\* \[ = *Number*\]</span></span>



| <span data-ttu-id="a6a5d-109">Partie</span><span class="sxs-lookup"><span data-stu-id="a6a5d-109">Part</span></span>     | <span data-ttu-id="a6a5d-110">Description</span><span class="sxs-lookup"><span data-stu-id="a6a5d-110">Description</span></span>                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a5d-111">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="a6a5d-111">*Number*</span></span> | <span data-ttu-id="a6a5d-112">Expression numérique qui prend la valeur d’un entier long qui identifie la valeur de confiance de la [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="a6a5d-112">A numeric expression that evaluates to a Long integer that identifies confidence value for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6a5d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a6a5d-113">Remarks</span></span>

<span data-ttu-id="a6a5d-114">Si la valeur de confiance renvoyée pour la meilleure correspondance (UserInput. Confidence) ne dépasse pas la valeur que vous définissez pour la propriété **confidence** , le texte fourni dans [**ConfidenceText**](confidencetext-property.md) est affiché dans le Conseil d’écoute.</span><span class="sxs-lookup"><span data-stu-id="a6a5d-114">If the returned confidence value of the best match (UserInput.Confidence) does not exceed value you set for the **Confidence** property, the text supplied in [**ConfidenceText**](confidencetext-property.md) is displayed in the Listening Tip.</span></span>

 

 