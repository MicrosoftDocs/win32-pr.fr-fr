---
title: Création d’un fournisseur de protocole RDP (Remote Desktop Protocol)
description: Informations sur la création d’un fournisseur de protocole RDP (Remote Desktop Protocol). Le gestionnaire de protocole est implémenté en tant que serveur COM et enregistré dans un emplacement où le service Services Bureau à distance démarre.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41265a350b4d5c559731a09abc21aa4c81b9b29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510182"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a><span data-ttu-id="c371c-104">Création d’un fournisseur de protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="c371c-104">Creating a Remote Desktop Protocol Provider</span></span>

<span data-ttu-id="c371c-105">Les sections suivantes contiennent des informations sur la création d’un fournisseur de protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="c371c-105">The following sections contain information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="c371c-106">Le gestionnaire de protocole est implémenté en tant que serveur COM et enregistré dans un emplacement où le service Services Bureau à distance démarre.</span><span class="sxs-lookup"><span data-stu-id="c371c-106">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c371c-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c371c-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="c371c-108">Inscription du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="c371c-108">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
</dt> <dd>

<span data-ttu-id="c371c-109">Vous devez créer au moins une entrée de valeur de Registre pour votre gestionnaire de protocole afin que le service Services Bureau à distance puisse l’instancier.</span><span class="sxs-lookup"><span data-stu-id="c371c-109">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

</dd> <dt>

[<span data-ttu-id="c371c-110">Séquence d’appel de méthode</span><span class="sxs-lookup"><span data-stu-id="c371c-110">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dd>

<span data-ttu-id="c371c-111">Le service Services Bureau à distance et votre fournisseur de protocole appellent l’un l’autre dans des séquences clairement définies.</span><span class="sxs-lookup"><span data-stu-id="c371c-111">The Remote Desktop Services service and your protocol provider call each other in clearly defined sequences.</span></span>

</dd> </dl>

-   [<span data-ttu-id="c371c-112">Inscription du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="c371c-112">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
-   [<span data-ttu-id="c371c-113">Séquence d’appel de méthode</span><span class="sxs-lookup"><span data-stu-id="c371c-113">Method Call Sequence</span></span>](method-call-sequence.md)

## <a name="related-topics"></a><span data-ttu-id="c371c-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c371c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c371c-115">API du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="c371c-115">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dt>

[<span data-ttu-id="c371c-116">Utilisation de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="c371c-116">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> </dl>

 

 




