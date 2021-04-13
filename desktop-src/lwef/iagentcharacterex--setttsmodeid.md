---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34392e65fcb8f3a46db6251f01f59ad76aba278d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381613"
---
# <a name="iagentcharacterexsetttsmodeid"></a><span data-ttu-id="9e863-103">IAgentCharacterEx::SetTTSModeID</span><span class="sxs-lookup"><span data-stu-id="9e863-103">IAgentCharacterEx::SetTTSModeID</span></span>

<span data-ttu-id="9e863-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9e863-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

<span data-ttu-id="9e863-105">Définit l’ID de mode du jeu de moteurs TTS pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="9e863-105">Sets the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="9e863-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="9e863-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="9e863-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span><span class="sxs-lookup"><span data-stu-id="9e863-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="9e863-108">Paramètre d’ID de mode du moteur TTS pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="9e863-108">The mode ID setting of the TTS engine for the character.</span></span>

> [!Note]  
> <span data-ttu-id="9e863-109">**IAgentCharacterEx : SetTTSModeID** peut échouer si Speech.dll n’est pas installé et que le moteur que vous spécifiez ne correspond pas au paramètre de mode TTS compilé du caractère.</span><span class="sxs-lookup"><span data-stu-id="9e863-109">**IAgentCharacterEx:SetTTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

</dd> </dl>

<span data-ttu-id="9e863-110">Ce paramètre détermine le mode de moteur par défaut pour la sortie TTS orale d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="9e863-110">This setting determines the preferred engine mode for a character's spoken TTS output.</span></span> <span data-ttu-id="9e863-111">L’ID de mode pour un moteur TTS (conversion de texte par synthèse vocale) est le GUID défini par le fournisseur de reconnaissance vocale qui identifie de façon unique le mode du moteur (mis en forme à l’aide d’accolades et de tirets).</span><span class="sxs-lookup"><span data-stu-id="9e863-111">The mode ID for a TTS (text-to-speech) engine is the GUID defined by the speech vendor that uniquely identifies the mode of the engine (formatted with braces and dashes).</span></span> <span data-ttu-id="9e863-112">Pour plus d’informations, consultez la [documentation du kit de développement logiciel (SDK) Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e863-112">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="9e863-113">Si vous définissez un ID de mode TTS, il remplace la tentative de serveur pour qu’il corresponde à un moteur de reconnaissance vocale en fonction de l’ID de mode TTS compilé du caractère, de l’ID de langue système actuel et de l’ID de langue actuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="9e863-113">If you set a TTS mode ID, it overrides the server attempt to match a speech engine based on the character's compiled TTS mode ID, the current system language ID, and the character's current language ID.</span></span> <span data-ttu-id="9e863-114">Toutefois, si vous tentez de définir un ID de mode lorsque l’utilisateur a désactivé la sortie vocale dans la feuille de propriétés de l’agent Microsoft ou que le moteur associé n’est pas installé, cet appel échoue.</span><span class="sxs-lookup"><span data-stu-id="9e863-114">However, if you attempt to set a mode ID when the user has disabled speech output in the Microsoft Agent property sheet or when the associated engine is not installed, this call will fail.</span></span>

<span data-ttu-id="9e863-115">Si vous ne définissez pas un ID de mode de moteur TTS pour le caractère, le serveur définit un moteur qui correspond au paramètre de langue du caractère (à l’aide des interfaces de l’API Microsoft Speech).</span><span class="sxs-lookup"><span data-stu-id="9e863-115">If you do not set a TTS engine mode ID for the character, the server sets an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="9e863-116">La définition de cette propriété chargera le moteur associé s’il n’est pas déjà chargé.</span><span class="sxs-lookup"><span data-stu-id="9e863-116">Setting this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="9e863-117">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="9e863-117">This property applies to only your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="9e863-118">La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech.</span><span class="sxs-lookup"><span data-stu-id="9e863-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="9e863-119">Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.</span><span class="sxs-lookup"><span data-stu-id="9e863-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e863-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e863-120">See Also</span></span>

[<span data-ttu-id="9e863-121">**IAgentCharacterEx:GetTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="9e863-121">**IAgentCharacterEx:GetTTSModeID**</span></span>](iagentcharacterex--getttsmodeid.md)


 

 




