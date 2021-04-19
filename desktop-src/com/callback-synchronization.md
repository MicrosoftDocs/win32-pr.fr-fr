---
title: Synchronisation des rappels
description: Synchronisation des rappels
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c274c35a6df176f65c505f2a3fecc9a53a20e5d9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106511714"
---
# <a name="callback-synchronization"></a><span data-ttu-id="1f514-103">Synchronisation des rappels</span><span class="sxs-lookup"><span data-stu-id="1f514-103">Callback Synchronization</span></span>

<span data-ttu-id="1f514-104">L' [API WinInet](/windows/desktop/WinInet/portal) asynchrone (utilisée pour les protocoles les plus courants) laisse la synchronisation du mécanisme de rappel et de l’application appelante en tant qu’exercice pour le client.</span><span class="sxs-lookup"><span data-stu-id="1f514-104">The asynchronous [WinInet API](/windows/desktop/WinInet/portal) (used for the most common protocols) leaves the synchronization of the callback mechanism and the calling application as an exercise for the client.</span></span> <span data-ttu-id="1f514-105">Cette opération est intentionnelle car elle offre le plus grand degré de flexibilité.</span><span class="sxs-lookup"><span data-stu-id="1f514-105">This is intentional because it allows the greatest degree of flexibility.</span></span> <span data-ttu-id="1f514-106">Les protocoles par défaut et l’implémentation du moniker d’URL effectuent cette synchronisation et garantissent que les applications à thread unique et à thread cloisonné n’ont jamais à gérer la contention de style thread libre.</span><span class="sxs-lookup"><span data-stu-id="1f514-106">The default protocols and the URL moniker implementation perform this synchronization and guarantee that single-threaded and apartment-threaded applications never have to deal with free-thread-style contention.</span></span> <span data-ttu-id="1f514-107">Autrement dit, les interfaces [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) et [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) du client sont appelées uniquement sur leurs threads appropriés.</span><span class="sxs-lookup"><span data-stu-id="1f514-107">That is, the client's [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) and [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) interfaces are called only on their proper threads.</span></span> <span data-ttu-id="1f514-108">Cette fonctionnalité est transparente pour l’utilisateur de l’URL mMoniker tant que chaque thread qui appelle [**IMoniker :: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) et [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) a une file d’attente de messages.</span><span class="sxs-lookup"><span data-stu-id="1f514-108">This feature is transparent to the user of the URL mMoniker as long each thread that calls [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) and [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) has a message queue.</span></span>

<span data-ttu-id="1f514-109">La spécification du moniker asynchrone requiert un contrôle plus précis de la définition des priorités et de la gestion des téléchargements que ce qui est autorisé par WinSock ou WinInet.</span><span class="sxs-lookup"><span data-stu-id="1f514-109">The asynchronous moniker specification requires more precise control over the prioritization and management of downloads than is allowed for by either WinSock or WinInet.</span></span> <span data-ttu-id="1f514-110">En conséquence, un moniker d’URL gère tous les téléchargements pour tout thread appelant donné, en utilisant (dans le cadre de sa synchronisation) un schéma de priorité basé sur la spécification [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1f514-110">Accordingly, a URL moniker manages all the downloads for any given caller's thread, using (as part of its synchronization) a priority scheme based on the [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) specification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f514-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f514-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f514-112">Monikers d’URL</span><span class="sxs-lookup"><span data-stu-id="1f514-112">URL Monikers</span></span>](url-monikers.md)
</dt> </dl>

 

 