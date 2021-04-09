---
title: Propriété VoiceCaption (objet Commands)
description: Propriété VoiceCaption
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739477"
---
# <a name="voicecaption-property-commands-object"></a><span data-ttu-id="8099a-103">Propriété VoiceCaption (objet Commands)</span><span class="sxs-lookup"><span data-stu-id="8099a-103">VoiceCaption Property (Commands Object)</span></span>

<span data-ttu-id="8099a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8099a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8099a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="8099a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8099a-106">Retourne ou définit le texte affiché pour l’objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) dans la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="8099a-106">Returns or sets the text displayed for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="8099a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="8099a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8099a-108">\*agents. \***caractères («**_CharacterID_\*_»). Chaîne Commands. VoiceCaption_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="8099a-108">*agent.\***Characters("**_CharacterID_*_").Commands.VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="8099a-109">Partie</span><span class="sxs-lookup"><span data-stu-id="8099a-109">Part</span></span>     | <span data-ttu-id="8099a-110">Description</span><span class="sxs-lookup"><span data-stu-id="8099a-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="8099a-111">*string*</span><span class="sxs-lookup"><span data-stu-id="8099a-111">*string*</span></span> | <span data-ttu-id="8099a-112">Expression de chaîne qui prend la valeur du texte affiché.</span><span class="sxs-lookup"><span data-stu-id="8099a-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8099a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8099a-113">Remarks</span></span>

<span data-ttu-id="8099a-114">Si vous définissez la propriété [**Voice**](voice-property.md) de votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) , vous définissez en général également sa propriété **VoiceCaption** .</span><span class="sxs-lookup"><span data-stu-id="8099a-114">If you set the [**Voice**](voice-property.md) property of your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection, you will typically also set its **VoiceCaption** property.</span></span> <span data-ttu-id="8099a-115">Le paramètre de texte **VoiceCaption** s’affiche dans la fenêtre commandes vocales lorsque votre application cliente est en entrée-active et que le caractère est visible.</span><span class="sxs-lookup"><span data-stu-id="8099a-115">The **VoiceCaption** text setting appears in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="8099a-116">Si cette propriété n’est pas définie, le paramètre de la propriété [**Caption**](caption-property.md) de la collection **Commands** détermine le texte affiché.</span><span class="sxs-lookup"><span data-stu-id="8099a-116">If this property is not set, the setting for the **Commands** collection's [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="8099a-117">Lorsque ni la propriété **VoiceCaption** ni **Caption** n’est définie, les commandes de la collection s’affichent dans la fenêtre commandes vocales sous « (commande non définie) » lorsque votre application cliente devient entrée-active.</span><span class="sxs-lookup"><span data-stu-id="8099a-117">When neither the **VoiceCaption** or **Caption** property is set, then commands in the collection appear in the Voice Commands Window under "(undefined command)" when your client application becomes input-active.</span></span>

<span data-ttu-id="8099a-118">Le paramètre **VoiceCaption** détermine également le texte affiché dans l’info-bulle d’écoute pour indiquer les commandes que le caractère écoute.</span><span class="sxs-lookup"><span data-stu-id="8099a-118">The **VoiceCaption** setting also determines the text displayed in the Listening Tip to indicate the commands for which the character listens.</span></span>

## <a name="see-also"></a><span data-ttu-id="8099a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8099a-119">See Also</span></span>

[<span data-ttu-id="8099a-120">Propriété Caption</span><span class="sxs-lookup"><span data-stu-id="8099a-120">Caption property</span></span>](caption-property.md)


 

 
