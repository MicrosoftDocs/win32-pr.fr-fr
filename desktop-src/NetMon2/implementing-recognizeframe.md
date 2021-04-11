---
description: Les analyses réseau appellent la fonction RecognizeFrame d’un analyseur pour déterminer que l’analyseur reconnaît les données non réclamées d’une trame.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implémentation de RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970eee80a04168b3fa06b117c2c219c506da7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320554"
---
# <a name="implementing-recognizeframe"></a><span data-ttu-id="73ec4-103">Implémentation de RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="73ec4-103">Implementing RecognizeFrame</span></span>

<span data-ttu-id="73ec4-104">Les analyses réseau appellent la fonction [**RecognizeFrame**](recognizeframe.md) d’un analyseur pour déterminer que l’analyseur reconnaît les données non réclamées d’une trame.</span><span class="sxs-lookup"><span data-stu-id="73ec4-104">Network Monitors calls the [**RecognizeFrame**](recognizeframe.md) function of a parser to determine that the parser recognizes the unclaimed data of a frame.</span></span> <span data-ttu-id="73ec4-105">Les données non réclamées peuvent se trouver au début d’une image, mais en général, les données non réclamées se trouvent au milieu d’une trame.</span><span class="sxs-lookup"><span data-stu-id="73ec4-105">The unclaimed data may be at the start of a frame, but typically, unclaimed data is located in the middle of a frame.</span></span> <span data-ttu-id="73ec4-106">L’illustration suivante montre les données inutilisées situées au milieu d’une trame.</span><span class="sxs-lookup"><span data-stu-id="73ec4-106">The following illustration shows unclaimed data located in the middle of a frame.</span></span>

![données libérées situées au milieu d’une trame](images/recognizeframe1.png)

<span data-ttu-id="73ec4-108">Moniteur réseau fournit les informations suivantes quand il appelle la fonction [**RecognizeFrame**](recognizeframe.md) :</span><span class="sxs-lookup"><span data-stu-id="73ec4-108">Network Monitor provides the following information when it calls the [**RecognizeFrame**](recognizeframe.md) function:</span></span>

-   <span data-ttu-id="73ec4-109">Handle du frame.</span><span class="sxs-lookup"><span data-stu-id="73ec4-109">A handle to the frame.</span></span>
-   <span data-ttu-id="73ec4-110">Pointeur vers le début du frame.</span><span class="sxs-lookup"><span data-stu-id="73ec4-110">A pointer to the start of the frame.</span></span>
-   <span data-ttu-id="73ec4-111">Pointeur vers le début des données inrécupérées.</span><span class="sxs-lookup"><span data-stu-id="73ec4-111">A pointer to the start of the unclaimed data.</span></span>
-   <span data-ttu-id="73ec4-112">Valeur MAC du premier protocole dans le frame.</span><span class="sxs-lookup"><span data-stu-id="73ec4-112">The MAC value of the first protocol in the frame.</span></span>
-   <span data-ttu-id="73ec4-113">Nombre d’octets dans les données inrécupérées ; autrement dit, les octets restants dans le frame.</span><span class="sxs-lookup"><span data-stu-id="73ec4-113">The number of bytes in the unclaimed data; that is, the bytes remaining in the frame.</span></span>
-   <span data-ttu-id="73ec4-114">Handle du protocole précédent.</span><span class="sxs-lookup"><span data-stu-id="73ec4-114">A handle to the previous protocol.</span></span>
-   <span data-ttu-id="73ec4-115">Offset du protocole précédent.</span><span class="sxs-lookup"><span data-stu-id="73ec4-115">The offset of the previous protocol.</span></span>

<span data-ttu-id="73ec4-116">Lorsque la DLL de l’analyseur détermine que les données non réclamées commencent par le protocole de l’analyseur, la DLL de l’analyseur détermine l’emplacement de démarrage du protocole suivant et le protocole qui suit.</span><span class="sxs-lookup"><span data-stu-id="73ec4-116">When the parser DLL determines that unclaimed data starts with the parser protocol, the parser DLL determines where the next protocol starts, and which protocol follows.</span></span> <span data-ttu-id="73ec4-117">La DLL de l’analyseur fonctionne de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="73ec4-117">The parser DLL functions in the following conditional ways:</span></span>

