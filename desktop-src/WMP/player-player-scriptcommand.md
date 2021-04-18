---
title: Événement Player. commande
description: L’événement commande se produit lors de la réception d’une commande ou d’une URL synchronisée. | Événement Player. commande
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- Événement commande lecteur Windows Media
- Événement commande lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement commande
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9ca7ec22694956e1d91d055e8db057a91ecca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533329"
---
# <a name="playerscriptcommand-event"></a><span data-ttu-id="5a2d9-107">Événement Player. commande</span><span class="sxs-lookup"><span data-stu-id="5a2d9-107">Player.ScriptCommand event</span></span>

<span data-ttu-id="5a2d9-108">L’événement **commande** se produit lors de la réception d’une commande ou d’une URL synchronisée.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-108">The **ScriptCommand** event occurs when a synchronized command or URL is received.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a2d9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a2d9-109">Syntax</span></span>


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="5a2d9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a2d9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a2d9-111">*scType*</span><span class="sxs-lookup"><span data-stu-id="5a2d9-111">*scType*</span></span> 
</dt> <dd>

<span data-ttu-id="5a2d9-112">Chaîne spécifiant le type de commande de script.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-112">String specifying the type of script command.</span></span>

</dd> <dt>

<span data-ttu-id="5a2d9-113">*Paramètre*</span><span class="sxs-lookup"><span data-stu-id="5a2d9-113">*Param*</span></span> 
</dt> <dd>

<span data-ttu-id="5a2d9-114">**Chaîne** spécifiant la commande de script.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-114">**String** specifying the script command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a2d9-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a2d9-115">Return value</span></span>

<span data-ttu-id="5a2d9-116">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a2d9-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5a2d9-117">Remarks</span></span>

<span data-ttu-id="5a2d9-118">Les commandes peuvent être incorporées parmi les sons et les images d’un fichier ou d’un flux Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-118">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="5a2d9-119">Les commandes sont une paire de chaînes Unicode associées à une heure désignée dans le flux.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-119">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="5a2d9-120">Lorsque le flux atteint l’heure associée à la commande, le contrôle du lecteur Windows Media envoie un événement **commande** avec deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-120">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="5a2d9-121">Un paramètre spécifie le type de commande en cours d’envoi, tandis que l’autre paramètre spécifie la commande.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-121">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="5a2d9-122">Le type de paramètre est utilisé pour déterminer la façon dont le paramètre de commande est traité.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-122">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="5a2d9-123">Tout type de commande peut être incorporé dans un fichier ou un flux à gérer par l’événement **commande** .</span><span class="sxs-lookup"><span data-stu-id="5a2d9-123">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="5a2d9-124">Le tableau suivant répertorie les types de commande de script qui sont traités automatiquement par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-124">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="5a2d9-125">Type</span><span class="sxs-lookup"><span data-stu-id="5a2d9-125">Type</span></span>                   | <span data-ttu-id="5a2d9-126">Description</span><span class="sxs-lookup"><span data-stu-id="5a2d9-126">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2d9-127">CAPTION</span><span class="sxs-lookup"><span data-stu-id="5a2d9-127">CAPTION</span></span>                | <span data-ttu-id="5a2d9-128">Le contrôle affiche le texte associé dans la balise DIV spécifiée par *ClosedCaption*. **captioningID**.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-128">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="5a2d9-129">ÉVÉNEMENT</span><span class="sxs-lookup"><span data-stu-id="5a2d9-129">EVENT</span></span>                  | <span data-ttu-id="5a2d9-130">Indique au contrôle d’exécuter les instructions définies pour l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-130">Tells the control to execute instructions defined for the specified event.</span></span>                                                                                          |
| <span data-ttu-id="5a2d9-131">EXTENSION</span><span class="sxs-lookup"><span data-stu-id="5a2d9-131">FILENAME</span></span>               | <span data-ttu-id="5a2d9-132">Le contrôle réinitialise sa propriété **URL** , tente d’ouvrir le fichier spécifié et commence à lire immédiatement le nouveau flux.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-132">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="5a2d9-133">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="5a2d9-133">OPENEVENT</span></span>              | <span data-ttu-id="5a2d9-134">Met en mémoire tampon la commande de type d’événement associée pour l’exécution en temps opportun du script d’événement.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-134">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="5a2d9-135">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="5a2d9-135">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="5a2d9-136">Le paramètre *param* contient le texte Lyric synchronisé.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-136">The *Param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="5a2d9-137">Le lecteur Windows Media affiche le texte Lyric dans la zone de légende fermée de la fonctionnalité de **lecture** en cours.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-137">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="5a2d9-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="5a2d9-138">TEXT</span></span>                   | <span data-ttu-id="5a2d9-139">Le contrôle affiche le texte associé dans la balise DIV spécifiée par *ClosedCaption*. **captioningID**.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-139">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="5a2d9-140">URL</span><span class="sxs-lookup"><span data-stu-id="5a2d9-140">URL</span></span>                    | <span data-ttu-id="5a2d9-141">Le contrôle ouvre automatiquement l’URL spécifiée à l’aide du navigateur Internet par défaut si les *paramètres*. la propriété **invokeURLs** a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-141">The control automatically opens the URL specified using the default Internet browser if the *Settings*.**invokeURLs** property is set to true.</span></span>                      |



 

