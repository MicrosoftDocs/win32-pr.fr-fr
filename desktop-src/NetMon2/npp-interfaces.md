---
description: Les fournisseurs de paquets réseau (NPPs) fournissent des interfaces COM qui sont appelées par les applications NPP et Moniteur réseau.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: Interfaces NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518956"
---
# <a name="npp-interfaces"></a><span data-ttu-id="5b43b-103">Interfaces NPP</span><span class="sxs-lookup"><span data-stu-id="5b43b-103">NPP Interfaces</span></span>

<span data-ttu-id="5b43b-104">Les fournisseurs de paquets réseau (NPPs) fournissent des interfaces COM qui sont appelées par les applications NPP et Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="5b43b-104">Network packet providers (NPPs) provide COM interfaces that are called by NPP applications, and Network Monitor.</span></span> <span data-ttu-id="5b43b-105">Lorsque vous appelez [CreateNPPInterface](createnppinterface.md), rappelez-vous que chaque npp est représenté sous la forme d’un objet com in-process unique.</span><span class="sxs-lookup"><span data-stu-id="5b43b-105">When you call [CreateNPPInterface](createnppinterface.md), remember that each NPP is represented as a single in-process COM object.</span></span> <span data-ttu-id="5b43b-106">Les applications peuvent instancier un nombre quelconque d’objets NPP.</span><span class="sxs-lookup"><span data-stu-id="5b43b-106">Applications can instantiate any number of NPP objects.</span></span> <span data-ttu-id="5b43b-107">Toutefois, chaque objet instancié doit utiliser un et une seule des cinq interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="5b43b-107">However, each instantiated object must use one—and only one—of the five NPP interfaces.</span></span>

<span data-ttu-id="5b43b-108">Notez également que différentes interfaces NPP fournissent des données réseau sous différentes formes.</span><span class="sxs-lookup"><span data-stu-id="5b43b-108">Note also that different NPP interfaces provide network data in various forms.</span></span> <span data-ttu-id="5b43b-109">Par exemple, Moniteur réseau utilise l’interface **IDelaydC** pour capturer le trafic réseau et l’enregistrer dans un fichier de capture. tandis que les analyses utilisent l’interface **IRTC** pour capturer le trafic réseau en temps réel.</span><span class="sxs-lookup"><span data-stu-id="5b43b-109">For example, Network Monitor uses the **IDelaydC** interface to capture network traffic and save it to a capture file; while monitors use the **IRTC** interface to capture real time network traffic.</span></span> <span data-ttu-id="5b43b-110">Le tableau suivant décrit Moniteur réseau interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="5b43b-110">The following table describes Network Monitor NPP interfaces.</span></span>



| <span data-ttu-id="5b43b-111">Interface</span><span class="sxs-lookup"><span data-stu-id="5b43b-111">Interface</span></span>                | <span data-ttu-id="5b43b-112">Description</span><span class="sxs-lookup"><span data-stu-id="5b43b-112">Description</span></span>                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b43b-113">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="5b43b-113">IDelaydC</span></span>](idelaydc.md) | <span data-ttu-id="5b43b-114">Capture le trafic réseau qui est stocké dans un fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="5b43b-114">Captures network traffic that is stored in a capture file.</span></span> <span data-ttu-id="5b43b-115">Cette interface est utilisée par les applications Moniteur réseau et NPP.</span><span class="sxs-lookup"><span data-stu-id="5b43b-115">This interface is used by Network Monitor and NPP applications.</span></span>                                          |
| [<span data-ttu-id="5b43b-116">IESP</span><span class="sxs-lookup"><span data-stu-id="5b43b-116">IESP</span></span>](iesp.md)         | <span data-ttu-id="5b43b-117">Capture le trafic réseau qui est stocké dans un fichier de capture et fournit des statistiques améliorées dans un format de fichier ESP spécial.</span><span class="sxs-lookup"><span data-stu-id="5b43b-117">Captures network traffic that is stored in a capture file and provides enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="5b43b-118">Cette interface est utilisée par les applications NPP</span><span class="sxs-lookup"><span data-stu-id="5b43b-118">This interface is used by NPP applications</span></span> |
| [<span data-ttu-id="5b43b-119">IRTC</span><span class="sxs-lookup"><span data-stu-id="5b43b-119">IRTC</span></span>](irtc.md)         | <span data-ttu-id="5b43b-120">Capture le trafic réseau en temps réel et déclenche des événements lorsqu’ils se produisent.</span><span class="sxs-lookup"><span data-stu-id="5b43b-120">Captures real time network traffic and triggers events when they occur.</span></span> <span data-ttu-id="5b43b-121">Cette interface est utilisée par les [*analyses*](m.md) et les applications NPP.</span><span class="sxs-lookup"><span data-stu-id="5b43b-121">This interface is used by [*monitors*](m.md) and NPP applications.</span></span>     |
| [<span data-ttu-id="5b43b-122">IStats</span><span class="sxs-lookup"><span data-stu-id="5b43b-122">IStats</span></span>](istats.md)     | <span data-ttu-id="5b43b-123">Récupère des statistiques sous forme de données brutes plutôt que de frames.</span><span class="sxs-lookup"><span data-stu-id="5b43b-123">Retrieves statistics as raw data rather than frames.</span></span> <span data-ttu-id="5b43b-124">Cette interface est utilisée par les applications NPP telles que [*Perfmon*](p.md).</span><span class="sxs-lookup"><span data-stu-id="5b43b-124">This interface is used by NPP applications such as [*Perfmon*](p.md).</span></span>                     |



 

 

 



