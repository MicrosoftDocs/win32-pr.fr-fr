---
title: Guide de programmation WPD
description: Guide de programmation
ms.assetid: 87777b0b-a7a0-4032-99bb-92b717d3c452
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f774ffd9d7576a07b34c467a5a155d98e4f3e703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519534"
---
# <a name="wpd-programming-guide"></a><span data-ttu-id="135b5-103">Guide de programmation WPD</span><span class="sxs-lookup"><span data-stu-id="135b5-103">WPD programming guide</span></span>

<span data-ttu-id="135b5-104">La principale source de ce guide de programmation est un exemple fourni avec le kit de développement logiciel (SDK) Windows Mobile Devices (WPD).</span><span class="sxs-lookup"><span data-stu-id="135b5-104">The primary source for this programming guide is a sample that ships with the Windows Portable Devices (WPD) Software Development Kit (SDK).</span></span> <span data-ttu-id="135b5-105">Cet exemple, nommé WpdApiSample.exe, se compose de sept modules. cpp.</span><span class="sxs-lookup"><span data-stu-id="135b5-105">This sample, named WpdApiSample.exe, consists of seven .cpp modules.</span></span> <span data-ttu-id="135b5-106">Six de ces modules contiennent le code qui illustre 26 tâches qu’une application peut accomplir à l’aide de l’interface de programmation d’applications (API) WPD.</span><span class="sxs-lookup"><span data-stu-id="135b5-106">Six of these modules contain the code that demonstrates 26 tasks that an application can accomplish using the WPD application programming interface (API).</span></span>

<span data-ttu-id="135b5-107">Les exceptions à ce qui précède sont les rubriques qui décrivent : les tâches du service de périphérique, le menu contextuel et les extensions de feuille de propriétés. ces rubriques n’ont pas été extraites de WpdApiSample.</span><span class="sxs-lookup"><span data-stu-id="135b5-107">The exceptions to the above are the topics that describe: device service tasks, the context menu and property sheet extensions; these topics were not taken from WpdApiSample.</span></span> <span data-ttu-id="135b5-108">Les tâches du service d’appareil sont basées sur l’exemple nommé WpdServiceApiSample.</span><span class="sxs-lookup"><span data-stu-id="135b5-108">The device service tasks are based on the sample named WpdServiceApiSample.</span></span> <span data-ttu-id="135b5-109">Les extensions de menu contextuel et de feuille de propriétés sont extraites des applications qui ne sont pas fournies avec le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="135b5-109">The context menu and property sheet extensions are snippets taken from applications that do not ship with the Windows SDK.</span></span>

<span data-ttu-id="135b5-110">Les sections suivantes se concentrent sur les tâches accomplies par ces exemples et expliquent comment chacune d’elles est accomplie à l’aide des interfaces WPD et d’un certain nombre de méthodes trouvées dans ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="135b5-110">The following sections focus on the tasks accomplished by these samples and explain how each is accomplished using the WPD interfaces and a number of the methods found in these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="135b5-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="135b5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="135b5-112">**Appareils mobiles Windows**</span><span class="sxs-lookup"><span data-stu-id="135b5-112">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
