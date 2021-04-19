---
title: Détection du lecteur Windows Media à partir d’une application
description: Détection du lecteur Windows Media à partir d’une application
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Lecteur Windows Media, détection à partir d’applications
- détection de Windows Media Player à partir d’applications
- Registre, détection de Windows Media Player à partir d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511451"
---
# <a name="detecting-windows-media-player-from-an-application"></a><span data-ttu-id="b5272-106">Détection du lecteur Windows Media à partir d’une application</span><span class="sxs-lookup"><span data-stu-id="b5272-106">Detecting Windows Media Player from an Application</span></span>

<span data-ttu-id="b5272-107">Vous pouvez déterminer quelle version du lecteur Windows Media est installée en vérifiant la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="b5272-107">You can determine what version of Windows Media Player is installed by checking the following registry key:</span></span>

<span data-ttu-id="b5272-108">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Active Setup \\ Components installée**</span><span class="sxs-lookup"><span data-stu-id="b5272-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Active Setup\\Installed Components**</span></span>

<span data-ttu-id="b5272-109">Pour le lecteur Windows Media 6,4, consultez la clé **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.</span><span class="sxs-lookup"><span data-stu-id="b5272-109">For Windows Media Player 6.4, look at key **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.</span></span>

<span data-ttu-id="b5272-110">Pour Windows Media Player 7 ou version ultérieure, consultez la clé **{6BF52A52-394A-11D3-B153-00C04F79FAA6}**.</span><span class="sxs-lookup"><span data-stu-id="b5272-110">For Windows Media Player 7 or later, look at key **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**.</span></span>

<span data-ttu-id="b5272-111">Sous l’une de ces clés, si **isInstalled**</span><span class="sxs-lookup"><span data-stu-id="b5272-111">Under either of these keys, if the **IsInstalled**</span></span><dl> <dt>

<span data-ttu-id="b5272-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="b5272-112">Data type</span></span>
</dt> <dd><span data-ttu-id="b5272-113">DWORD</span><span class="sxs-lookup"><span data-stu-id="b5272-113">DWORD</span></span></dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

<span data-ttu-id="b5272-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="b5272-114">Data type</span></span>
</dt> <dd><span data-ttu-id="b5272-115">string</span><span class="sxs-lookup"><span data-stu-id="b5272-115">string</span></span></dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a><span data-ttu-id="b5272-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5272-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5272-117">**Redistribution du logiciel Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="b5272-117">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




