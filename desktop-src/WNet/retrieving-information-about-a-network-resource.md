---
title: Récupération d’informations sur une ressource réseau
description: Pour identifier le fournisseur réseau qui possède une ressource, une application peut appeler la fonction WNetGetResourceInformation, comme illustré dans l’exemple de code suivant.
ms.assetid: 4bddb55c-181d-4c6f-bd92-9c27d6b894bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf21e48be540f5307fc1ebd2359aea7ff03cbe0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101968"
---
# <a name="retrieving-information-about-a-network-resource"></a>Récupération d’informations sur une ressource réseau

Pour identifier le fournisseur réseau qui possède une ressource, une application peut appeler la fonction [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , comme illustré dans l’exemple de code suivant.

L’exemple suivant est une fonction (CheckServer) qui prend un nom de serveur en tant que paramètre et retourne des informations sur ce serveur. Tout d’abord, la fonction appelle la fonction [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) pour initialiser le contenu d’un bloc de mémoire à zéro. L’exemple appelle ensuite la fonction [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) , en spécifiant une mémoire tampon suffisamment grande pour contenir uniquement une structure [**Resource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) . La routine comprend le traitement des erreurs pour gérer le cas où une mémoire tampon de cette taille est insuffisante pour contenir les chaînes de longueur variable auxquelles les membres de la structure de la **ressource Resource** pointent. Si cette erreur se produit, l’exemple alloue suffisamment de mémoire et appelle à nouveau **WNetGetResourceInformation** . Enfin, l’exemple libère la mémoire allouée.

Notez que l’exemple suppose que le paramètre *pszServer* pointe vers un nom de serveur que l’un des fournisseurs de réseau de l’ordinateur local reconnaît.


```C++
#include <Windows.h>
#include <Winnetwk.h >

// Need to link with Mpr.lib
#pragma comment(lib, "Mpr.lib")
//
// Verify a server on the network. 
//
DWORD
CheckServer( LPTSTR pszServer )
{  
    DWORD dwBufferSize = sizeof(NETRESOURCE);
    LPBYTE lpBuffer;                  // buffer
    NETRESOURCE nr;
    LPTSTR pszSystem = NULL;          // variable-length strings

    //
    // Set the block of memory to zero; then initialize
    // the NETRESOURCE structure. 
    //
    ZeroMemory(&nr, sizeof(nr));

    nr.dwScope       = RESOURCE_GLOBALNET;
    nr.dwType        = RESOURCETYPE_ANY;
    nr.lpRemoteName  = pszServer;

    //
    // First call the WNetGetResourceInformation function with 
    // memory allocated to hold only a NETRESOURCE structure. This 
    // method can succeed if all the NETRESOURCE pointers are NULL.
    // If the call fails because the buffer is too small, allocate
    // a larger buffer.
    //
    lpBuffer = (LPBYTE) malloc( dwBufferSize );
    if (lpBuffer == NULL) 
        return FALSE;

    while ( WNetGetResourceInformation(&nr, lpBuffer, &dwBufferSize, 
                &pszSystem) == ERROR_MORE_DATA)
    {
        lpBuffer = (LPBYTE) realloc(lpBuffer, dwBufferSize);
    }

    // Process the contents of the NETRESOURCE structure and the
    // variable-length strings in lpBuffer and set dwValue. When
    // finished, free the memory.

    free(lpBuffer);

    return TRUE;
}
```



 

 