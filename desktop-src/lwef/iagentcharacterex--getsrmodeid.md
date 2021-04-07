---
title: IAgentCharacterEx GetSRModeID
description: IAgentCharacterEx GetSRModeID
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723811"
---
# <a name="iagentcharacterexgetsrmodeid"></a><span data-ttu-id="a5aa1-103">IAgentCharacterEx::GetSRModeID</span><span class="sxs-lookup"><span data-stu-id="a5aa1-103">IAgentCharacterEx::GetSRModeID</span></span>

<span data-ttu-id="a5aa1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a5aa1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

<span data-ttu-id="a5aa1-105">Récupère l’ID de mode du moteur de reconnaissance vocale défini pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="a5aa1-105">Retrieves the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="a5aa1-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a5aa1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a5aa1-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span><span class="sxs-lookup"><span data-stu-id="a5aa1-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="a5aa1-108">Adresse d’un BSTR qui reçoit le paramètre de l’ID de mode du moteur de reconnaissance vocale pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="a5aa1-108">Address of a BSTR that receives the mode ID setting of the speech recognition engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="a5aa1-109">Ce paramètre retourne le jeu de moteurs pour l’entrée vocale d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="a5aa1-109">This setting returns the engine set for a character's speech input.</span></span> <span data-ttu-id="a5aa1-110">L’ID de mode d’un moteur de reconnaissance vocale est une représentation sous forme de chaîne du GUID (mis en forme à l’aide d’accolades et de tirets) par le fournisseur de reconnaissance vocale qui identifie le moteur de manière unique.</span><span class="sxs-lookup"><span data-stu-id="a5aa1-110">The mode ID for a speech recognition engine is a string representation of the GUID (formatted with braces and dashes) by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="a5aa1-111">Pour plus d’informations, consultez la [documentation du kit de développement logiciel (SDK) Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="a5aa1-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="a5aa1-112">Si vous ne définissez pas un ID de mode de moteur de reconnaissance vocale pour le caractère, le serveur retourne un moteur qui correspond au paramètre de langue du caractère (à l’aide des interfaces de l’API Microsoft Speech).</span><span class="sxs-lookup"><span data-stu-id="a5aa1-112">If you do not set a speech recognition engine mode ID for the character, the server returns an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="a5aa1-113">Si aucun moteur de reconnaissance vocale correspondant n’est disponible pour le caractère, le serveur retourne une chaîne null (vide).</span><span class="sxs-lookup"><span data-stu-id="a5aa1-113">If there is no matching speech recognition engine available for the character, the server returns a null (empty) string.</span></span>

<span data-ttu-id="a5aa1-114">Lorsque l’entrée vocale est activée (dans la fenêtre Options de caractères avancés), l’interrogation ou la définition de cette propriété chargera le moteur associé (s’il n’est pas déjà chargé) et démarrera les services de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="a5aa1-114">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="a5aa1-115">Autrement dit, la clé d’écoute est disponible et l’info-bulle d’écoute est affichable.</span><span class="sxs-lookup"><span data-stu-id="a5aa1-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="a5aa1-116">(La clé d’écoute et l’info-bulle d’écoute sont activées uniquement si elles sont également activées dans les options de caractères avancés.) Toutefois, si vous interrogez la propriété alors que la reconnaissance vocale est désactivée, le serveur ne démarre pas les services vocaux et retourne une chaîne null (chaîne vide).</span><span class="sxs-lookup"><span data-stu-id="a5aa1-116">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services and it returns a null string (empty string).</span></span>

<span data-ttu-id="a5aa1-117">Cette fonction retourne uniquement le paramètre de l’utilisation du caractère par l’application cliente ; le paramètre ne reflète pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="a5aa1-117">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="a5aa1-118">Cette fonction n’échoue pas si [**IAgentSpeechInputProperties :: GetEnabled**](iagentspeechinputproperties--getenabled.md) retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="a5aa1-118">This function does not fail if the [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**.</span></span>

<span data-ttu-id="a5aa1-119">La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech.</span><span class="sxs-lookup"><span data-stu-id="a5aa1-119">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="a5aa1-120">Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.</span><span class="sxs-lookup"><span data-stu-id="a5aa1-120">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5aa1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5aa1-121">See Also</span></span>

[<span data-ttu-id="a5aa1-122">**IAgentCharacterEx::SetSRModeID**</span><span class="sxs-lookup"><span data-stu-id="a5aa1-122">**IAgentCharacterEx::SetSRModeID**</span></span>](iagentcharacterex--setsrmodeid.md)


 

 




