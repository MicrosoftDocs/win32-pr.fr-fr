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
# <a name="enumerations-peer-infrastructure"></a>Énumérations (infrastructure homologue)

En utilisant des énumérations, vous pouvez obtenir une liste de toutes les entités homologues spécifiques qui correspondent à vos critères.

**Pour obtenir une énumération et récupérer les résultats**

1.  Obtenez un handle pour l’énumération. Appelez une fonction **PeerEnum** , par exemple, appelez la fonction de représentation graphique d’homologue [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) . Les fonctions **PeerEnum** créent l’énumération et retournent un handle vers cette énumération à l’application appelante. Ce descripteur doit être utilisé pour récupérer les résultats.
2.  Vous pouvez également obtenir le nombre d’entités dans l’énumération. Appelez une fonction **GetItemCount** , par exemple, appelez [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) ou [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).
    > [!Note]  
    > Vous pouvez utiliser la valeur retournée par la fonction **GetItemCount** pour déterminer le nombre d’éléments pouvant être récupérés.

     

3.  Récupérez un groupe de résultats. Appelez une fonction **GetNextItem** , par exemple, appelez [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).
    > [!Note]  
    > Quand une application appelle une fonction **GetNextItem** , elle spécifie le nombre d’entités à retourner, puis la fonction retourne un pointeur vers un tableau de pointeurs vers les entités, et le nombre d’entités, qui est toujours inférieur ou égal au nombre spécifié. Une application peut être amenée à appeler cette fonction plusieurs fois, jusqu’à ce que le nombre d’entités retournées soit inférieur au nombre demandé.

     

4.  Une fois que les données ne sont pas nécessaires, libérez le pointeur vers les données. Appelez une fonction **FreeData** , par exemple, appelez [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) ou [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).
    > [!Note]  
    > Pour plus d’informations, consultez [libération de données homologues](freeing-peer-data.md).

     

5.  Une fois que l’application n’a pas besoin du descripteur de l’énumération, libérez-la. Appelez une fonction **EndEnumeration** , par exemple, appelez [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) ou [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).

## <a name="example-of-an-enumeration"></a>Exemple d’énumération

L’extrait de code suivant montre comment énumérer les identités disponibles.


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



 

 



