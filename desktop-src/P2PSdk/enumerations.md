---
title: Énumérations (infrastructure homologue)
description: En utilisant des énumérations, vous pouvez obtenir une liste de toutes les entités homologues spécifiques qui correspondent à vos critères.
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90a6806c9fdf7b776980abbaaa3f28643c49360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518689"
---
# <a name="enumerations-peer-infrastructure"></a><span data-ttu-id="b4383-103">Énumérations (infrastructure homologue)</span><span class="sxs-lookup"><span data-stu-id="b4383-103">Enumerations (Peer Infrastructure)</span></span>

<span data-ttu-id="b4383-104">En utilisant des énumérations, vous pouvez obtenir une liste de toutes les entités homologues spécifiques qui correspondent à vos critères.</span><span class="sxs-lookup"><span data-stu-id="b4383-104">By using Enumerations, you can obtain a list of all the specific peer entities that match your criteria.</span></span>

<span data-ttu-id="b4383-105">**Pour obtenir une énumération et récupérer les résultats**</span><span class="sxs-lookup"><span data-stu-id="b4383-105">**To obtain an enumeration and retrieve the results**</span></span>

1.  <span data-ttu-id="b4383-106">Obtenez un handle pour l’énumération.</span><span class="sxs-lookup"><span data-stu-id="b4383-106">Obtain a handle to the enumeration.</span></span> <span data-ttu-id="b4383-107">Appelez une fonction **PeerEnum** , par exemple, appelez la fonction de représentation graphique d’homologue [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) .</span><span class="sxs-lookup"><span data-stu-id="b4383-107">Call a **PeerEnum** function, for example, call the [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) Peer Graphing function.</span></span> <span data-ttu-id="b4383-108">Les fonctions **PeerEnum** créent l’énumération et retournent un handle vers cette énumération à l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="b4383-108">The **PeerEnum** functions create the enumeration, and return a handle to that enumeration to the calling application.</span></span> <span data-ttu-id="b4383-109">Ce descripteur doit être utilisé pour récupérer les résultats.</span><span class="sxs-lookup"><span data-stu-id="b4383-109">This handle must be used to retrieve the results.</span></span>
2.  <span data-ttu-id="b4383-110">Vous pouvez également obtenir le nombre d’entités dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="b4383-110">Optionally, obtain the number of entities in the enumeration.</span></span> <span data-ttu-id="b4383-111">Appelez une fonction **GetItemCount** , par exemple, appelez [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) ou [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span><span class="sxs-lookup"><span data-stu-id="b4383-111">Call a **GetItemCount** function, for example, call [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) or [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span></span>
    > [!Note]  
    > <span data-ttu-id="b4383-112">Vous pouvez utiliser la valeur retournée par la fonction **GetItemCount** pour déterminer le nombre d’éléments pouvant être récupérés.</span><span class="sxs-lookup"><span data-stu-id="b4383-112">You can use the value returned by the **GetItemCount** function to determine the number of items available to retrieve.</span></span>

     

3.  <span data-ttu-id="b4383-113">Récupérez un groupe de résultats.</span><span class="sxs-lookup"><span data-stu-id="b4383-113">Retrieve a group of results.</span></span> <span data-ttu-id="b4383-114">Appelez une fonction **GetNextItem** , par exemple, appelez [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span><span class="sxs-lookup"><span data-stu-id="b4383-114">Call a **GetNextItem** function, for example, call [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span></span>
    > [!Note]  
    > <span data-ttu-id="b4383-115">Quand une application appelle une fonction **GetNextItem** , elle spécifie le nombre d’entités à retourner, puis la fonction retourne un pointeur vers un tableau de pointeurs vers les entités, et le nombre d’entités, qui est toujours inférieur ou égal au nombre spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4383-115">When an application calls a **GetNextItem** function, it specifies the number of entities to return, and then the function returns a pointer to an array of pointers to the entities, and the number of entities, which is always less than or equal to the number specified.</span></span> <span data-ttu-id="b4383-116">Une application peut être amenée à appeler cette fonction plusieurs fois, jusqu’à ce que le nombre d’entités retournées soit inférieur au nombre demandé.</span><span class="sxs-lookup"><span data-stu-id="b4383-116">An application might need to call this function many times—until the number of entities returned is less than the number requested.</span></span>

     

4.  <span data-ttu-id="b4383-117">Une fois que les données ne sont pas nécessaires, libérez le pointeur vers les données.</span><span class="sxs-lookup"><span data-stu-id="b4383-117">After the data is not needed, free the pointer to the data.</span></span> <span data-ttu-id="b4383-118">Appelez une fonction **FreeData** , par exemple, appelez [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) ou [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span><span class="sxs-lookup"><span data-stu-id="b4383-118">Call a **FreeData** function, for example, call [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span>
    > [!Note]  
    > <span data-ttu-id="b4383-119">Pour plus d’informations, consultez [libération de données homologues](freeing-peer-data.md).</span><span class="sxs-lookup"><span data-stu-id="b4383-119">For more information, see [Freeing Peer Data](freeing-peer-data.md).</span></span>

     

5.  <span data-ttu-id="b4383-120">Une fois que l’application n’a pas besoin du descripteur de l’énumération, libérez-la.</span><span class="sxs-lookup"><span data-stu-id="b4383-120">After the application does not need the handle to the enumeration, release it.</span></span> <span data-ttu-id="b4383-121">Appelez une fonction **EndEnumeration** , par exemple, appelez [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) ou [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span><span class="sxs-lookup"><span data-stu-id="b4383-121">Call an **EndEnumeration** function, for example, call [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) or [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span></span>

## <a name="example-of-an-enumeration"></a><span data-ttu-id="b4383-122">Exemple d’énumération</span><span class="sxs-lookup"><span data-stu-id="b4383-122">Example of an Enumeration</span></span>

<span data-ttu-id="b4383-123">L’extrait de code suivant montre comment énumérer les identités disponibles.</span><span class="sxs-lookup"><span data-stu-id="b4383-123">The following code snippet shows you how to enumerate through available identities.</span></span>


```C++
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: EnumIdentities
//
// Purpose:  Demonstrate how to enumerate identities.
//
// Returns:  HRESULT
//

HRESULT EnumIdentities(void)
{
    HPEERENUM hPeerEnum = NULL;
    HRESULT hr = PeerEnumIdentities(&hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cIdentities = 0;
        hr = PeerGetItemCount(hPeerEnum, &cIdentities);

        if (SUCCEEDED(hr))
        {
            ULONG i;

            for (i = 0; i < cIdentities; i++)
            {
                ULONG cItem = 1; // process one result at a time
                PEER_NAME_PAIR ** ppNamePair = NULL; // pointer to an array of pointers

                hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNamePair);

                if (SUCCEEDED(hr) && (1 == cItem))
                {
                    wprintf(L"%s [%s]\r\n", (*ppNamePair)->pwzFriendlyName, (*ppNamePair)->pwzPeerName);
                    PeerFreeData(ppNamePair);
                }
            }
        }
        PeerEndEnumeration(hPeerEnum);
    }
 
    return hr;
}
```



 

 



