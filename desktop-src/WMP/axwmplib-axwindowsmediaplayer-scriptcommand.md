---
title: Événement commande de l’objet AxWindowsMediaPlayer
description: L’événement commande se produit lors de la réception d’une commande ou d’une URL synchronisée. | Événement commande de l’objet AxWindowsMediaPlayer
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- Événement commande de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527309"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4ab00-105">Événement commande de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4ab00-105">ScriptCommand Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4ab00-106">L’événement commande se produit lors de la réception d’une commande ou d’une URL synchronisée.</span><span class="sxs-lookup"><span data-stu-id="4ab00-106">The ScriptCommand event occurs when a synchronized command or URL is received.</span></span>

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a><span data-ttu-id="4ab00-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="4ab00-107">Event Data</span></span>

<span data-ttu-id="4ab00-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4ab00-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEventHandler**.</span></span> <span data-ttu-id="4ab00-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEvent**, qui contient les propriétés suivantes relatives à cet événement.</span><span class="sxs-lookup"><span data-stu-id="4ab00-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="4ab00-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="4ab00-110">Property</span></span> | <span data-ttu-id="4ab00-111">Description</span><span class="sxs-lookup"><span data-stu-id="4ab00-111">Description</span></span>                                                   |
|----------|---------------------------------------------------------------|
| <span data-ttu-id="4ab00-112">scType</span><span class="sxs-lookup"><span data-stu-id="4ab00-112">scType</span></span>   | <span data-ttu-id="4ab00-113">System. StringSpecifies le type de commande de script.</span><span class="sxs-lookup"><span data-stu-id="4ab00-113">System.StringSpecifies the type of script command.</span></span><br/> |
| <span data-ttu-id="4ab00-114">param</span><span class="sxs-lookup"><span data-stu-id="4ab00-114">param</span></span>    | <span data-ttu-id="4ab00-115">System. StringSpecifies la commande de script.</span><span class="sxs-lookup"><span data-stu-id="4ab00-115">System.StringSpecifies the script command.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="4ab00-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4ab00-116">Remarks</span></span>

