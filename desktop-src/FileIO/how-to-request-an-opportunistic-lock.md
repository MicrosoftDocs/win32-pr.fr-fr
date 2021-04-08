---
description: Les verrous opportunistes sont demandés en ouvrant un fichier avec les autorisations et les indicateurs appropriés à l’application ouvrant le fichier. Tous les fichiers pour lesquels des verrous opportunistes seront demandés doivent être ouverts pour une opération avec chevauchement (asynchrone).
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: Comment demander un verrou opportuniste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868238"
---
# <a name="how-to-request-an-opportunistic-lock"></a><span data-ttu-id="322f3-104">Comment demander un verrou opportuniste</span><span class="sxs-lookup"><span data-stu-id="322f3-104">How to Request an Opportunistic Lock</span></span>

<span data-ttu-id="322f3-105">Les applications clientes demandent directement des verrous opportunistes uniquement lorsque le verrou est destiné à un fichier sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="322f3-105">Client applications directly request opportunistic locks only when the lock is intended for a file on the local server.</span></span> <span data-ttu-id="322f3-106">Lors de l’accès aux fichiers sur des serveurs distants, il s’agit du redirecteur réseau, et non de l’application cliente, qui demande le verrou opportuniste du serveur distant.</span><span class="sxs-lookup"><span data-stu-id="322f3-106">When accessing files on remote servers, it is the network redirector, and not the client application, that requests the opportunistic lock from the remote server.</span></span>

<span data-ttu-id="322f3-107">Les verrous opportunistes sont demandés en ouvrant un fichier avec les autorisations et les indicateurs appropriés à l’application ouvrant le fichier.</span><span class="sxs-lookup"><span data-stu-id="322f3-107">Opportunistic locks are requested by first opening a file with permissions and flags appropriate to the application opening the file.</span></span> <span data-ttu-id="322f3-108">Tous les fichiers pour lesquels des verrous opportunistes seront demandés doivent être ouverts pour une opération avec chevauchement (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="322f3-108">All files for which opportunistic locks will be requested must be opened for overlapped (asynchronous) operation.</span></span> <span data-ttu-id="322f3-109">Une fois les fichiers ouverts pour une opération avec chevauchement, utilisez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec le code de contrôle approprié pour demander un verrou opportuniste.</span><span class="sxs-lookup"><span data-stu-id="322f3-109">After the files are opened for overlapped operation, use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the appropriate control code to request an opportunistic lock.</span></span> <span data-ttu-id="322f3-110">Pour obtenir la liste des opérations de verrouillage opportuniste, voir [opérations de verrouillage opportuniste](opportunistic-lock-operations.md).</span><span class="sxs-lookup"><span data-stu-id="322f3-110">For a list of the opportunistic lock operations, see [Opportunistic Lock Operations](opportunistic-lock-operations.md).</span></span>

<span data-ttu-id="322f3-111">Les applications sont averties qu’un verrou opportuniste est interrompu à l’aide du membre **hEvent** de la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associée au fichier.</span><span class="sxs-lookup"><span data-stu-id="322f3-111">Applications are notified that an opportunistic lock is broken by using the **hEvent** member of the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the file.</span></span> <span data-ttu-id="322f3-112">Les applications peuvent également utiliser des fonctions telles que [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) et [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span><span class="sxs-lookup"><span data-stu-id="322f3-112">Applications may also use functions such as [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) and [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span></span> <span data-ttu-id="322f3-113">L’application est chargée d’associer le fichier approprié au verrou opportuniste rompu.</span><span class="sxs-lookup"><span data-stu-id="322f3-113">The application is responsible for associating the correct file with the broken opportunistic lock.</span></span>

<span data-ttu-id="322f3-114">Pour plus d’informations sur la notification, consultez [Synchronization](/windows/desktop/Sync/synchronization).</span><span class="sxs-lookup"><span data-stu-id="322f3-114">For more information on notification, see [Synchronization](/windows/desktop/Sync/synchronization).</span></span>

 

 
