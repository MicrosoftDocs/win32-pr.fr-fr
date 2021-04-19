---
description: Windows Installer implémente un certain nombre de contrôles standard que les auteurs de packages peuvent placer dans des boîtes de dialogue. Toutefois, tous les contrôles Microsoft Windows standard ne sont pas disponibles et les contrôles personnalisés ne peuvent pas être créés pour être utilisés avec l’interface utilisateur du programme d’installation.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Vue d’ensemble des contrôles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fbd8477416eb5a126eca56cb1050112309b0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521190"
---
# <a name="controls-overview"></a><span data-ttu-id="99408-104">Vue d’ensemble des contrôles</span><span class="sxs-lookup"><span data-stu-id="99408-104">Controls Overview</span></span>

<span data-ttu-id="99408-105">Windows Installer implémente un certain nombre de contrôles standard que les auteurs de packages peuvent placer dans des boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="99408-105">Windows Installer implements a number of standard controls that package authors can place onto dialog boxes.</span></span> <span data-ttu-id="99408-106">Toutefois, tous les contrôles Microsoft Windows standard ne sont pas disponibles et les contrôles personnalisés ne peuvent pas être créés pour être utilisés avec l’interface utilisateur du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="99408-106">However, not all standard Microsoft Windows controls are available, and custom controls cannot be created for use with the installer UI.</span></span>

<span data-ttu-id="99408-107">Les contrôles sont créés sur les boîtes de dialogue dans le programme d’installation d’une manière similaire à la façon dont les boîtes de dialogue sont créées par programme à l’aide de l’API de l’interface utilisateur Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="99408-107">Controls are created on dialog boxes in the installer in a manner similar to how dialog boxes are created programmatically using the Microsoft Windows user interface API.</span></span> <span data-ttu-id="99408-108">Un contrôle est créé à partir d’un modèle enregistré dans la table de contrôle.</span><span class="sxs-lookup"><span data-stu-id="99408-108">A control is created from a template recorded in the Control table.</span></span> <span data-ttu-id="99408-109">Ce modèle est légèrement différent en ce qu’il contient le nom unique de la boîte de dialogue dans laquelle le contrôle apparaît.</span><span class="sxs-lookup"><span data-stu-id="99408-109">This template is slightly different in that it contains the unique name of the dialog box on which the control appears.</span></span>

<span data-ttu-id="99408-110">Dans l’API de l’interface utilisateur de Microsoft Windows, l’interaction de l’utilisateur s’effectue en créant une fonction de rappel pour gérer les messages publiés par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="99408-110">In the Microsoft Windows user interface API, user interaction is accomplished by creating a callback function to handle messages posted by the control.</span></span> <span data-ttu-id="99408-111">En outre, la plupart des contrôles Microsoft Windows reçoivent des messages, tels que ceux envoyés par la fonction [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="99408-111">Also, most Microsoft Windows controls receive messages, such as those sent by the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="99408-112">La communication entre l’utilisateur et les contrôles s’effectue dans le programme d’installation à l’aide de [ControlEvents](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="99408-112">Communication between the user and controls is accomplished in the installer through the use of [ControlEvents](controlevent-overview.md).</span></span> <span data-ttu-id="99408-113">Toutefois, il existe un ensemble limité de ControlEvents qui sont spécifiques à chaque contrôle dans l’ensemble limité de contrôles dans Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="99408-113">However, there is a limited set of ControlEvents that are specific to each control in the limited set of controls in Windows Installer.</span></span> <span data-ttu-id="99408-114">Les contrôles peuvent poster plus d’un ControlEvent, et peuvent recevoir plusieurs ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="99408-114">Controls may post more than one ControlEvent and may receive more than one ControlEvent.</span></span>

<span data-ttu-id="99408-115">Les contrôles peuvent publier des ControlEvents spécifiques à l’aide de la table ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="99408-115">Controls can publish specific ControlEvents through the use of the ControlEvent table.</span></span> <span data-ttu-id="99408-116">Les contrôles peuvent recevoir ControlEvents via l’utilisation de la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="99408-116">Controls can receive ControlEvents through the use of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="99408-117">Windows Installer publie ControlEvents lors de l’exécution de certaines actions également, et les contrôles souscrits à ces ControlEvents dans la table EventMapping les reçoivent.</span><span class="sxs-lookup"><span data-stu-id="99408-117">Windows Installer publishes ControlEvents during the execution of some actions as well, and controls subscribed to these ControlEvents in the EventMapping table receive them.</span></span>

 

 
