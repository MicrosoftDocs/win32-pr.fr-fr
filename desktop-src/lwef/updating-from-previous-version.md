---
title: Mise à jour à partir de la version précédente
description: Mise à jour à partir de la version précédente
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e2cf49fbe21c2522226ec61ab57c93d9df27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513448"
---
# <a name="updating-from-previous-version"></a><span data-ttu-id="f83b3-103">Mise à jour à partir de la version précédente</span><span class="sxs-lookup"><span data-stu-id="f83b3-103">Updating from Previous Version</span></span>

<span data-ttu-id="f83b3-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f83b3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f83b3-105">Les applications générées et compilées avec la version 1,5 précédente de Microsoft Agent doivent s’exécuter sans modification sous la nouvelle version 2,0.</span><span class="sxs-lookup"><span data-stu-id="f83b3-105">Applications built and compiled with the previous 1.5 version of Microsoft Agent should run without modification under the new 2.0 version.</span></span> <span data-ttu-id="f83b3-106">La propriété [**Connected**](connected-property.md) ne peut plus avoir la valeur **false**; certaines propriétés de l’objet SpeechInput qui ont été remplacées existent toujours, mais ne transforment plus les valeurs et le serveur ne déclenche plus les événements de [**redémarrage**](https://www.bing.com/search?q=**Restart**) et d' [**arrêt**](https://www.bing.com/search?q=**Shutdown**) .</span><span class="sxs-lookup"><span data-stu-id="f83b3-106">The [**Connected**](connected-property.md) property can no longer be set to **False**; certain properties of the SpeechInput object that have been replaced still exist, but no longer turn any values, and the server no longer fires the [**Restart**](https://www.bing.com/search?q=**Restart**) and [**Shutdown**](https://www.bing.com/search?q=**Shutdown**) events.</span></span>

<span data-ttu-id="f83b3-107">Toutefois, si vous mettez à jour vos applications pour utiliser le contrôle de l’agent 2,0, vous devrez peut-être modifier votre code.</span><span class="sxs-lookup"><span data-stu-id="f83b3-107">However, if you update your applications to use the Agent 2.0 control, you may have to modify your code.</span></span> <span data-ttu-id="f83b3-108">Si vous avez installé la version 2,0 de Microsoft Agent et que vous chargez un projet Visual Basic utilisez la version antérieure du contrôle de l’agent, Visual Basic comprend une option qui affiche automatiquement un message indiquant qu’il a détecté une nouvelle version du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f83b3-108">If you have installed the 2.0 version of Microsoft Agent and load a Visual Basic project use the earlier version of the Agent control, Visual Basic includes an option that will automatically display a message indicating that it detected a new version of the control.</span></span> <span data-ttu-id="f83b3-109">Pour garantir le bon fonctionnement de votre application, choisissez toujours d’utiliser la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="f83b3-109">To ensure proper operation of your application, always choose to use the later version.</span></span>

<span data-ttu-id="f83b3-110">Pour d’autres langages de programmation (tels que Microsoft Office 97 VBA), pour mettre à jour le contrôle, vous devrez peut-être d’abord supprimer le contrôle de l’agent 1,5 et enregistrer votre code.</span><span class="sxs-lookup"><span data-stu-id="f83b3-110">For other programming languages (such as Microsoft Office 97 VBA), to update the control, you may have to first remove the 1.5 Agent control and save your code.</span></span> <span data-ttu-id="f83b3-111">Ensuite, quittez l’environnement de programmation, redémarrez l’environnement de programmation, rechargez votre code et insérez le nouveau contrôle.</span><span class="sxs-lookup"><span data-stu-id="f83b3-111">Then, quit the programming environment, restart the programming environment, reload your code and insert the new control.</span></span> <span data-ttu-id="f83b3-112">Évitez de modifier une application compatible agent 2,0 dans la même instance de l’environnement de programmation que vous modifiez une application agent 1,5 dans.</span><span class="sxs-lookup"><span data-stu-id="f83b3-112">Avoid editing an Agent 2.0-enabled application in the same instance of the programming environment that you are editing an Agent 1.5-enabled application in.</span></span> <span data-ttu-id="f83b3-113">Certains environnements de programmation peuvent ne pas gérer les différences entre les deux versions des contrôles.</span><span class="sxs-lookup"><span data-stu-id="f83b3-113">Some programming environments may not handle the differences between the two versions of controls.</span></span>

<span data-ttu-id="f83b3-114">Vous devez être en mesure de désinstaller l’agent 1,5 sur votre système après l’installation de la version de l’agent 2,0.</span><span class="sxs-lookup"><span data-stu-id="f83b3-114">You should be able to uninstall the Agent 1.5 release on your system after installing the Agent 2.0 release.</span></span> <span data-ttu-id="f83b3-115">Toutefois, si l’agent 1,5 est installé sur la version 2,0, vous devrez peut-être réinstaller 2,0.</span><span class="sxs-lookup"><span data-stu-id="f83b3-115">However, if Agent 1.5 is installed over the 2.0 release, you may have to reinstall 2.0.</span></span>

 

 