<span data-ttu-id="4ab00-117">Les commandes peuvent être incorporées parmi les sons et les images d’un fichier ou d’un flux Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4ab00-117">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="4ab00-118">Les commandes sont une paire de chaînes Unicode associées à une heure désignée dans le flux.</span><span class="sxs-lookup"><span data-stu-id="4ab00-118">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="4ab00-119">Lorsque le flux atteint l’heure associée à la commande, le contrôle du lecteur Windows Media envoie un événement **commande** avec deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="4ab00-119">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="4ab00-120">Un paramètre spécifie le type de commande en cours d’envoi, tandis que l’autre paramètre spécifie la commande.</span><span class="sxs-lookup"><span data-stu-id="4ab00-120">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="4ab00-121">Le type de paramètre est utilisé pour déterminer la façon dont le paramètre de commande est traité.</span><span class="sxs-lookup"><span data-stu-id="4ab00-121">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="4ab00-122">Tout type de commande peut être incorporé dans un fichier ou un flux à gérer par l’événement **commande** .</span><span class="sxs-lookup"><span data-stu-id="4ab00-122">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="4ab00-123">Le tableau suivant répertorie les types de commande de script qui sont traités automatiquement par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4ab00-123">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="4ab00-124">Type</span><span class="sxs-lookup"><span data-stu-id="4ab00-124">Type</span></span>                   | <span data-ttu-id="4ab00-125">Description</span><span class="sxs-lookup"><span data-stu-id="4ab00-125">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab00-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="4ab00-126">CAPTION</span></span>                | <span data-ttu-id="4ab00-127">Le contrôle affiche le texte associé dans l’élément HTML spécifié par IWMPClosedCaption. **captioningId**.</span><span class="sxs-lookup"><span data-stu-id="4ab00-127">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="4ab00-128">ÉVÉNEMENT</span><span class="sxs-lookup"><span data-stu-id="4ab00-128">EVENT</span></span>                  | <span data-ttu-id="4ab00-129">Le contrôle exécute les instructions définies pour l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="4ab00-129">The control executes instructions defined for the specified event.</span></span>                                                                                                  |
| <span data-ttu-id="4ab00-130">EXTENSION</span><span class="sxs-lookup"><span data-stu-id="4ab00-130">FILENAME</span></span>               | <span data-ttu-id="4ab00-131">Le contrôle réinitialise sa propriété **URL** , tente d’ouvrir le fichier spécifié et commence à lire immédiatement le nouveau flux.</span><span class="sxs-lookup"><span data-stu-id="4ab00-131">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="4ab00-132">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="4ab00-132">OPENEVENT</span></span>              | <span data-ttu-id="4ab00-133">Met en mémoire tampon la commande de type d’événement associée pour l’exécution en temps opportun du script d’événement.</span><span class="sxs-lookup"><span data-stu-id="4ab00-133">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="4ab00-134">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="4ab00-134">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="4ab00-135">Le paramètre *param* contient le texte Lyric synchronisé.</span><span class="sxs-lookup"><span data-stu-id="4ab00-135">The *param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="4ab00-136">Le lecteur Windows Media affiche le texte Lyric dans la zone de légende fermée de la fonctionnalité de **lecture** en cours.</span><span class="sxs-lookup"><span data-stu-id="4ab00-136">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="4ab00-137">TEXT</span><span class="sxs-lookup"><span data-stu-id="4ab00-137">TEXT</span></span>                   | <span data-ttu-id="4ab00-138">Le contrôle affiche le texte associé dans l’élément HTML spécifié par IWMPClosedCaption. **captioningId**.</span><span class="sxs-lookup"><span data-stu-id="4ab00-138">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="4ab00-139">URL</span><span class="sxs-lookup"><span data-stu-id="4ab00-139">URL</span></span>                    | <span data-ttu-id="4ab00-140">Le contrôle ouvre automatiquement l’URL spécifiée à l’aide du navigateur Internet par défaut si IWMPSettings. la propriété **invokeURLs** a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="4ab00-140">The control automatically opens the URL specified using the default Internet browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span>                    |



 

<span data-ttu-id="4ab00-141">Vous pouvez incorporer n’importe quel autre type de commande tant que vous fournissez du code pour gérer la commande.</span><span class="sxs-lookup"><span data-stu-id="4ab00-141">You can embed any other type of command as long as you provide code to handle the command.</span></span> <span data-ttu-id="4ab00-142">Bien que les commandes inconnues soient ignorées par le contrôle du lecteur Windows Media, elles sont toujours transmises à l’événement **commande** .</span><span class="sxs-lookup"><span data-stu-id="4ab00-142">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="4ab00-143">L’événement commande n’est pas appelé si le fichier est en cours d’analyse en mode avance rapide ou rembobinage.</span><span class="sxs-lookup"><span data-stu-id="4ab00-143">The ScriptCommand event is not called if the file is being scanned in fast forward or rewind mode.</span></span>

<span data-ttu-id="4ab00-144">Les commandes d’URL reçues par le contrôle du lecteur Windows Media sont appelées automatiquement dans votre navigateur Web par défaut si IWMPSettings. la propriété **invokeURLs** a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="4ab00-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="4ab00-145">Vous pouvez utiliser IWMPSettings. propriété **defaultFrame** pour spécifier le frame cible dans lequel la page Web s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4ab00-145">You can use the IWMPSettings.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="4ab00-146">L’URL envoyée au lecteur Windows Media est traitée par rapport à l’URL de base spécifiée par IWMPSettings. propriété **baseURL** .</span><span class="sxs-lookup"><span data-stu-id="4ab00-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the IWMPSettings.**baseURL** property.</span></span> <span data-ttu-id="4ab00-147">L’URL de base est concaténée avec l’URL relative, ce qui génère une URL entièrement spécifiée qui est transmise en tant que paramètre de commande par l’événement **commande** .</span><span class="sxs-lookup"><span data-stu-id="4ab00-147">The base URL is concatenated with the relative URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="4ab00-148">Le contrôle du lecteur Windows Media traite toujours les commandes d’URL entrantes de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="4ab00-148">The Windows Media Player control always processes incoming URL commands in the following manner:</span></span>

