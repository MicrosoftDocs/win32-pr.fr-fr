---
title: Propriété VoiceCaption (objet Command)
description: En savoir plus sur la propriété VoiceCaption de l’objet Command, qui définit ou retourne le texte affiché pour l’objet Command dans la fenêtre commandes vocales.
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d700b5d29b4c493be7382d45de55f44e6d02646c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396164"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="51de1-103">Propriété VoiceCaption (objet Command)</span><span class="sxs-lookup"><span data-stu-id="51de1-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="51de1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51de1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="51de1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="51de1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="51de1-106">Définit ou retourne le texte affiché pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) dans la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="51de1-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="51de1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="51de1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="51de1-108">\*agents. \***caractères («**_CharacterID_*_»). Commandes («_*_nom_\*_»)._ \*  \[  =  *Chaîne* VoiceCaption\]</span><span class="sxs-lookup"><span data-stu-id="51de1-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="51de1-109">Partie</span><span class="sxs-lookup"><span data-stu-id="51de1-109">Part</span></span>     | <span data-ttu-id="51de1-110">Description</span><span class="sxs-lookup"><span data-stu-id="51de1-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="51de1-111">*string*</span><span class="sxs-lookup"><span data-stu-id="51de1-111">*string*</span></span> | <span data-ttu-id="51de1-112">Expression de chaîne qui prend la valeur du texte affiché.</span><span class="sxs-lookup"><span data-stu-id="51de1-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51de1-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="51de1-113">Remarks</span></span>

<span data-ttu-id="51de1-114">Si vous définissez un objet de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](https://www.bing.com/search?q=**Commands**) et que vous définissez sa propriété [**Voice**](voice-property.md) , vous définissez en général également sa propriété [**VoiceCaption**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="51de1-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="51de1-115">Ce texte s’affiche dans la fenêtre commandes vocales lorsque votre application cliente est en entrée-active et que le caractère est visible.</span><span class="sxs-lookup"><span data-stu-id="51de1-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="51de1-116">Si cette propriété n’est pas définie, le paramètre de la propriété [**Caption**](caption-property.md) détermine le texte affiché.</span><span class="sxs-lookup"><span data-stu-id="51de1-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="51de1-117">Lorsque ni la propriété **VoiceCaption** ni la propriété **Caption** n’est définie, la commande n’apparaît pas dans la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="51de1-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="51de1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51de1-118">See Also</span></span>

[<span data-ttu-id="51de1-119">**Propriété Caption**</span><span class="sxs-lookup"><span data-stu-id="51de1-119">**Caption property**</span></span>](caption-property.md)


 

 