-   <span data-ttu-id="73ec4-118">Si la DLL de l’analyseur reconnaît des données non réclamées, la DLL de l’analyseur définit le paramètre *pProtocolStatus* et retourne un pointeur vers le protocole suivant dans le frame ou la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="73ec4-118">If the parser DLL recognizes unclaimed data, the parser DLL sets the *pProtocolStatus* parameter, and returns a pointer to either the next protocol in the frame, or **NULL**.</span></span> <span data-ttu-id="73ec4-119">La **valeur null** est retournée si le protocole actuel est le dernier protocole dans le frame.</span><span class="sxs-lookup"><span data-stu-id="73ec4-119">**NULL** is returned if the current protocol is the last protocol in the frame.</span></span>
-   <span data-ttu-id="73ec4-120">Si la DLL de l’analyseur reconnaît les données non réclamées et identifie le protocole qui suit (à partir des informations fournies dans le protocole), la DLL de l’analyseur retourne un pointeur vers le descripteur du protocole suivant dans le paramètre *phNextProtocol* de la fonction.</span><span class="sxs-lookup"><span data-stu-id="73ec4-120">If the parser DLL recognizes unclaimed data and identifies the protocol that follows (from information provided in the protocol), then the parser DLL returns a pointer to the handle of the next protocol in the *phNextProtocol* parameter of the function.</span></span>
-   <span data-ttu-id="73ec4-121">Si la DLL de l’analyseur ne reconnaît pas les données non réclamées, la DLL de l’analyseur retourne le pointeur au début des données non réclamées et Moniteur réseau continue d’analyser les données non réclamées.</span><span class="sxs-lookup"><span data-stu-id="73ec4-121">If the parser DLL does not recognize unclaimed data, the parser DLL returns the pointer to the start of unclaimed data, and Network Monitor continues trying to parse the unclaimed data.</span></span>

<span data-ttu-id="73ec4-122">**Pour implémenter RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="73ec4-122">**To implement RecognizeFrame**</span></span>

1.  <span data-ttu-id="73ec4-123">Testez pour déterminer que vous avez reconnu le protocole.</span><span class="sxs-lookup"><span data-stu-id="73ec4-123">Test to determine that you recognize the protocol.</span></span>
2.  <span data-ttu-id="73ec4-124">Si vous reconnaissez des données non réclamées et que vous connaissez le protocole qui suit, définissez *pProtocolStatus* sur protocole \_ Status \_ Next \_ Protocol, définissez *phNextProtocol* sur un pointeur qui pointe vers le handle pour le protocole suivant, puis renvoyez un pointeur vers le protocole suivant.</span><span class="sxs-lookup"><span data-stu-id="73ec4-124">If you recognize unclaimed data and you know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_NEXT\_PROTOCOL, set *phNextProtocol* to a pointer that points to the handle for the next protocol, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="73ec4-125">–ou–</span><span class="sxs-lookup"><span data-stu-id="73ec4-125">–or–</span></span>

    <span data-ttu-id="73ec4-126">Si vous reconnaissez des données non réclamées et que vous ne connaissez pas le protocole qui suit, affectez à *pProtocolStatus* la valeur État de protocole \_ \_ reconnu, puis renvoyez un pointeur au protocole suivant.</span><span class="sxs-lookup"><span data-stu-id="73ec4-126">If you recognize unclaimed data and you do not know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_RECOGNIZED, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="73ec4-127">–ou–</span><span class="sxs-lookup"><span data-stu-id="73ec4-127">–or–</span></span>

    <span data-ttu-id="73ec4-128">Si vous reconnaissez des données non réclamées et que votre protocole est le dernier protocole d’une trame, définissez *pProtocolStatus* sur l’état du protocole \_ \_ revendiqué, puis retournez la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="73ec4-128">If you recognize unclaimed data and your protocol is the last protocol in a frame, set *pProtocolStatus* to PROTOCOL\_STATUS\_CLAIMED, and then return **NULL**.</span></span>

    <span data-ttu-id="73ec4-129">–ou–</span><span class="sxs-lookup"><span data-stu-id="73ec4-129">–or–</span></span>

    <span data-ttu-id="73ec4-130">Si vous ne reconnaissez pas les données non réclamées, affectez à *pProtocolStatus* la valeur État du protocole \_ \_ non \_ reconnu, puis renvoyez le pointeur qui vous est transmis dans *pProtocol*.</span><span class="sxs-lookup"><span data-stu-id="73ec4-130">If you do not recognize unclaimed data, set *pProtocolStatus* to PROTOCOL\_STATUS\_NOT\_RECOGNIZED, and then return the pointer that is passed to you in *pProtocol*.</span></span>

<span data-ttu-id="73ec4-131">Voici une implémentation de base de [**RecognizeFrame**](recognizeframe.md).</span><span class="sxs-lookup"><span data-stu-id="73ec4-131">The following is a basic implementation of [**RecognizeFrame**](recognizeframe.md).</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



