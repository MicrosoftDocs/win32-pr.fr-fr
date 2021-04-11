---
title: Méthode Listen
description: Méthode Listen
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031111"
---
# <a name="listen-method"></a><span data-ttu-id="72ddb-103">Méthode Listen</span><span class="sxs-lookup"><span data-stu-id="72ddb-103">Listen Method</span></span>

<span data-ttu-id="72ddb-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72ddb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="72ddb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="72ddb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="72ddb-106">Active le mode d’écoute (reconnaissance vocale) pour une période programmée.</span><span class="sxs-lookup"><span data-stu-id="72ddb-106">Turns on Listening mode (speech recognition) for a timed period.</span></span>

</dd> <dt>

<span data-ttu-id="72ddb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="72ddb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="72ddb-108">\*agent. ***Caractères \* \* \* \* ("*** CharacterID \* \* *").* \*  *État* d’écoute</span><span class="sxs-lookup"><span data-stu-id="72ddb-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Listen** *State*</span></span>



| <span data-ttu-id="72ddb-109">Partie</span><span class="sxs-lookup"><span data-stu-id="72ddb-109">Part</span></span>    | <span data-ttu-id="72ddb-110">Description</span><span class="sxs-lookup"><span data-stu-id="72ddb-110">Description</span></span>                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72ddb-111">*State*</span><span class="sxs-lookup"><span data-stu-id="72ddb-111">*State*</span></span> | <span data-ttu-id="72ddb-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="72ddb-112">Required.</span></span> <span data-ttu-id="72ddb-113">Valeur booléenne qui détermine s’il faut activer ou désactiver le mode d’écoute.</span><span class="sxs-lookup"><span data-stu-id="72ddb-113">A Boolean value that determines whether to turn Listening mode on or off.</span></span> <span data-ttu-id="72ddb-114">**True** Active le mode d’écoute.</span><span class="sxs-lookup"><span data-stu-id="72ddb-114">**True** Turns Listening mode on.</span></span> <br/> <span data-ttu-id="72ddb-115">**Valeur false** Désactive le mode d’écoute.</span><span class="sxs-lookup"><span data-stu-id="72ddb-115">**False** Turns Listening mode off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72ddb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="72ddb-116">Remarks</span></span>

<span data-ttu-id="72ddb-117">La définition de cette méthode sur **true** active le mode d’écoute (active la reconnaissance vocale) pendant une période de temps fixe (10 secondes).</span><span class="sxs-lookup"><span data-stu-id="72ddb-117">Setting this method to **True** enables Listening mode (turns on speech recognition) for a fixed period of time (10 seconds).</span></span> <span data-ttu-id="72ddb-118">Bien que vous ne puissiez pas définir la valeur du délai d’attente, vous pouvez désactiver le mode d’écoute avant l’expiration du délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="72ddb-118">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="72ddb-119">Si vous (ou un autre client) avez correctement défini le mode d’écoute sur et que vous tentez d’affecter à cette propriété la **valeur true** avant l’expiration du délai d’attente, la méthode réussit et réinitialise le délai d’attente. Toutefois, si le mode d’écoute est activé parce que l’utilisateur appuie sur la touche d’écoute, la méthode aboutit, mais le délai d’attente est ignoré et le mode d’écoute se termine en fonction de l’interaction de l’utilisateur avec la clé d’écoute.</span><span class="sxs-lookup"><span data-stu-id="72ddb-119">If you (or another client) successfully set Listening mode on and you attempt to set this property to **True** before the time-out expires, the method succeeds and resets the time-out. However, if the Listening mode is on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="72ddb-120">Cette méthode réussit uniquement lorsqu’elle est appelée par le client d’entrée-actif et si les services vocaux ont été démarrés.</span><span class="sxs-lookup"><span data-stu-id="72ddb-120">This method succeeds only when called by the input-active client and if speech services have been started.</span></span> <span data-ttu-id="72ddb-121">Pour vous assurer que les services de reconnaissance vocale ont été démarrés, interrogez ou définissez les [**SRModeID**](srmodeid-property.md) ou définissez le paramètre de [**voix**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object) avant d’appeler **Listen** , sinon la méthode échouera.</span><span class="sxs-lookup"><span data-stu-id="72ddb-121">To ensure that speech services have been started, query or set the [**SRModeID**](srmodeid-property.md) or set the [**Voice**](voice-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) before you call **Listen** otherwise the method will fail.</span></span> <span data-ttu-id="72ddb-122">Pour détecter la réussite de cette méthode, appelez-la en tant que fonction et elle renverra une valeur booléenne indiquant si la méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="72ddb-122">To detect the success of this method, call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



