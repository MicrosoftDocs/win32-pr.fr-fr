---
description: Déterminez la version de Windows Update Agent (WUA) avant de l’utiliser.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Détermination de la version actuelle de WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524968"
---
# <a name="determining-the-current-version-of-wua"></a><span data-ttu-id="a9785-103">Détermination de la version actuelle de WUA</span><span class="sxs-lookup"><span data-stu-id="a9785-103">Determining the Current Version of WUA</span></span>

<span data-ttu-id="a9785-104">Pour obtenir des informations générales sur la mise à jour de l’agent WUA, y compris des instructions pas à pas pour déterminer par programmation à partir de votre application si la version de WUA exécutée sur l’ordinateur répond à vos besoins, consultez [mise à jour de l’agent de Windows Update](updating-the-windows-update-agent.md).</span><span class="sxs-lookup"><span data-stu-id="a9785-104">For general information on updating the WUA, including step by step instructions to programmatically determine from within your app whether the version of WUA that is running on the computer meets your needs, see [Updating the Windows Update Agent](updating-the-windows-update-agent.md).</span></span>

<span data-ttu-id="a9785-105">Dans les versions de Windows antérieures à Windows 7 et Windows Server 2008 R2, vous devez déterminer la version installée de Windows Update Agent (WUA) avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="a9785-105">On versions of Windows prior to Windows 7 and Windows Server 2008 R2, you should determine the installed version of Windows Update Agent (WUA) before you use it.</span></span> <span data-ttu-id="a9785-106">La version actuelle de WUA est déterminée par la version du Wuaueng.dll qui s’exécute dans le \\ sous-répertoire system32 de l’installation Windows actuelle.</span><span class="sxs-lookup"><span data-stu-id="a9785-106">The current version of WUA is determined by the version of the Wuaueng.dll that is running in the \\System32 subdirectory of the current Windows installation.</span></span> <span data-ttu-id="a9785-107">Si la version de Wuaueng.dll est la version 5.4.3790.1000 ou une version ultérieure, WUA est installé.</span><span class="sxs-lookup"><span data-stu-id="a9785-107">If the version of Wuaueng.dll is version 5.4.3790.1000 or a later version, WUA is installed.</span></span> <span data-ttu-id="a9785-108">Une version antérieure à 5.4.3790.1000 indique que Software Update Services (SUS) 1,0 est installé.</span><span class="sxs-lookup"><span data-stu-id="a9785-108">A version that is earlier than 5.4.3790.1000 indicates that Software Update Services (SUS) 1.0 is installed.</span></span>

<span data-ttu-id="a9785-109">Lorsqu’un appel à SUS 1,0 est effectué à l’aide de l’API WUA, un **HRESULT** de Wu \_ E au \_ \_ LEGACYSERVER est retourné.</span><span class="sxs-lookup"><span data-stu-id="a9785-109">When a call is made to SUS 1.0 by using the WUA API, an **HRESULT** of WU\_E\_AU\_LEGACYSERVER is returned.</span></span>

<span data-ttu-id="a9785-110">Vous pouvez également utiliser la méthode [**IWindowsUpdateAgentInfo :: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) pour récupérer la version de fichier actuelle de Wuapi.dll qui s’exécute sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a9785-110">You can also use the [**IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) method to retrieve the current file version of Wuapi.dll that is running on a computer.</span></span> <span data-ttu-id="a9785-111">L’interface [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) n’est pas prise en charge dans WUA 1,0.</span><span class="sxs-lookup"><span data-stu-id="a9785-111">The [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) interface is not supported in WUA 1.0.</span></span>
