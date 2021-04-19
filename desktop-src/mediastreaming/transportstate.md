---
title: Énumération TransportState
description: Définit les États de transport disponibles, comme défini par les instructions UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- API de diffusion multimédia par l’énumération TransportState
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526456"
---
# <a name="transportstate-enumeration"></a><span data-ttu-id="51511-104">Énumération TransportState</span><span class="sxs-lookup"><span data-stu-id="51511-104">TransportState enumeration</span></span>

<span data-ttu-id="51511-105">Définit les États de transport disponibles, comme défini par les instructions UPnP.</span><span class="sxs-lookup"><span data-stu-id="51511-105">Defines the available transport states as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="51511-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51511-106">Syntax</span></span>


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a><span data-ttu-id="51511-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="51511-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="51511-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Connue**</span><span class="sxs-lookup"><span data-stu-id="51511-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="51511-109">État de l’appareil erroné.</span><span class="sxs-lookup"><span data-stu-id="51511-109">Erroneous device state.</span></span>

</dd> <dt>

<span data-ttu-id="51511-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Mis**</span><span class="sxs-lookup"><span data-stu-id="51511-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped**</span></span>
</dt> <dd>

<span data-ttu-id="51511-111">Le transport de l’appareil est à l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="51511-111">The device s transport is in a stopped state.</span></span>

</dd> <dt>

<span data-ttu-id="51511-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Écoute**</span><span class="sxs-lookup"><span data-stu-id="51511-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Playing**</span></span>
</dt> <dd>

<span data-ttu-id="51511-113">Le transport de l’appareil est à l’État en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="51511-113">The device s transport is in a playing state.</span></span>

</dd> <dt>

<span data-ttu-id="51511-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition**</span><span class="sxs-lookup"><span data-stu-id="51511-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning**</span></span>
</dt> <dd>

<span data-ttu-id="51511-115">Le transport de l’appareil est dans un état de transition qui entraîne une autre valeur d’État.</span><span class="sxs-lookup"><span data-stu-id="51511-115">The device s transport is in a transitioning state which will result in another state value.</span></span>

</dd> <dt>

<span data-ttu-id="51511-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Suspendu**</span><span class="sxs-lookup"><span data-stu-id="51511-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused**</span></span>
</dt> <dd>

<span data-ttu-id="51511-117">Le transport de l’appareil est dans un état suspendu.</span><span class="sxs-lookup"><span data-stu-id="51511-117">The device s transport is in a paused state.</span></span>

</dd> <dt>

<span data-ttu-id="51511-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**D'**</span><span class="sxs-lookup"><span data-stu-id="51511-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Recording**</span></span>
</dt> <dd>

<span data-ttu-id="51511-119">Le transport de l’appareil est dans un état d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="51511-119">The device s transport is in a recording state.</span></span>

</dd> <dt>

<span data-ttu-id="51511-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span><span class="sxs-lookup"><span data-stu-id="51511-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span></span>
</dt> <dd>

<span data-ttu-id="51511-121">Le transport de l’appareil n’a pas d’URI défini pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="51511-121">The device s transport does not have an URI set for playback.</span></span>

</dd> <dt>

<span data-ttu-id="51511-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Famille**</span><span class="sxs-lookup"><span data-stu-id="51511-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="51511-123">État antérieur de l’appareil à l’état de transport actuel.</span><span class="sxs-lookup"><span data-stu-id="51511-123">The device s previous state to the current transport state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51511-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51511-124">Requirements</span></span>



| <span data-ttu-id="51511-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51511-125">Requirement</span></span> | <span data-ttu-id="51511-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="51511-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51511-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="51511-127">IDL</span></span><br/> | <dl> <span data-ttu-id="51511-128"><dt>Windows. Media. streaming. idl (référence Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="51511-128"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





