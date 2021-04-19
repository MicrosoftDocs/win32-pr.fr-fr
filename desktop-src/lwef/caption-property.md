---
title: Propriété Caption (objet Command)
description: Propriété Caption
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106538603"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="f8542-103">Propriété Caption (objet Command)</span><span class="sxs-lookup"><span data-stu-id="f8542-103">Caption Property (Command Object)</span></span>

<span data-ttu-id="f8542-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f8542-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f8542-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="f8542-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f8542-106">Détermine le texte affiché pour une [**commande**](/windows/desktop/lwef/the-command-object) dans le menu contextuel du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="f8542-106">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="f8542-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="f8542-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f8542-108">\*agent \***. Caractères («**_CharacterID_*_»). Commandes («_*_nom_\*_»)._ \*  \[  =  *Chaîne* de légende\]</span><span class="sxs-lookup"><span data-stu-id="f8542-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="f8542-109">Partie</span><span class="sxs-lookup"><span data-stu-id="f8542-109">Part</span></span>     | <span data-ttu-id="f8542-110">Description</span><span class="sxs-lookup"><span data-stu-id="f8542-110">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8542-111">*string*</span><span class="sxs-lookup"><span data-stu-id="f8542-111">*string*</span></span> | <span data-ttu-id="f8542-112">Expression de chaîne qui prend la valeur du texte affiché en tant que légende de la **commande**.</span><span class="sxs-lookup"><span data-stu-id="f8542-112">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8542-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f8542-113">Remarks</span></span>

<span data-ttu-id="f8542-114">Pour spécifier une touche d’accès (mnémonique non linéaire) pour votre **légende**, incluez un caractère perluète (&) avant ce caractère.</span><span class="sxs-lookup"><span data-stu-id="f8542-114">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="f8542-115">Si vous ne définissez pas de **VoiceCaption** pour votre commande, votre paramètre de **légende** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f8542-115">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
