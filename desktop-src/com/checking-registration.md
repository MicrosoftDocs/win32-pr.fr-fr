---
title: Vérification de l’inscription
description: Vérification de l’inscription
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939779"
---
# <a name="checking-registration"></a><span data-ttu-id="706e3-103">Vérification de l’inscription</span><span class="sxs-lookup"><span data-stu-id="706e3-103">Checking Registration</span></span>

<span data-ttu-id="706e3-104">Chaque fois qu’une application est chargée, elle doit vérifier son inscription pour déterminer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="706e3-104">Each time an application loads, it should check its registration to determine the following:</span></span>

-   <span data-ttu-id="706e3-105">Indique si les CLSID sont présents dans le registre.</span><span class="sxs-lookup"><span data-stu-id="706e3-105">Whether the CLSIDs are present in the registry.</span></span> <span data-ttu-id="706e3-106">Si elles ne sont pas présentes, l’application doit s’inscrire en tant que programme d’installation d’origine.</span><span class="sxs-lookup"><span data-stu-id="706e3-106">If they are not present, the application should register as the original setup.</span></span>
-   <span data-ttu-id="706e3-107">Si les CLSID de l’application sont présents dans le registre, mais ne contiennent pas d’informations OLE 2.</span><span class="sxs-lookup"><span data-stu-id="706e3-107">Whether the application's CLSIDs are present in the register but have no OLE 2-related information in them.</span></span> <span data-ttu-id="706e3-108">Si c’est le cas, l’application doit s’inscrire en tant que programme d’installation d’origine.</span><span class="sxs-lookup"><span data-stu-id="706e3-108">If this is the case, the application should register as the original setup.</span></span>
-   <span data-ttu-id="706e3-109">Indique si le chemin d’accès contenant des entrées de serveur ([LocalServer](localserver.md) et [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) et [InprocServer32](inprocserver32.md)et [DefaultIcon](defaulticon.md)) pointe vers l’emplacement où l’application est actuellement installée.</span><span class="sxs-lookup"><span data-stu-id="706e3-109">Whether the path containing server entries ([LocalServer](localserver.md) and [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) and [InprocServer32](inprocserver32.md), and [DefaultIcon](defaulticon.md)) points to the location at which the application is currently installed.</span></span> <span data-ttu-id="706e3-110">Si le chemin d’accès ne le fait pas, réécrivez les entrées du chemin d’accès pour pointer vers l’emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="706e3-110">If the path does not, rewrite the path entries to point to the current location.</span></span>

## <a name="related-topics"></a><span data-ttu-id="706e3-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="706e3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="706e3-112">Inscription des applications COM</span><span class="sxs-lookup"><span data-stu-id="706e3-112">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




