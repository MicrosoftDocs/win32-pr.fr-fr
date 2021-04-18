---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbe745f0611d184fefd729c04e50635bc4006e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509611"
---
# <a name="iagentcharacterstopall"></a><span data-ttu-id="77093-103">IAgentCharacter :: StopAll</span><span class="sxs-lookup"><span data-stu-id="77093-103">IAgentCharacter::StopAll</span></span>

<span data-ttu-id="77093-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="77093-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

<span data-ttu-id="77093-105">Arrête toutes les animations (requêtes) et les supprime de la file d’attente d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="77093-105">Stops all animations (requests) and removes them from the character's animation queue.</span></span>

<dl> <dt>

<span data-ttu-id="77093-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span><span class="sxs-lookup"><span data-stu-id="77093-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span></span>
</dt> <dd>

<span data-ttu-id="77093-107">Champ de type de code qui indique les types de demandes à arrêter (et à supprimer de la file d’attente du caractère), constitué des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="77093-107">A bitfield that indicates the types of requests to stop (and remove from the character's queue), comprised from the following:</span></span>



|                                                                                   |                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77093-108">**const type d’arrêt long non signé** **\_ \_ = 0xFFFFFFFF ;**</span><span class="sxs-lookup"><span data-stu-id="77093-108">**const unsigned long** **STOP\_TYPE\_ALL = 0xFFFFFFFF;**</span></span><br/>              | <span data-ttu-id="77093-109">Arrête toutes les demandes d’animation, y compris les demandes de [**préparation**](iagentcharacter--prepare.md) non mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="77093-109">Stops all animation requests, including non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span> |
| <span data-ttu-id="77093-110">**const type d’arrêt long non signé** **\_ \_ lu = 0x00000001 ;**</span><span class="sxs-lookup"><span data-stu-id="77093-110">**const unsigned long** **STOP\_TYPE\_PLAY = 0x00000001;**</span></span><br/>             | <span data-ttu-id="77093-111">Arrête toutes les demandes de lecture.</span><span class="sxs-lookup"><span data-stu-id="77093-111">Stops all Play requests.</span></span>                                                                                 |
| <span data-ttu-id="77093-112">**const type d’arrêt long non signé** **\_ \_ Move = 0x00000002 ;**</span><span class="sxs-lookup"><span data-stu-id="77093-112">**const unsigned long** **STOP\_TYPE\_MOVE = 0x00000002;**</span></span><br/>             | <span data-ttu-id="77093-113">Arrête toutes les demandes de [**déplacement**](https://www.bing.com/search?q=**Move**) .</span><span class="sxs-lookup"><span data-stu-id="77093-113">Stops all [**Move**](https://www.bing.com/search?q=**Move**) requests.</span></span>                                               |
| <span data-ttu-id="77093-114">**const type d’arrêt long non signé** **\_ \_ Speak = 0x00000004 ;**</span><span class="sxs-lookup"><span data-stu-id="77093-114">**const unsigned long** **STOP\_TYPE\_SPEAK = 0x00000004;**</span></span><br/>            | <span data-ttu-id="77093-115">Arrête toutes les demandes [**Speak**](iagentcharacter--speak.md) .</span><span class="sxs-lookup"><span data-stu-id="77093-115">Stops all [**Speak**](iagentcharacter--speak.md) requests.</span></span>                                              |
| <span data-ttu-id="77093-116">**const unsigned long** **Stop \_ type \_ Prepare = 0x00000008 ;**</span><span class="sxs-lookup"><span data-stu-id="77093-116">**const unsigned long** **STOP\_TYPE\_PREPARE = 0x00000008;**</span></span><br/>          | <span data-ttu-id="77093-117">Arrête toutes les demandes de [**préparation**](iagentcharacter--prepare.md) mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="77093-117">Stops all queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                                   |
| <span data-ttu-id="77093-118">**const, unsigned long** **Stop \_ \_ , type NONQUEUEDPREPARE = 0x00000010 ;**</span><span class="sxs-lookup"><span data-stu-id="77093-118">**const unsigned long** **STOP\_TYPE\_NONQUEUEDPREPARE = 0x00000010;**</span></span><br/> | <span data-ttu-id="77093-119">Arrête toutes les demandes de [**préparation**](iagentcharacter--prepare.md) non mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="77093-119">Stops all non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                               |
| <span data-ttu-id="77093-120">type d’arrêt **long non signé const** **\_ \_ visible = 0x00000020 ;**</span><span class="sxs-lookup"><span data-stu-id="77093-120">**const unsigned long** **STOP\_TYPE\_VISIBLE = 0x00000020;**</span></span><br/>          | <span data-ttu-id="77093-121">Arrête toutes les demandes d' [**affichage**](iagentcharacter--show.md) ou de [**masquage**](iagentcharacter--hide.md) .</span><span class="sxs-lookup"><span data-stu-id="77093-121">Stops all [**Hide**](iagentcharacter--hide.md) or [**Show**](iagentcharacter--show.md) requests.</span></span>       |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="77093-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77093-122">See Also</span></span>

[<span data-ttu-id="77093-123">**IAgentCharacter :: Stop**</span><span class="sxs-lookup"><span data-stu-id="77093-123">**IAgentCharacter::Stop**</span></span>](iagentcharacter--stop.md)


 

 





