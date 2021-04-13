---
title: Objet agent de révocation des licences
description: Objet agent de révocation des licences
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- Windows Media Format SDK, objets de l’agent de révocation des licences
- ASF (Advanced Systems Format), objets de l’agent de révocation des licences
- ASF (format des systèmes avancés), objets de l’agent de révocation des licences
- objets, objets de l’agent de révocation des licences
- révocation de licence, objets de l’agent de révocation des licences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381479"
---
# <a name="license-revocation-agent-object"></a><span data-ttu-id="a6dd7-108">Objet agent de révocation des licences</span><span class="sxs-lookup"><span data-stu-id="a6dd7-108">License Revocation Agent Object</span></span>

<span data-ttu-id="a6dd7-109">L’objet agent de révocation de licence gère le côté client de la révocation de licence.</span><span class="sxs-lookup"><span data-stu-id="a6dd7-109">The license revocation agent object manages the client side of license revocation.</span></span> <span data-ttu-id="a6dd7-110">La révocation des licences est le processus par lequel un serveur de licences peut supprimer des licences du magasin de licences sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="a6dd7-110">License revocation is the process by which a license server can remove licenses from the license store on the client computer.</span></span> <span data-ttu-id="a6dd7-111">Le processus consiste à transmettre plusieurs messages entre l’application cliente et le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="a6dd7-111">The process involves passing several messages between the client application and the license server.</span></span> <span data-ttu-id="a6dd7-112">Les méthodes exposées sur ce processus d’objet et génèrent ces messages.</span><span class="sxs-lookup"><span data-stu-id="a6dd7-112">The methods exposed on this object process and generate those messages.</span></span>

<span data-ttu-id="a6dd7-113">L’objet agent de révocation de licences est créé par la fonction [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) , qui définit un pointeur vers une interface [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .</span><span class="sxs-lookup"><span data-stu-id="a6dd7-113">The license revocation agent object is created by the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function, which sets a pointer to an [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span> <span data-ttu-id="a6dd7-114">**IUnknown** et **IWMLicenseRevocationAgent** sont les seules interfaces prises en charge par cet objet.</span><span class="sxs-lookup"><span data-stu-id="a6dd7-114">**IUnknown** and **IWMLicenseRevocationAgent** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6dd7-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6dd7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6dd7-116">**Objets**</span><span class="sxs-lookup"><span data-stu-id="a6dd7-116">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




