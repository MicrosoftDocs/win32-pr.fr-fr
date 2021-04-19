---
title: Énumération DeviceTypes
description: Décrit les types d’appareils DLNA pris en charge par l’API de diffusion multimédia en continu.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- API de diffusion multimédia par l’énumération DeviceTypes
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530939"
---
# <a name="devicetypes-enumeration"></a><span data-ttu-id="acfa0-104">Énumération DeviceTypes</span><span class="sxs-lookup"><span data-stu-id="acfa0-104">DeviceTypes enumeration</span></span>

<span data-ttu-id="acfa0-105">Décrit les types d’appareils DLNA pris en charge par l’API de diffusion multimédia en continu.</span><span class="sxs-lookup"><span data-stu-id="acfa0-105">Describes the DLNA device types that are supported by the Media Streaming API.</span></span>

## <a name="syntax"></a><span data-ttu-id="acfa0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acfa0-106">Syntax</span></span>


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a><span data-ttu-id="acfa0-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="acfa0-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="acfa0-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Connue**</span><span class="sxs-lookup"><span data-stu-id="acfa0-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="acfa0-109">Type d’appareil inconnu.</span><span class="sxs-lookup"><span data-stu-id="acfa0-109">Unknown device type.</span></span>

</dd> <dt>

<span data-ttu-id="acfa0-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="acfa0-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**</span></span>
</dt> <dd>

<span data-ttu-id="acfa0-111">Convertisseur de médias numériques DLNA (DMR).</span><span class="sxs-lookup"><span data-stu-id="acfa0-111">DLNA Digital Media Renderer (DMR).</span></span> <span data-ttu-id="acfa0-112">La valeur est équivalente au type d’appareil **urn : schemas-UPnP-org : Device : MediaRenderer : 1**.</span><span class="sxs-lookup"><span data-stu-id="acfa0-112">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaRenderer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="acfa0-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**</span><span class="sxs-lookup"><span data-stu-id="acfa0-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**</span></span>
</dt> <dd>

<span data-ttu-id="acfa0-114">Serveur de médias numériques DLNA (DMS).</span><span class="sxs-lookup"><span data-stu-id="acfa0-114">DLNA Digital Media Server (DMS).</span></span> <span data-ttu-id="acfa0-115">La valeur est équivalente au type d’appareil **urn : schemas-UPnP-org : Device : MediaServer : 1**.</span><span class="sxs-lookup"><span data-stu-id="acfa0-115">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaServer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="acfa0-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="acfa0-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**</span></span>
</dt> <dd>

<span data-ttu-id="acfa0-117">Lecteur multimédia numérique DLNA</span><span class="sxs-lookup"><span data-stu-id="acfa0-117">DLNA Digital Media Player</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="acfa0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acfa0-118">Requirements</span></span>



| <span data-ttu-id="acfa0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acfa0-119">Requirement</span></span> | <span data-ttu-id="acfa0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="acfa0-120">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acfa0-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="acfa0-121">IDL</span></span><br/> | <dl> <span data-ttu-id="acfa0-122"><dt>Windows. Media. streaming. idl (référence Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="acfa0-122"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





