---
description: ICE29 vérifie que les noms de flux tronqués restent uniques. Toute table ayant une colonne binaire ou objet est validée. Consultez le type de données de la colonne binaire.
ms.assetid: a51b641d-992b-4b6b-a208-d94bc7d05115
title: ICE29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f606bd09314d045b643816c08349eba38bde72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951640"
---
# <a name="ice29"></a><span data-ttu-id="7c54e-105">ICE29</span><span class="sxs-lookup"><span data-stu-id="7c54e-105">ICE29</span></span>

<span data-ttu-id="7c54e-106">ICE29 vérifie que les noms de flux tronqués restent uniques.</span><span class="sxs-lookup"><span data-stu-id="7c54e-106">ICE29 validates that truncated stream names remain unique.</span></span> <span data-ttu-id="7c54e-107">Toute table ayant une colonne binaire ou objet est validée.</span><span class="sxs-lookup"><span data-stu-id="7c54e-107">Any table having a Binary or Object column is validated.</span></span> <span data-ttu-id="7c54e-108">Consultez le type de données de la colonne [binaire](binary.md) .</span><span class="sxs-lookup"><span data-stu-id="7c54e-108">See the [Binary](binary.md) column data type.</span></span>

<span data-ttu-id="7c54e-109">La gestion des flux par l’implémentation de stockage structuré OLE Win32 limite les noms de flux.</span><span class="sxs-lookup"><span data-stu-id="7c54e-109">Handling of streams by the Win32 OLE structured storage implementation limits stream names.</span></span> <span data-ttu-id="7c54e-110">Consultez [limitations OLE sur les flux](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="7c54e-110">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="7c54e-111">Le programme d’installation peut compresser des noms de flux d’une longueur maximale de 62 caractères.</span><span class="sxs-lookup"><span data-stu-id="7c54e-111">The installer can compress stream names up to 62 characters in length.</span></span> <span data-ttu-id="7c54e-112">Les noms plus longs sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="7c54e-112">Names longer than this are truncated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c54e-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c54e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c54e-114">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="7c54e-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



