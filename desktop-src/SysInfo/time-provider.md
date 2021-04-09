---
description: Le système d’exploitation Microsoft Windows prend en charge un large éventail de périphériques matériels et de protocoles de temps réseau à l’aide de l’architecture du fournisseur de temps.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Fournisseur de temps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867381"
---
# <a name="time-provider"></a><span data-ttu-id="abde2-103">Fournisseur de temps</span><span class="sxs-lookup"><span data-stu-id="abde2-103">Time Provider</span></span>

<span data-ttu-id="abde2-104">Le système d’exploitation Microsoft Windows prend en charge un large éventail de périphériques matériels et de protocoles de temps réseau à l’aide de l’architecture du *fournisseur de temps* .</span><span class="sxs-lookup"><span data-stu-id="abde2-104">The Microsoft Windows operating system provides support for a variety of hardware devices and network time protocols using the *time provider* architecture.</span></span> <span data-ttu-id="abde2-105">Les fournisseurs de temps d’entrée récupèrent des horodatages précis à partir du matériel ou du réseau, et les fournisseurs de temps de sortie fournissent des horodateurs à d’autres clients sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="abde2-105">Input time providers retrieve accurate time stamps from hardware or the network, and output time providers provide time stamps to other clients on the network.</span></span>

<span data-ttu-id="abde2-106">Les fournisseurs de temps sont gérés par le *Gestionnaire du fournisseur de temps*.</span><span class="sxs-lookup"><span data-stu-id="abde2-106">Time providers are managed by the *time provider manager*.</span></span> <span data-ttu-id="abde2-107">Il est responsable du chargement, du démarrage et de l’arrêt des fournisseurs de temps comme indiqué par le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="abde2-107">It is responsible for loading, starting, and stopping time providers as directed by the service control manager.</span></span> <span data-ttu-id="abde2-108">Cette interface rend l’écriture d’un fournisseur de temps plus facile que l’écriture d’un service complet.</span><span class="sxs-lookup"><span data-stu-id="abde2-108">This interface makes writing a time provider easier than writing a full service.</span></span>

-   [<span data-ttu-id="abde2-109">Création d’un fournisseur de temps</span><span class="sxs-lookup"><span data-stu-id="abde2-109">Creating a Time Provider</span></span>](creating-a-time-provider.md)
-   [<span data-ttu-id="abde2-110">Inscription d’un fournisseur de temps</span><span class="sxs-lookup"><span data-stu-id="abde2-110">Registering a Time Provider</span></span>](registering-a-time-provider.md)
-   [<span data-ttu-id="abde2-111">Exemple de fournisseur de temps</span><span class="sxs-lookup"><span data-stu-id="abde2-111">Sample Time Provider</span></span>](sample-time-provider.md)

## <a name="related-topics"></a><span data-ttu-id="abde2-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="abde2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abde2-113">Service de temps Windows</span><span class="sxs-lookup"><span data-stu-id="abde2-113">Windows Time Service</span></span>](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



