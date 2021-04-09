---
title: Gestion des erreurs (Windows Media Player SDK)
description: Gestion des erreurs
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Lecteur Windows Media, gestion des erreurs
- Windows Media Player Object Model, gestion des erreurs
- modèle objet, gestion des erreurs
- Contrôle ActiveX du lecteur Windows Media, gestion des erreurs
- Contrôle ActiveX, gestion des erreurs
- Contrôle ActiveX Windows Media Player Mobile, gestion des erreurs
- Windows Media Player Mobile, gestion des erreurs
- Guide de migration, gestion des erreurs
- gestion des erreurs dans le modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102625"
---
# <a name="error-handling-windows-media-player-sdk"></a><span data-ttu-id="6df01-112">Gestion des erreurs (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="6df01-112">Error Handling (Windows Media Player SDK)</span></span>

<span data-ttu-id="6df01-113">Le contrôle ActiveX du lecteur Windows Media 6,4 fournit la gestion des erreurs par défaut en affichant les messages d’erreur dans les boîtes de dialogue et dans la barre d’État.</span><span class="sxs-lookup"><span data-stu-id="6df01-113">The Windows Media Player 6.4 ActiveX control provides default error handling by displaying error messages in dialog boxes and on the status bar.</span></span> <span data-ttu-id="6df01-114">Vous pouvez également fournir une gestion personnalisée des erreurs en traitant les erreurs dans votre script.</span><span class="sxs-lookup"><span data-stu-id="6df01-114">You can also provide custom error handling by processing errors in your script.</span></span> <span data-ttu-id="6df01-115">La gestion des erreurs est pilotée par les événements, ce qui signifie que vous recevez une notification pour chaque erreur et que vous devez décider comment traiter chaque événement d’erreur lorsqu’il se produit.</span><span class="sxs-lookup"><span data-stu-id="6df01-115">Error handling is event driven, which means you receive a notification for each error, and must decide how to deal with each error event when it occurs.</span></span> <span data-ttu-id="6df01-116">Pour plus d’informations sur la gestion des erreurs à l’aide du modèle d’objet de la version 6,4, consultez la section gestion des erreurs du Guide du modèle d’objet du lecteur version 6,4, qui fait partie du kit de développement logiciel (SDK) du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6df01-116">For more information about handling errors using the version 6.4 object model, see the Error Handling section of the Version 6.4 Player Object Model Guide, which is part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="6df01-117">Le modèle objet Windows Media Player 7 ou version ultérieure fournit l’objet d' **erreur** et l’objet **ErrorItem** pour gérer les erreurs.</span><span class="sxs-lookup"><span data-stu-id="6df01-117">The Windows Media Player 7 or later object model provides the **Error** object and the **ErrorItem** object to handle errors.</span></span> <span data-ttu-id="6df01-118">Ces deux objets fonctionnent ensemble pour vous fournir un mécanisme de gestion des erreurs qui vous donne un contrôle complet et flexible du processus de gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="6df01-118">These two objects work together to provide you with an error handling mechanism that gives you complete and flexible control of the error handling process.</span></span> <span data-ttu-id="6df01-119">L’objet **Error** donne accès à une collection d’objets **ErrorItem** ; chaque objet **ErrorItem** fournit des détails sur un message d’erreur individuel.</span><span class="sxs-lookup"><span data-stu-id="6df01-119">The **Error** object provides access to a collection of **ErrorItem** objects; each **ErrorItem** object provides details about an individual error message.</span></span>

