---
title: Propriété VoiceCaption (objet Command)
description: Propriété VoiceCaption
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1077c8d65a52bc8f0cfa329fdceb740e30e6784
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106511115"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="44a9e-103">Propriété VoiceCaption (objet Command)</span><span class="sxs-lookup"><span data-stu-id="44a9e-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="44a9e-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="44a9e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="44a9e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="44a9e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="44a9e-106">Définit ou retourne le texte affiché pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) dans la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="44a9e-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="44a9e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="44a9e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="44a9e-108">\*agents. \***caractères («**_CharacterID_*_»). Commandes («_*_nom_\*_»)._ \*  \[  =  *Chaîne* VoiceCaption\]</span><span class="sxs-lookup"><span data-stu-id="44a9e-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="44a9e-109">Partie</span><span class="sxs-lookup"><span data-stu-id="44a9e-109">Part</span></span>     | <span data-ttu-id="44a9e-110">Description</span><span class="sxs-lookup"><span data-stu-id="44a9e-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="44a9e-111">*string*</span><span class="sxs-lookup"><span data-stu-id="44a9e-111">*string*</span></span> | <span data-ttu-id="44a9e-112">Expression de chaîne qui prend la valeur du texte affiché.</span><span class="sxs-lookup"><span data-stu-id="44a9e-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44a9e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="44a9e-113">Remarks</span></span>

<span data-ttu-id="44a9e-114">Si vous définissez un objet de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](https://www.bing.com/search?q=**Commands**) et que vous définissez sa propriété [**Voice**](voice-property.md) , vous définissez en général également sa propriété [**VoiceCaption**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="44a9e-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="44a9e-115">Ce texte s’affiche dans la fenêtre commandes vocales lorsque votre application cliente est en entrée-active et que le caractère est visible.</span><span class="sxs-lookup"><span data-stu-id="44a9e-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="44a9e-116">Si cette propriété n’est pas définie, le paramètre de la propriété [**Caption**](caption-property.md) détermine le texte affiché.</span><span class="sxs-lookup"><span data-stu-id="44a9e-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="44a9e-117">Lorsque ni la propriété **VoiceCaption** ni la propriété **Caption** n’est définie, la commande n’apparaît pas dans la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="44a9e-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="44a9e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44a9e-118">See Also</span></span>

[<span data-ttu-id="44a9e-119">**Propriété Caption**</span><span class="sxs-lookup"><span data-stu-id="44a9e-119">**Caption property**</span></span>](caption-property.md)


 

 
