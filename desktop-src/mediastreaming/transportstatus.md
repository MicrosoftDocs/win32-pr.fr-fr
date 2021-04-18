---
title: Énumération TransportStatus
description: Définit l’état de transport disponible tel que défini par les instructions UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- API de diffusion multimédia par l’énumération TransportStatus
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526666"
---
# <a name="transportstatus-enumeration"></a><span data-ttu-id="10ce8-104">Énumération TransportStatus</span><span class="sxs-lookup"><span data-stu-id="10ce8-104">TransportStatus enumeration</span></span>

<span data-ttu-id="10ce8-105">Définit l’état de transport disponible tel que défini par les instructions UPnP.</span><span class="sxs-lookup"><span data-stu-id="10ce8-105">Defines the available transport status as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ce8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10ce8-106">Syntax</span></span>


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a><span data-ttu-id="10ce8-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="10ce8-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="10ce8-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Connue**</span><span class="sxs-lookup"><span data-stu-id="10ce8-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="10ce8-109">État du périphérique erroné.</span><span class="sxs-lookup"><span data-stu-id="10ce8-109">Erroneous device status.</span></span>

</dd> <dt>

<span data-ttu-id="10ce8-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Bien**</span><span class="sxs-lookup"><span data-stu-id="10ce8-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok**</span></span>
</dt> <dd>

<span data-ttu-id="10ce8-111">L’appareil est dans un état correct.</span><span class="sxs-lookup"><span data-stu-id="10ce8-111">The device is in a good status.</span></span>

</dd> <dt>

<span data-ttu-id="10ce8-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span><span class="sxs-lookup"><span data-stu-id="10ce8-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span></span>
</dt> <dd>

<span data-ttu-id="10ce8-113">Une erreur s’est produite sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="10ce8-113">An error occurred on the device.</span></span>

</dd> <dt>

<span data-ttu-id="10ce8-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Famille**</span><span class="sxs-lookup"><span data-stu-id="10ce8-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="10ce8-115">État antérieur de l’appareil à l’état de transport actuel.</span><span class="sxs-lookup"><span data-stu-id="10ce8-115">The device s previous status to the current transport status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10ce8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10ce8-116">Requirements</span></span>



| <span data-ttu-id="10ce8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10ce8-117">Requirement</span></span> | <span data-ttu-id="10ce8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="10ce8-118">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10ce8-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="10ce8-119">IDL</span></span><br/> | <dl> <span data-ttu-id="10ce8-120"><dt>Windows. Media. streaming. idl (référence Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="10ce8-120"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





