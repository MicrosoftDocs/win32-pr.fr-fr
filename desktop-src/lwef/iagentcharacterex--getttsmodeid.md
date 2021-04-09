---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030881"
---
# <a name="iagentcharacterexgetttsmodeid"></a><span data-ttu-id="fa6e1-103">IAgentCharacterEx::GetTTSModeID</span><span class="sxs-lookup"><span data-stu-id="fa6e1-103">IAgentCharacterEx::GetTTSModeID</span></span>

<span data-ttu-id="fa6e1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fa6e1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

<span data-ttu-id="fa6e1-105">Récupère l’ID de mode du jeu de moteurs TTS pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-105">Retrieves the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="fa6e1-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fa6e1-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span><span class="sxs-lookup"><span data-stu-id="fa6e1-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="fa6e1-108">Adresse d’un BSTR qui reçoit le paramètre de l’ID de mode du moteur TTS pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-108">Address of a BSTR that receives the mode ID setting of the TTS engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="fa6e1-109">Ce paramètre renvoie l’ID de mode de moteur TTS (conversion de texte par synthèse vocale) pour la sortie parlée d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-109">This setting returns the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="fa6e1-110">L’ID de mode d’un moteur TTS est une représentation sous forme de chaîne du GUID (mis en forme à l’aide d’accolades et de tirets) défini par le fournisseur vocal qui identifie de façon unique le moteur.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-110">The mode ID for a TTS engine is a string representation of the GUID (formatted with braces and dashes) defined by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="fa6e1-111">Pour plus d’informations, consultez la [documentation du kit de développement logiciel (SDK) Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="fa6e1-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="fa6e1-112">L’interrogation de cette propriété chargera le moteur associé s’il n’est pas déjà chargé.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-112">Querying this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="fa6e1-113">Si vous ne définissez pas un ID de mode de moteur TTS pour le caractère, le serveur tente de renvoyer un moteur qui correspond (à l’aide des interfaces de l’API Microsoft Speech) au paramètre TTS compilé du caractère et au paramètre de langue actuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-113">If you do not set a TTS engine mode ID for the character, the server attempts to return an engine that matches (using Microsoft Speech API interfaces) the character's compiled TTS setting and the character's current language setting.</span></span> <span data-ttu-id="fa6e1-114">Si elles sont différentes, le paramètre de langue du caractère remplace le paramètre de mode créé.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-114">If these are different, then the character's language setting overrides its authored mode setting.</span></span> <span data-ttu-id="fa6e1-115">Si vous n’avez pas défini le paramètre de langue du caractère, la langue du caractère est l’ID de langue par défaut de l’utilisateur, et le serveur tente la correspondance en fonction de cet ID de langue.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-115">If you have not set the character's language setting, the character's language is the user default language ID, and the server attempts the match based on that language ID.</span></span>

<span data-ttu-id="fa6e1-116">Cette fonction n’échoue pas si [**IAgentAudioObjectProperties :: GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-116">This function does not fail if the [**IAgentAudioObjectProperties::GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) returns **False**.</span></span>

<span data-ttu-id="fa6e1-117">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="fa6e1-118">La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="fa6e1-119">Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.</span><span class="sxs-lookup"><span data-stu-id="fa6e1-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa6e1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa6e1-120">See Also</span></span>

[<span data-ttu-id="fa6e1-121">**IAgentCharacterEx::SetTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="fa6e1-121">**IAgentCharacterEx::SetTTSModeID**</span></span>](iagentcharacterex--setttsmodeid.md)


 

 




