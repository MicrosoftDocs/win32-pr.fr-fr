---
title: Énumération ControlReconnectStatus
description: Spécifie le résultat de la méthode de reconnexion IMsRdpClient8.
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’énumération ControlReconnectStatus
topic_type:
- apiref
api_name:
- ControlReconnectStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5638cbdda268dd453881ee1d88085728479aada6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510942"
---
# <a name="controlreconnectstatus-enumeration"></a><span data-ttu-id="cfffd-104">Énumération ControlReconnectStatus</span><span class="sxs-lookup"><span data-stu-id="cfffd-104">ControlReconnectStatus enumeration</span></span>

<span data-ttu-id="cfffd-105">Spécifie le résultat de la méthode [**IMsRdpClient8 :: reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="cfffd-105">Specifies the result of the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfffd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfffd-106">Syntax</span></span>


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a><span data-ttu-id="cfffd-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="cfffd-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cfffd-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span><span class="sxs-lookup"><span data-stu-id="cfffd-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span></span>
</dt> <dd>

<span data-ttu-id="cfffd-109">L’opération de reconnexion a été démarrée.</span><span class="sxs-lookup"><span data-stu-id="cfffd-109">The reconnect operation was started.</span></span>

</dd> <dt>

<span data-ttu-id="cfffd-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span><span class="sxs-lookup"><span data-stu-id="cfffd-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span></span>
</dt> <dd>

<span data-ttu-id="cfffd-111">Impossible de démarrer l’opération de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="cfffd-111">The reconnect operation could not be started.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cfffd-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfffd-112">Requirements</span></span>



| <span data-ttu-id="cfffd-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfffd-113">Requirement</span></span> | <span data-ttu-id="cfffd-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfffd-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfffd-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfffd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cfffd-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cfffd-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="cfffd-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfffd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cfffd-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cfffd-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="cfffd-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cfffd-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="cfffd-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfffd-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfffd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfffd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfffd-122">**IMsRdpClient8 :: reconnecter**</span><span class="sxs-lookup"><span data-stu-id="cfffd-122">**IMsRdpClient8::Reconnect**</span></span>](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





