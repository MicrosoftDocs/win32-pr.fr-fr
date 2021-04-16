---
title: Stockage asynchrone et synchrone
description: Stockage asynchrone et synchrone
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508162"
---
# <a name="asynchronous-and-synchronous-storage"></a><span data-ttu-id="7edf6-103">Stockage asynchrone et synchrone</span><span class="sxs-lookup"><span data-stu-id="7edf6-103">Asynchronous and Synchronous Storage</span></span>

<span data-ttu-id="7edf6-104">Les monikers asynchrones peuvent également retourner un objet de [stockage asynchrone](/windows/desktop/Stg/asynchronous-storage) dans la notification [**IBindStatusCallback :: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7edf6-104">Asynchronous monikers may also return an [Asynchronous Storage](/windows/desktop/Stg/asynchronous-storage) object in the [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) notification.</span></span> <span data-ttu-id="7edf6-105">Cet objet de stockage peut autoriser l’accès à certaines données persistantes de l’objet pendant que la liaison est toujours en cours.</span><span class="sxs-lookup"><span data-stu-id="7edf6-105">This storage object may allow access to some of the object's persistent data while the binding is still in progress.</span></span> <span data-ttu-id="7edf6-106">Un client peut choisir entre deux modes de stockage : blocage et non-blocage.</span><span class="sxs-lookup"><span data-stu-id="7edf6-106">A client can choose between two modes for the storage: blocking and nonblocking.</span></span>

<span data-ttu-id="7edf6-107">En mode blocage, qui est compatible avec les implémentations actuelles des objets de stockage, si les données ne sont pas disponibles, l’appel est bloqué jusqu’à l’arrivée des données.</span><span class="sxs-lookup"><span data-stu-id="7edf6-107">In blocking mode, which is compatible with current implementations of storage objects, if data is unavailable, the call blocks until data arrives.</span></span> <span data-ttu-id="7edf6-108">En mode non bloquant, au lieu de bloquer l’appel, l’objet de stockage retourne une nouvelle erreur E \_ en attente lorsque les données ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="7edf6-108">In nonblocking mode, rather than blocking the call, the storage object returns a new error E\_PENDING when data is unavailable.</span></span> <span data-ttu-id="7edf6-109">Un client connaissant la liaison et le stockage asynchrones note cette erreur et attend d’autres notifications ([**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) pour retenter l’opération.</span><span class="sxs-lookup"><span data-stu-id="7edf6-109">A client aware of asynchronous binding and storage notes this error and waits for further notifications ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) to retry the operation.</span></span> <span data-ttu-id="7edf6-110">Un client peut choisir entre un stockage synchrone (blocage) et un stockage asynchrone (sans blocage) en choisissant de définir l' \_ indicateur BINDF ASYNCSTORAGE dans la valeur *grfBINDF* retournée à [**IBindStatusCallback :: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7edf6-110">A client can choose between a synchronous (blocking) and asynchronous (nonblocking) storage by choosing whether to set the BINDF\_ASYNCSTORAGE flag in the *grfBINDF* value returned to [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7edf6-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7edf6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7edf6-112">Monikers asynchrones</span><span class="sxs-lookup"><span data-stu-id="7edf6-112">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 