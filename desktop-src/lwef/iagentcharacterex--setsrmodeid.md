---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104462715"
---
# <a name="iagentcharacterexsetsrmodeid"></a><span data-ttu-id="8f337-103">IAgentCharacterEx::SetSRModeID</span><span class="sxs-lookup"><span data-stu-id="8f337-103">IAgentCharacterEx::SetSRModeID</span></span>

<span data-ttu-id="8f337-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8f337-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

<span data-ttu-id="8f337-105">Définit l’ID de mode du moteur de reconnaissance vocale défini pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="8f337-105">Sets the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="8f337-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8f337-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="8f337-107">bszModeID</span><span class="sxs-lookup"><span data-stu-id="8f337-107">bszModeID</span></span>

<span data-ttu-id="8f337-108">Paramètre de l’ID de mode du moteur de reconnaissance vocale pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="8f337-108">The mode ID setting of the speech recognition engine for the character.</span></span>

<span data-ttu-id="8f337-109">Ce paramètre définit le moteur pour l’entrée vocale d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="8f337-109">This setting sets the engine for a character's speech input.</span></span> <span data-ttu-id="8f337-110">L’ID de mode d’un moteur de reconnaissance vocale est le GUID défini par le fournisseur de reconnaissance vocale qui identifie de façon unique le mode du moteur (mis en forme à l’aide d’accolades et de tirets).</span><span class="sxs-lookup"><span data-stu-id="8f337-110">The mode ID for a speech recognition engine is the GUID defined by the speech vendor that uniquely identifies the engine's mode (formatted with braces and dashes).</span></span> <span data-ttu-id="8f337-111">Pour plus d’informations, consultez la [documentation du kit de développement logiciel (SDK) Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="8f337-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="8f337-112">Si vous spécifiez un ID de mode qui ne correspond pas au paramètre de langue du caractère, si l’utilisateur a désactivé la reconnaissance vocale (dans la feuille de propriétés de l’agent Microsoft) ou si le moteur n’est pas installé, cet appel échoue.</span><span class="sxs-lookup"><span data-stu-id="8f337-112">If you specify a mode ID that does not match the character's language setting, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or the engine is not installed, this call will fail.</span></span> <span data-ttu-id="8f337-113">Si vous ne définissez pas un ID de mode de moteur de reconnaissance vocale pour le caractère, le serveur définit celui qui correspond au paramètre de langue du caractère (à l’aide des interfaces de l’API Microsoft Speech).</span><span class="sxs-lookup"><span data-stu-id="8f337-113">If you do not set a speech recognition engine mode ID for the character, the server sets one that matches the character's language setting (using Microsoft Speech API interfaces).</span></span>

<span data-ttu-id="8f337-114">Lorsque l’entrée vocale est activée dans la feuille de propriétés de l’agent (options de caractères avancés), la définition de cette propriété chargera le moteur associé (s’il n’est pas déjà chargé) et démarrez les services vocaux.</span><span class="sxs-lookup"><span data-stu-id="8f337-114">When speech input is enabled in the Agent property sheet (Advanced Character Options), setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="8f337-115">Autrement dit, la clé d’écoute est disponible et l’info-bulle d’écoute est affichable.</span><span class="sxs-lookup"><span data-stu-id="8f337-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="8f337-116">(La clé d’écoute et l’info-bulle d’écoute sont activées uniquement si elles sont également activées dans les options de caractères avancés.) Toutefois, si vous interrogez la propriété alors que la reconnaissance vocale est désactivée, le serveur ne démarre pas les services vocaux.</span><span class="sxs-lookup"><span data-stu-id="8f337-116">(The Listening key and Listening tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="8f337-117">Cette propriété s’applique uniquement au client du caractère ; le paramètre ne reflète pas le paramètre pour d’autres clients du caractère ou d’autres caractères du client.</span><span class="sxs-lookup"><span data-stu-id="8f337-117">This property applies to only the client of the character; the setting does not reflect the setting for other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="8f337-118">La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech.</span><span class="sxs-lookup"><span data-stu-id="8f337-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="8f337-119">Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.</span><span class="sxs-lookup"><span data-stu-id="8f337-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f337-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f337-120">See Also</span></span>

[<span data-ttu-id="8f337-121">**IAgentCharacterEx::GetSRModeID**</span><span class="sxs-lookup"><span data-stu-id="8f337-121">**IAgentCharacterEx::GetSRModeID**</span></span>](iagentcharacterex--getsrmodeid.md)


 

 




