---
description: CSingleFilterTerminal est une classe de base de terminal supplémentaire applicable aux terminaux statiques et dynamiques.
ms.assetid: d423438f-1324-4df3-beaa-fdef325fac2e
title: CSingleFilterTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111a20e59ab0c549e994695610364c451c07fd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527227"
---
# <a name="csinglefilterterminal"></a><span data-ttu-id="9f3d4-103">CSingleFilterTerminal</span><span class="sxs-lookup"><span data-stu-id="9f3d4-103">CSingleFilterTerminal</span></span>

<span data-ttu-id="9f3d4-104">**CSingleFilterTerminal** est une classe de base de terminal supplémentaire applicable aux terminaux statiques et dynamiques.</span><span class="sxs-lookup"><span data-stu-id="9f3d4-104">**CSingleFilterTerminal** is an additional terminal base class applicable to both static and dynamic terminals.</span></span> <span data-ttu-id="9f3d4-105">Elle est dérivée de [**CBaseTerminal**](cbaseterminal.md) et rend l’implémentation plus spécifique en supposant que le terminal possède un filtre DirectShow unique.</span><span class="sxs-lookup"><span data-stu-id="9f3d4-105">It is derived from [**CBaseTerminal**](cbaseterminal.md) and makes the implementation more specific by assuming that the terminal has a single DirectShow filter.</span></span> <span data-ttu-id="9f3d4-106">Lorsque cette condition est remplie, la dérivation d’une implémentation de terminal à partir de **CSingleFilterTerminal** est beaucoup plus facile que la dérivation à partir de **CBaseTerminal**.</span><span class="sxs-lookup"><span data-stu-id="9f3d4-106">When this condition is met, deriving a terminal implementation from **CSingleFilterTerminal** is much easier than deriving from **CBaseTerminal**.</span></span>

<span data-ttu-id="9f3d4-107">Défini dans MSPterm. h.</span><span class="sxs-lookup"><span data-stu-id="9f3d4-107">Defined in MSPterm.h.</span></span>

 

 