<span data-ttu-id="6df01-120">Lorsqu’une erreur se produit, les informations sur l’erreur sont publiées dans une file d’attente d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="6df01-120">When an error occurs, the error information is posted to an error queue.</span></span> <span data-ttu-id="6df01-121">La file d’attente est une collection d’objets **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="6df01-121">The queue is a collection of **ErrorItem** objects.</span></span> <span data-ttu-id="6df01-122">À mesure que chaque erreur est ajoutée à la file d’attente, elle est associée à un numéro d’index (commençant par zéro) qui peut être utilisé pour identifier l’objet **ErrorItem** particulier.</span><span class="sxs-lookup"><span data-stu-id="6df01-122">As each error is added to the queue, it is associated with an index number (beginning with zero) that can be used to identify the particular **ErrorItem** object.</span></span> <span data-ttu-id="6df01-123">*Erreur*. la propriété **errorCount** récupère le nombre d’erreurs dans la file d’attente d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="6df01-123">The *Error*.**errorCount** property retrieves the number of errors in the error queue.</span></span> <span data-ttu-id="6df01-124">Étant donné que les numéros d’index sont de base zéro, l’erreur la plus récente publiée dans la file d’attente aura toujours une valeur d’index égale à *Error*. **errorCount** moins un.</span><span class="sxs-lookup"><span data-stu-id="6df01-124">Since the index numbers are zero-based, the most recent error posted to the queue will always have an index value equal to *Error*.**errorCount** minus one.</span></span>

<span data-ttu-id="6df01-125">Vous pouvez créer un gestionnaire d’événements d’erreur pour le lecteur Windows Media à l’aide d’un script.</span><span class="sxs-lookup"><span data-stu-id="6df01-125">You can create an error event handler for Windows Media Player using script.</span></span> <span data-ttu-id="6df01-126">L’exemple JScript suivant montre comment récupérer l’élément d’erreur le plus récent de la file d’attente d’erreurs et afficher le code d’erreur et la description d’erreur à l’aide du modèle objet Windows Media Player 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6df01-126">The following JScript example shows how to retrieve the most recent error item from the error queue and display the error code and error description using the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="6df01-127">L’objet **lecteur** a été créé avec l’ID = « wmp9 ».</span><span class="sxs-lookup"><span data-stu-id="6df01-127">The **Player** object was created with ID = "WMP9".</span></span>


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



<span data-ttu-id="6df01-128">L’objet **Error** a deux méthodes supplémentaires que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="6df01-128">The **Error** object has two additional methods that you can use.</span></span> <span data-ttu-id="6df01-129">*Erreur*. la méthode **clearErrorQueue** vous permet de supprimer toutes les erreurs de la file d’attente d’erreurs et de réinitialiser le numéro d’index à zéro.</span><span class="sxs-lookup"><span data-stu-id="6df01-129">The *Error*.**clearErrorQueue** method allows you to remove all the errors from the error queue and reset the index number to zero.</span></span> <span data-ttu-id="6df01-130">Vous avez un contrôle total sur ce processus ; vous pouvez conserver les erreurs dans la file d’attente tant que vous en avez besoin pour qu’elles soient disponibles, puis vider la file d’attente lorsque vous avez terminé de traiter les erreurs.</span><span class="sxs-lookup"><span data-stu-id="6df01-130">You have complete control over this process; you can keep errors in the queue for as long as you need them to be available, and then empty the queue when you're finished handling the errors.</span></span>

<span data-ttu-id="6df01-131">*Erreur*. la méthode **Webhelp** offre un moyen d’afficher les informations les plus récentes sur l’erreur à l’utilisateur à l’aide d’Internet.</span><span class="sxs-lookup"><span data-stu-id="6df01-131">The *Error*.**webHelp** method provides a way to display the most current error information to the user by using the Internet.</span></span> <span data-ttu-id="6df01-132">Lorsqu’elle est appelée, cette méthode transfère toutes les informations pertinentes sur la première erreur de la file d’attente (celle avec l’index zéro) à l’aide Web du lecteur Microsoft Windows Media, qui affiche des informations supplémentaires sur l’erreur dans la fenêtre du navigateur active.</span><span class="sxs-lookup"><span data-stu-id="6df01-132">When called, this method transfers all relevant information about the first error in the queue (the one with index zero) to Microsoft Windows Media Player Web Help, which displays further information about the error in the current browser window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6df01-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6df01-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6df01-134">**Error, objet**</span><span class="sxs-lookup"><span data-stu-id="6df01-134">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="6df01-135">**Objet ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="6df01-135">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="6df01-136">**Guide de migration du modèle objet**</span><span class="sxs-lookup"><span data-stu-id="6df01-136">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