<span data-ttu-id="72ddb-123">La méthode échoue également si l’utilisateur appuie sur la touche d’écoute et que vous tentez de définir **Listen** sur **false**.</span><span class="sxs-lookup"><span data-stu-id="72ddb-123">The method also fails if the user is pressing the Listening key and you attempt to set **Listen** to **False**.</span></span> <span data-ttu-id="72ddb-124">Toutefois, si l’utilisateur a relâché la clé d’écoute et que le mode d’écoute n’a pas dépassé le délai d’attente, elle échoue.</span><span class="sxs-lookup"><span data-stu-id="72ddb-124">However, if the user has released the Listening key and Listening mode has not timed out, it will succeed.</span></span>

<span data-ttu-id="72ddb-125">**Listen** échoue également si aucun moteur vocal compatible n’est disponible et correspond au paramètre [**LanguageID**](languageid-property.md) du caractère, l’utilisateur a désactivé l’entrée vocale à l’aide de la feuille de propriétés de l’agent Microsoft ou le périphérique audio est occupé.</span><span class="sxs-lookup"><span data-stu-id="72ddb-125">**Listen** also fails if there is no compatible speech engine available that matches the character's [**LanguageID**](languageid-property.md) setting, the user has disabled speech input using the Microsoft Agent property sheet, or the audio device is busy.</span></span>

<span data-ttu-id="72ddb-126">Lorsque vous avez correctement défini cette méthode sur **true**, le serveur déclenche l’événement [**ListenStart**](listenstart-event.md) .</span><span class="sxs-lookup"><span data-stu-id="72ddb-126">When you successfully set this method to **True**, the server triggers the [**ListenStart**](listenstart-event.md) event.</span></span> <span data-ttu-id="72ddb-127">Le serveur envoie [**ListenComplete**](listencomplete-event.md) lorsque le délai d’attente du mode d’écoute se termine ou lorsque vous définissez **Listen** sur **false**.</span><span class="sxs-lookup"><span data-stu-id="72ddb-127">The server sends [**ListenComplete**](listencomplete-event.md) when the Listening mode time-out completes or when you set **Listen** to **False**.</span></span>

<span data-ttu-id="72ddb-128">Cette méthode n’appelle pas automatiquement [**Stop**](stop-method.md) et joue une animation d’état d’écoute comme le fait le serveur quand vous appuyez sur la touche d’écoute.</span><span class="sxs-lookup"><span data-stu-id="72ddb-128">This method does not automatically call [**Stop**](stop-method.md) and play a Listening state animation as the server does when the Listening key is pressed.</span></span> <span data-ttu-id="72ddb-129">Cela vous permet de déterminer s’il faut interrompre l’animation en cours à l’aide de l’animation [**ListenStart**](listenstart-event.md) en appelant **Stop** et en lisant votre propre animation appropriée.</span><span class="sxs-lookup"><span data-stu-id="72ddb-129">This enables you to determine whether to interrupt the current animation using the [**ListenStart**](listenstart-event.md) animation by calling **Stop** and playing your own appropriate animation.</span></span> <span data-ttu-id="72ddb-130">Toutefois, le serveur appelle **Stop** et exécute une animation d’État auditif lorsqu’un énoncé utilisateur est détecté.</span><span class="sxs-lookup"><span data-stu-id="72ddb-130">However, the server does call **Stop** and plays a Hearing state animation when a user utterance is detected.</span></span>

## <a name="see-also"></a><span data-ttu-id="72ddb-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72ddb-131">See Also</span></span>

<span data-ttu-id="72ddb-132">[**Propriété LanguageID**](languageid-property.md), [**événement ListenComplete**](listencomplete-event.md), [**événement ListenStart**](listenstart-event.md)</span><span class="sxs-lookup"><span data-stu-id="72ddb-132">[**LanguageID property**](languageid-property.md), [**ListenComplete event**](listencomplete-event.md), [**ListenStart event**](listenstart-event.md)</span></span>


 

