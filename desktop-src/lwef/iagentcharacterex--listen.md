---
title: IAgentCharacterEx écouter
description: IAgentCharacterEx écouter
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310389"
---
# <a name="iagentcharacterexlisten"></a><span data-ttu-id="417ef-103">IAgentCharacterEx :: Listen</span><span class="sxs-lookup"><span data-stu-id="417ef-103">IAgentCharacterEx::Listen</span></span>

<span data-ttu-id="417ef-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="417ef-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

<span data-ttu-id="417ef-105">Active ou désactive le mode d’écoute (entrée de reconnaissance vocale).</span><span class="sxs-lookup"><span data-stu-id="417ef-105">Turns Listening mode (speech recognition input) on or off.</span></span>

-   <span data-ttu-id="417ef-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="417ef-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="417ef-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span><span class="sxs-lookup"><span data-stu-id="417ef-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span></span>
</dt> <dd>

<span data-ttu-id="417ef-108">Indicateur du mode d’écoute.</span><span class="sxs-lookup"><span data-stu-id="417ef-108">Listening mode flag.</span></span> <span data-ttu-id="417ef-109">Si ce paramètre a la **valeur true**, le mode d’écoute est activé ; Si la **valeur est false**, le mode d’écoute est désactivé.</span><span class="sxs-lookup"><span data-stu-id="417ef-109">If this parameter is **True**, the Listening mode is turned on; if **False**, Listening mode is turned off.</span></span>

</dd> </dl>

<span data-ttu-id="417ef-110">L’affectation de la **valeur true** à cette méthode active le mode d’écoute (active la reconnaissance vocale) pendant une période de temps fixe.</span><span class="sxs-lookup"><span data-stu-id="417ef-110">Setting this method to **True** enables the Listening mode (turns on speech recognition) for a fixed period of time.</span></span> <span data-ttu-id="417ef-111">Bien que vous ne puissiez pas définir la valeur du délai d’attente, vous pouvez désactiver le mode d’écoute avant l’expiration du délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="417ef-111">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="417ef-112">En outre, si le mode d’écoute est déjà activé parce que vous (ou un autre client) avez correctement défini la méthode sur **true** avant l’expiration du délai d’attente, la méthode réussit et réinitialise le délai d’attente. Toutefois, si le mode d’écoute est déjà activé parce que l’utilisateur appuie sur la touche d’écoute, la méthode aboutit, mais le délai d’attente est ignoré et le mode d’écoute se termine en fonction de l’interaction de l’utilisateur avec la clé d’écoute.</span><span class="sxs-lookup"><span data-stu-id="417ef-112">In addition, if the Listening mode is already on because you (or another client) successfully set the method to **True** before the time-out expires, the method succeeds and resets the time-out. However, if Listening mode is already on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="417ef-113">Cette méthode ne fonctionnera que lorsqu’elle est appelée par le client d’entrée-actif.</span><span class="sxs-lookup"><span data-stu-id="417ef-113">This method will succeed only when called by the input-active client.</span></span> <span data-ttu-id="417ef-114">Par conséquent, la méthode échoue si votre client n’est pas le client actif du premier caractère.</span><span class="sxs-lookup"><span data-stu-id="417ef-114">Therefore, the method will fail if your client is not the active client of the topmost character.</span></span> <span data-ttu-id="417ef-115">La méthode échouera également si vous tentez de définir la méthode sur **false** et que l’utilisateur appuie sur la touche d’écoute.</span><span class="sxs-lookup"><span data-stu-id="417ef-115">The method will also fail if you attempt to set the method to **False** and the user is pressing the Listening key.</span></span> <span data-ttu-id="417ef-116">Elle peut également échouer si aucun moteur vocal compatible ne correspond au paramètre ID de langue du caractère ou si l’utilisateur a désactivé l’entrée vocale à l’aide de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="417ef-116">It can also fail if there is no compatible speech engine available that matches the character's language ID setting or the user has disabled speech input using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="417ef-117">Toutefois, la méthode n’échouera pas si le périphérique audio est occupé.</span><span class="sxs-lookup"><span data-stu-id="417ef-117">However, the method will not fail if the audio device is busy.</span></span>

<span data-ttu-id="417ef-118">Lorsque vous avez correctement défini cette méthode sur **true**, le serveur déclenche l’événement [**IAgentNotifySinkEx :: ListeningState**](iagentnotifysinkex--listeningstate.md) .</span><span class="sxs-lookup"><span data-stu-id="417ef-118">When you successfully set this method to **True**, the server triggers the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event.</span></span> <span data-ttu-id="417ef-119">Le serveur envoie également **IAgentNotifySinkEx :: ListeningState** lorsque le délai d’attente du mode d’écoute est terminé ou lorsque vous définissez [**IAgentCharacterEx :: Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) sur **false**.</span><span class="sxs-lookup"><span data-stu-id="417ef-119">The server also sends **IAgentNotifySinkEx::ListeningState** when the Listening mode time-out completes or when you set [**IAgentCharacterEx::Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) to **False**.</span></span>

<span data-ttu-id="417ef-120">Cette méthode n’appelle pas automatiquement [**IAgentCharacter :: stopAll**](iagentcharacter--stopall.md) et joue une animation d’état d’écoute du caractère tel qu’il se produit lorsque l’utilisateur appuie sur la touche d’écoute.</span><span class="sxs-lookup"><span data-stu-id="417ef-120">This method does not automatically call [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md) and play a Listening state animation of the character as occurs when the user presses the Listening key.</span></span> <span data-ttu-id="417ef-121">Cela vous permet d’utiliser l’événement [**IAgentNotifySinkEx :: ListeningState**](iagentnotifysinkex--listeningstate.md) pour déterminer si vous souhaitez arrêter l’animation actuelle et lire votre propre animation appropriée.</span><span class="sxs-lookup"><span data-stu-id="417ef-121">This enables you to use the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event to determine whether you wish to stop the current animation and play your own appropriate animation.</span></span> <span data-ttu-id="417ef-122">Toutefois, une fois qu’un énoncé utilisateur est détecté, le serveur appelle automatiquement **IAgentCharacter :: stopAll** et émet une animation d’État auditif.</span><span class="sxs-lookup"><span data-stu-id="417ef-122">However, once a user utterance is detected, the server automatically calls **IAgentCharacter::StopAll** and plays a Hearing state animation.</span></span>

## <a name="see-also"></a><span data-ttu-id="417ef-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="417ef-123">See Also</span></span>

<span data-ttu-id="417ef-124">[**IAgentNotifySinkEx :: ListeningState**](iagentnotifysinkex--listeningstate.md), [ **IAgentSpeechInputProperties :: GetEnabled**](iagentspeechinputproperties--getenabled.md)</span><span class="sxs-lookup"><span data-stu-id="417ef-124">[**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md), [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)</span></span>


 

 




