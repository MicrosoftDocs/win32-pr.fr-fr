---
title: Énumération ConnectionStatus
description: Représente l’état de l’appareil dans le réseau en dernier vu.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- API de diffusion multimédia par l’énumération ConnectionStatus
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540481"
---
# <a name="connectionstatus-enumeration"></a><span data-ttu-id="0be47-104">Énumération ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="0be47-104">ConnectionStatus enumeration</span></span>

<span data-ttu-id="0be47-105">Représente l’état de l’appareil dans le réseau en dernier vu.</span><span class="sxs-lookup"><span data-stu-id="0be47-105">Represents the state of the device in the network as last seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be47-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0be47-106">Syntax</span></span>


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a><span data-ttu-id="0be47-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="0be47-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0be47-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Service**</span><span class="sxs-lookup"><span data-stu-id="0be47-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Online**</span></span>
</dt> <dd>

<span data-ttu-id="0be47-109">L’appareil est en ligne et actif sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="0be47-109">Device is online and active on the network.</span></span>

</dd> <dt>

<span data-ttu-id="0be47-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion**</span><span class="sxs-lookup"><span data-stu-id="0be47-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline**</span></span>
</dt> <dd>

<span data-ttu-id="0be47-111">L’appareil est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="0be47-111">Device is offline.</span></span>

</dd> <dt>

<span data-ttu-id="0be47-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**En veille**</span><span class="sxs-lookup"><span data-stu-id="0be47-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Sleeping**</span></span>
</dt> <dd>

<span data-ttu-id="0be47-113">L’appareil est actuellement hors connexion, mais peut se réveiller automatiquement lorsqu’une tentative est faite pour communiquer avec lui.</span><span class="sxs-lookup"><span data-stu-id="0be47-113">Device is currently offline but might automatically wake up when an attempt is made to communicate with it.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0be47-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0be47-114">Requirements</span></span>



| <span data-ttu-id="0be47-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0be47-115">Requirement</span></span> | <span data-ttu-id="0be47-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0be47-116">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0be47-117">MIDL</span><span class="sxs-lookup"><span data-stu-id="0be47-117">IDL</span></span><br/> | <dl> <span data-ttu-id="0be47-118"><dt>Windows. Media. streaming. idl (référence Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="0be47-118"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





