---
title: Ping
description: Utilisez le paquet ping pour établir une connexion et négocier la sécurité avec le serveur.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- BITS ping
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "106510449"
---
# <a name="ping"></a><span data-ttu-id="7bebb-104">Ping</span><span class="sxs-lookup"><span data-stu-id="7bebb-104">Ping</span></span>

<span data-ttu-id="7bebb-105">Utilisez le paquet **ping** pour établir une connexion et négocier la sécurité avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="7bebb-105">Use the **Ping** packet to establish a connection and negotiate security with the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a><span data-ttu-id="7bebb-106">headers</span><span class="sxs-lookup"><span data-stu-id="7bebb-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="7bebb-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_publication bits</span><span class="sxs-lookup"><span data-stu-id="7bebb-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="7bebb-108">Verbe spécifique à BITS qui identifie ce paquet auprès du serveur BITS.</span><span class="sxs-lookup"><span data-stu-id="7bebb-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="7bebb-109">Remplacez l’URL distante par l’URI absolu ou relatif.</span><span class="sxs-lookup"><span data-stu-id="7bebb-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="7bebb-110">Remplacez généralement l’URL distante par le nom de fichier distant du travail.</span><span class="sxs-lookup"><span data-stu-id="7bebb-110">Typically, replace remote-URL with the remote file name of the job.</span></span>

</dd> <dt>

<span data-ttu-id="7bebb-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-type</span><span class="sxs-lookup"><span data-stu-id="7bebb-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="7bebb-112">Identifie ce paquet de requête en tant que paquet ping.</span><span class="sxs-lookup"><span data-stu-id="7bebb-112">Identifies this request packet as a Ping packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bebb-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7bebb-113">Remarks</span></span>

<span data-ttu-id="7bebb-114">Le paquet **ping** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="7bebb-114">The **Ping** packet is optional.</span></span> <span data-ttu-id="7bebb-115">Au lieu d’envoyer un paquet **ping** , vous pouvez utiliser le paquet [**Create-session**](create-session.md) pour établir une connexion et négocier la sécurité.</span><span class="sxs-lookup"><span data-stu-id="7bebb-115">Instead of sending a **Ping** packet, you can use the [**Create-Session**](create-session.md) packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="7bebb-116">Toutefois, il est plus efficace d’utiliser le paquet **ping** à cet effet.</span><span class="sxs-lookup"><span data-stu-id="7bebb-116">However, it is more efficient to use the **Ping** packet for this purpose.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bebb-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bebb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bebb-118">**ACK pour ping**</span><span class="sxs-lookup"><span data-stu-id="7bebb-118">**Ack for Ping**</span></span>](ack-for-ping.md)
</dt> <dt>

[<span data-ttu-id="7bebb-119">**Créer une session**</span><span class="sxs-lookup"><span data-stu-id="7bebb-119">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




