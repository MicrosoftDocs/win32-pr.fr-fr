---
title: Propriété Caption (objet collection Commands)
description: Propriété Caption
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010fe051568f71c4940b4bcf964f257ba9f52ca
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102688"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="6826d-103">Propriété Caption (objet collection Commands)</span><span class="sxs-lookup"><span data-stu-id="6826d-103">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="6826d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6826d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6826d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="6826d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6826d-106">Détermine le texte affiché pour un objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="6826d-106">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="6826d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="6826d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6826d-108">\*agent \***. Caractères («**_CharacterID_\*_»)._ \* [Chaîne Commands. Caption](caption-property.md) \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="6826d-108">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="6826d-109">Partie</span><span class="sxs-lookup"><span data-stu-id="6826d-109">Part</span></span>     | <span data-ttu-id="6826d-110">Description</span><span class="sxs-lookup"><span data-stu-id="6826d-110">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="6826d-111">*string*</span><span class="sxs-lookup"><span data-stu-id="6826d-111">*string*</span></span> | <span data-ttu-id="6826d-112">Expression de chaîne qui prend la valeur du texte affiché en tant que légende.</span><span class="sxs-lookup"><span data-stu-id="6826d-112">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6826d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6826d-113">Remarks</span></span>

<span data-ttu-id="6826d-114">La définition de la propriété [**Caption**](caption-property.md) de votre collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) définit son mode d’affichage dans le menu contextuel du caractère lorsque sa propriété [**visible**](visible-property.md) a la valeur true et que votre application n’est pas le client d’entrée-actif.</span><span class="sxs-lookup"><span data-stu-id="6826d-114">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="6826d-115">Pour spécifier une touche d’accès (mnémonique non linéaire) pour votre **légende**, incluez un caractère perluète (&) avant ce caractère.</span><span class="sxs-lookup"><span data-stu-id="6826d-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="6826d-116">Si vous définissez des commandes pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) qui a une [**légende**](caption-property.md), vous définissez généralement une **légende** pour la collection de **commandes** associée.</span><span class="sxs-lookup"><span data-stu-id="6826d-116">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
