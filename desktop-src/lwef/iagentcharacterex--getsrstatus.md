---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029024"
---
# <a name="iagentcharacterexgetsrstatus"></a><span data-ttu-id="24fd8-103">IAgentCharacterEx::GetSRStatus</span><span class="sxs-lookup"><span data-stu-id="24fd8-103">IAgentCharacterEx::GetSRStatus</span></span>

<span data-ttu-id="24fd8-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="24fd8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

<span data-ttu-id="24fd8-105">Récupère l’état de la condition nécessaire pour prendre en charge l’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="24fd8-105">Retrieves the status of the condition necessary to support speech input.</span></span>

-   <span data-ttu-id="24fd8-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="24fd8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="24fd8-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="24fd8-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="24fd8-108">Adresse d’une variable qui reçoit l’une des valeurs suivantes pour le paramètre d’État :</span><span class="sxs-lookup"><span data-stu-id="24fd8-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="24fd8-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="24fd8-109">Value</span></span>                                                                               | <span data-ttu-id="24fd8-110">Description</span><span class="sxs-lookup"><span data-stu-id="24fd8-110">Description</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24fd8-111">État d’écoute **longue non signée const** **\_ \_ CANLISTEN = 0 ;**</span><span class="sxs-lookup"><span data-stu-id="24fd8-111">**const unsigned long** **LISTEN\_STATUS\_CANLISTEN = 0;**</span></span><br/>               | <span data-ttu-id="24fd8-112">Les conditions prennent en charge l’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="24fd8-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="24fd8-113">**const unsigned long** **Listen \_ Status \_ noaudio = 1 ;**</span><span class="sxs-lookup"><span data-stu-id="24fd8-113">**const unsigned long** **LISTEN\_STATUS\_NOAUDIO = 1;**</span></span><br/>                 | <span data-ttu-id="24fd8-114">Aucun périphérique d’entrée audio n’est disponible sur ce système.</span><span class="sxs-lookup"><span data-stu-id="24fd8-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="24fd8-115">(Notez que cela ne détecte pas si un microphone est installé ; il peut détecter uniquement si l’utilisateur dispose d’une carte son compatible avec un pilote opérationnel.)</span><span class="sxs-lookup"><span data-stu-id="24fd8-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="24fd8-116">État d’écoute **longue non signée const** **\_ \_ NOTTOPMOST = 2 ;**</span><span class="sxs-lookup"><span data-stu-id="24fd8-116">**const unsigned long** **LISTEN\_STATUS\_NOTTOPMOST = 2;**</span></span><br/>              | <span data-ttu-id="24fd8-117">Un autre client est le client actif de ce caractère, ou le caractère actuel n’est pas au premier plan.</span><span class="sxs-lookup"><span data-stu-id="24fd8-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="24fd8-118">État d’écoute **longue non signée const** **\_ \_ CANTOPENAUDIO = 3 ;**</span><span class="sxs-lookup"><span data-stu-id="24fd8-118">**const unsigned long** **LISTEN\_STATUS\_CANTOPENAUDIO = 3;**</span></span><br/>           | <span data-ttu-id="24fd8-119">Le canal d’entrée ou de sortie audio est actuellement occupé, mais une autre application utilise l’audio.</span><span class="sxs-lookup"><span data-stu-id="24fd8-119">The audio input or output channel is currently busy, some other application is using audio.</span></span>                                                                                                                                               |
| <span data-ttu-id="24fd8-120">État d’écoute **longue non signée const** **\_ \_ COULDNTINITIALIZESPEECH = 4 ;**</span><span class="sxs-lookup"><span data-stu-id="24fd8-120">**const unsigned long** **LISTEN\_STATUS\_COULDNTINITIALIZESPEECH = 4;**</span></span><br/> | <span data-ttu-id="24fd8-121">Une erreur non spécifiée s’est produite lors de l’initialisation du sous-système de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="24fd8-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="24fd8-122">Cela inclut la possibilité qu’aucun moteur vocal ne soit disponible correspondant au paramètre de langue du caractère.</span><span class="sxs-lookup"><span data-stu-id="24fd8-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="24fd8-123">État d’écoute **longue non signée const** **\_ \_ SPEECHDISABLED = 5 ;**</span><span class="sxs-lookup"><span data-stu-id="24fd8-123">**const unsigned long** **LISTEN\_STATUS\_SPEECHDISABLED = 5;**</span></span><br/>          | <span data-ttu-id="24fd8-124">L’utilisateur a désactivé l’entrée vocale dans la fenêtre Options de caractères avancés.</span><span class="sxs-lookup"><span data-stu-id="24fd8-124">The user has disabled speech input in the Advanced Character Options window.</span></span>                                                                                                                                                              |
| <span data-ttu-id="24fd8-125">erreur d’état d’écoute **longue non signée const** **\_ \_ = 6 ;**</span><span class="sxs-lookup"><span data-stu-id="24fd8-125">**const unsigned long** **LISTEN\_STATUS\_ERROR = 6;**</span></span><br/>                   | <span data-ttu-id="24fd8-126">Une erreur s’est produite lors de la vérification de l’État audio, mais la cause de l’erreur n’a pas été retournée par le système.</span><span class="sxs-lookup"><span data-stu-id="24fd8-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

<span data-ttu-id="24fd8-127">Cette fonction vous permet d’interroger si les conditions actuelles prennent en charge l’entrée de reconnaissance vocale, y compris l’état du périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="24fd8-127">This function enables you to query whether current conditions support speech recognition input, including the status of the audio device.</span></span> <span data-ttu-id="24fd8-128">Si votre application utilise la méthode [**IAgentCharacterEx :: Listen**](iagentcharacterex--listen.md) , vous pouvez utiliser cette fonction pour mieux garantir le bon fonctionnement de l’appel.</span><span class="sxs-lookup"><span data-stu-id="24fd8-128">If your application uses the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method, you can use this function to better ensure that the call will succeed.</span></span> <span data-ttu-id="24fd8-129">L’appel de cette méthode charge également le moteur de reconnaissance vocale s’il n’est pas déjà chargé.</span><span class="sxs-lookup"><span data-stu-id="24fd8-129">Calling this method also loads the speech engine if it is not already loaded.</span></span> <span data-ttu-id="24fd8-130">Toutefois, il n’active pas le mode d’écoute.</span><span class="sxs-lookup"><span data-stu-id="24fd8-130">However, it does not turn on Listening mode.</span></span>

<span data-ttu-id="24fd8-131">Lorsque l’entrée vocale est activée dans la feuille de propriétés de l’agent (options de caractères avancés), l’interrogation de l’état chargera le moteur associé (s’il n’est pas déjà chargé) et démarrez Speech services.</span><span class="sxs-lookup"><span data-stu-id="24fd8-131">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying the status will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="24fd8-132">Autrement dit, la clé d’écoute est disponible et l’info-bulle d’écoute est affichable.</span><span class="sxs-lookup"><span data-stu-id="24fd8-132">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="24fd8-133">(La clé d’écoute et l’info-bulle d’écoute sont activées uniquement si elles sont également activées dans les options de caractères avancés.) Toutefois, si vous interrogez la propriété alors que la reconnaissance vocale est désactivée, le serveur ne démarre pas les services vocaux.</span><span class="sxs-lookup"><span data-stu-id="24fd8-133">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="24fd8-134">Cette fonction retourne uniquement le paramètre de l’utilisation du caractère par l’application cliente ; le paramètre ne reflète pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="24fd8-134">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

 

 