<span data-ttu-id="5a2d9-142">Vous pouvez incorporer n’importe quel autre type de commande tant que vous fournissez du code réciproque pour gérer la commande.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-142">You can embed any other type of command as long as you provide reciprocal code to handle the command.</span></span> <span data-ttu-id="5a2d9-143">Bien que les commandes inconnues soient ignorées par le contrôle du lecteur Windows Media, elles sont toujours transmises à l’événement **commande** .</span><span class="sxs-lookup"><span data-stu-id="5a2d9-143">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="5a2d9-144">Les commandes d’URL reçues par le contrôle du lecteur Windows Media sont automatiquement appelées dans votre navigateur Web par défaut, si les *paramètres*. la propriété **invokeURLs** a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the *Settings*.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="5a2d9-145">Vous pouvez utiliser les *paramètres*. propriété **defaultFrame** pour spécifier le frame cible dans lequel la page Web s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-145">You can use the *Settings*.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="5a2d9-146">L’URL envoyée au lecteur Windows Media est traitée par rapport à l’URL de base spécifiée par les *paramètres*. propriété **baseURL** .</span><span class="sxs-lookup"><span data-stu-id="5a2d9-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the *Settings*.**baseURL** property.</span></span> <span data-ttu-id="5a2d9-147">L’URL de base est concaténée avec l’URL relativement spécifiée, ce qui génère une URL entièrement spécifiée qui est transmise en tant que paramètre de commande par l’événement **commande** .</span><span class="sxs-lookup"><span data-stu-id="5a2d9-147">The base URL is concatenated with the relatively specified URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="5a2d9-148">Le contrôle du lecteur Windows Media traite toujours les commandes de type URL entrantes de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="5a2d9-148">The Windows Media Player control always processes incoming URL-type commands in the following manner:</span></span>

1.  <span data-ttu-id="5a2d9-149">Une commande de type URL est reçue.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="5a2d9-150">*Paramètres*. **baseURL** est utilisé pour créer une URL complète à partir de l’URL relative spécifiée dans la commande de script.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-150">*Settings*.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="5a2d9-151">*Commande* est appelé.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-151">*ScriptCommand* is called.</span></span>
4.  <span data-ttu-id="5a2d9-152">Après que *commande* a retourné, *Settings*. **invokeURLs** est activé.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-152">After *ScriptCommand* returns, *Settings*.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="5a2d9-153">Si *paramètres*. **invokeURLs** a la valeur true et la commande est un type d’URL, l’URL spécifiée est appelée.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-153">If *Settings*.**invokeURLs** is true and the command is a URL-type, the specified URL is invoked.</span></span> <span data-ttu-id="5a2d9-154">Si *paramètres*. **invokeURLs** a la valeur false ou, si la commande n’est pas un type d’URL, la commande est ignorée.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-154">If *Settings*.**invokeURLs** is false or if the command is not a URL-type, the command is ignored.</span></span>

<span data-ttu-id="5a2d9-155">Lors de la création d’un fichier Windows Media, vous pouvez spécifier le cadre dans lequel la nouvelle URL est affichée en concaténant deux et et le nom du cadre dans le champ de paramètre.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="5a2d9-156">L’exemple ci-dessous illustre les paramètres *commande* typiques.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-156">The example below illustrates typical *ScriptCommand* parameters.</span></span> <span data-ttu-id="5a2d9-157">Il spécifie que l’URL *MyPage* doit être lancée dans le frame *MyFrame* .</span><span class="sxs-lookup"><span data-stu-id="5a2d9-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



<span data-ttu-id="5a2d9-158">L’événement commande n’est pas appelé si le fichier est en cours d’analyse (transfert rapide ou retour rapide).</span><span class="sxs-lookup"><span data-stu-id="5a2d9-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or fast-reversed).</span></span>

<span data-ttu-id="5a2d9-159">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-159">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="5a2d9-160">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-160">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a2d9-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a2d9-161">Requirements</span></span>



| <span data-ttu-id="5a2d9-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a2d9-162">Requirement</span></span> | <span data-ttu-id="5a2d9-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a2d9-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2d9-164">Version</span><span class="sxs-lookup"><span data-stu-id="5a2d9-164">Version</span></span><br/> | <span data-ttu-id="5a2d9-165">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5a2d9-166">DLL</span><span class="sxs-lookup"><span data-stu-id="5a2d9-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a2d9-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a2d9-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a2d9-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a2d9-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2d9-169">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="5a2d9-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="5a2d9-170">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="5a2d9-170">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="5a2d9-171">**Paramètres. baseURL**</span><span class="sxs-lookup"><span data-stu-id="5a2d9-171">**Settings.baseURL**</span></span>](settings-baseurl.md)
</dt> <dt>

[<span data-ttu-id="5a2d9-172">**Paramètres. defaultFrame**</span><span class="sxs-lookup"><span data-stu-id="5a2d9-172">**Settings.defaultFrame**</span></span>](settings-defaultframe.md)
</dt> <dt>

[<span data-ttu-id="5a2d9-173">**Paramètres. invokeURLs**</span><span class="sxs-lookup"><span data-stu-id="5a2d9-173">**Settings.invokeURLs**</span></span>](settings-invokeurls.md)
</dt> </dl>

 

 





