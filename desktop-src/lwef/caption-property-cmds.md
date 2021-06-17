---
title: Propriété Caption (objet collection Commands)
description: En savoir plus sur la propriété Caption de l’objet de collection Command. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34ae7bd6da1fc6cc60f882cc231af5730a1077e
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262051"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="d6508-104">Propriété Caption (objet collection Commands)</span><span class="sxs-lookup"><span data-stu-id="d6508-104">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="d6508-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d6508-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d6508-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="d6508-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d6508-107">Détermine le texte affiché pour un objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="d6508-107">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="d6508-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="d6508-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d6508-109">\*agent \***. Caractères («**_CharacterID_\*_»)._ \* [Chaîne Commands. Caption](caption-property.md) \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="d6508-109">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="d6508-110">Partie</span><span class="sxs-lookup"><span data-stu-id="d6508-110">Part</span></span>     | <span data-ttu-id="d6508-111">Description</span><span class="sxs-lookup"><span data-stu-id="d6508-111">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="d6508-112">*string*</span><span class="sxs-lookup"><span data-stu-id="d6508-112">*string*</span></span> | <span data-ttu-id="d6508-113">Expression de chaîne qui prend la valeur du texte affiché en tant que légende.</span><span class="sxs-lookup"><span data-stu-id="d6508-113">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6508-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6508-114">Remarks</span></span>

<span data-ttu-id="d6508-115">La définition de la propriété [**Caption**](caption-property.md) de votre collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) définit son mode d’affichage dans le menu contextuel du caractère lorsque sa propriété [**visible**](visible-property.md) a la valeur true et que votre application n’est pas le client d’entrée-actif.</span><span class="sxs-lookup"><span data-stu-id="d6508-115">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="d6508-116">Pour spécifier une touche d’accès (mnémonique non linéaire) pour votre **légende**, incluez un caractère perluète (&) avant ce caractère.</span><span class="sxs-lookup"><span data-stu-id="d6508-116">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="d6508-117">Si vous définissez des commandes pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) qui a une [**légende**](caption-property.md), vous définissez généralement une **légende** pour la collection de **commandes** associée.</span><span class="sxs-lookup"><span data-stu-id="d6508-117">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
