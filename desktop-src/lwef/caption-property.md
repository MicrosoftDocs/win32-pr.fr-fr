---
title: Propriété Caption (objet Command)
description: En savoir plus sur la propriété Caption de l’objet Command. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262551"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="23dbf-104">Propriété Caption (objet Command)</span><span class="sxs-lookup"><span data-stu-id="23dbf-104">Caption Property (Command Object)</span></span>

<span data-ttu-id="23dbf-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="23dbf-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="23dbf-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="23dbf-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="23dbf-107">Détermine le texte affiché pour une [**commande**](/windows/desktop/lwef/the-command-object) dans le menu contextuel du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="23dbf-107">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="23dbf-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="23dbf-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="23dbf-109">\*agent \***. Caractères («**_CharacterID_*_»). Commandes («_*_nom_\*_»)._ \*  \[  =  *Chaîne* de légende\]</span><span class="sxs-lookup"><span data-stu-id="23dbf-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="23dbf-110">Partie</span><span class="sxs-lookup"><span data-stu-id="23dbf-110">Part</span></span>     | <span data-ttu-id="23dbf-111">Description</span><span class="sxs-lookup"><span data-stu-id="23dbf-111">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="23dbf-112">*string*</span><span class="sxs-lookup"><span data-stu-id="23dbf-112">*string*</span></span> | <span data-ttu-id="23dbf-113">Expression de chaîne qui prend la valeur du texte affiché en tant que légende de la **commande**.</span><span class="sxs-lookup"><span data-stu-id="23dbf-113">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23dbf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="23dbf-114">Remarks</span></span>

<span data-ttu-id="23dbf-115">Pour spécifier une touche d’accès (mnémonique non linéaire) pour votre **légende**, incluez un caractère perluète (&) avant ce caractère.</span><span class="sxs-lookup"><span data-stu-id="23dbf-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="23dbf-116">Si vous ne définissez pas de **VoiceCaption** pour votre commande, votre paramètre de **légende** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="23dbf-116">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