1.  <span data-ttu-id="4ab00-149">Une commande de type URL est reçue.</span><span class="sxs-lookup"><span data-stu-id="4ab00-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="4ab00-150">IWMPSettings. **baseURL** est utilisé pour créer une URL complète à partir de l’URL relative spécifiée dans la commande de script.</span><span class="sxs-lookup"><span data-stu-id="4ab00-150">IWMPSettings.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="4ab00-151">**Commande** est appelé.</span><span class="sxs-lookup"><span data-stu-id="4ab00-151">**ScriptCommand** is called.</span></span>
4.  <span data-ttu-id="4ab00-152">Après que **commande** a retourné, IWMPSettings. **invokeURLs** est activé.</span><span class="sxs-lookup"><span data-stu-id="4ab00-152">After **ScriptCommand** returns, IWMPSettings.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="4ab00-153">Si IWMPSettings. **invokeURLs** a la valeur true et la commande est une commande URL, l’URL spécifiée est appelée.</span><span class="sxs-lookup"><span data-stu-id="4ab00-153">If IWMPSettings.**invokeURLs** is true and the command is a URL command, the specified URL is invoked.</span></span> <span data-ttu-id="4ab00-154">Si IWMPSettings. **invokeURLs** a la valeur false ou, si la commande n’est pas une commande URL, la commande est ignorée.</span><span class="sxs-lookup"><span data-stu-id="4ab00-154">If IWMPSettings.**invokeURLs** is false or if the command is not a URL command, the command is ignored.</span></span>

<span data-ttu-id="4ab00-155">Lors de la création d’un fichier Windows Media, vous pouvez spécifier le cadre dans lequel la nouvelle URL est affichée en concaténant deux et et le nom du cadre dans le champ de paramètre.</span><span class="sxs-lookup"><span data-stu-id="4ab00-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="4ab00-156">L’exemple suivant illustre des paramètres **commande** typiques.</span><span class="sxs-lookup"><span data-stu-id="4ab00-156">The following example illustrates typical **ScriptCommand** parameters.</span></span> <span data-ttu-id="4ab00-157">Il spécifie que l’URL *MyPage* doit être lancée dans le frame *MyFrame* .</span><span class="sxs-lookup"><span data-stu-id="4ab00-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



<span data-ttu-id="4ab00-158">L’événement commande n’est pas appelé si le fichier est en cours d’analyse (transféré rapidement ou rembobiner).</span><span class="sxs-lookup"><span data-stu-id="4ab00-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or rewound).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ab00-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ab00-159">Requirements</span></span>



| <span data-ttu-id="4ab00-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ab00-160">Requirement</span></span> | <span data-ttu-id="4ab00-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ab00-161">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab00-162">Version</span><span class="sxs-lookup"><span data-stu-id="4ab00-162">Version</span></span><br/>   | <span data-ttu-id="4ab00-163">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4ab00-163">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4ab00-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4ab00-164">Namespace</span></span><br/> | <span data-ttu-id="4ab00-165">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4ab00-165">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4ab00-166">Assembly</span><span class="sxs-lookup"><span data-stu-id="4ab00-166">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4ab00-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4ab00-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ab00-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ab00-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ab00-169">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4ab00-169">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ab00-170">**AxWindowsMediaPlayer. URL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4ab00-170">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ab00-171">**IWMPClosedCaption. captioningId (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4ab00-171">**IWMPClosedCaption.captioningId (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ab00-172">**IWMPSettings. baseURL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4ab00-172">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ab00-173">**IWMPSettings. defaultFrame (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4ab00-173">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4ab00-174">**IWMPSettings. invokeURLs (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4ab00-174">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





