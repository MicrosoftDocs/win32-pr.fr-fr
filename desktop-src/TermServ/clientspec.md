---
title: Énumération ClientSpec
description: Utilisé avec la propriété ClientProtocolSpec pour spécifier le Protocole Bureau à distance utilisé entre le client et le serveur.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’énumération ClientSpec
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513765"
---
# <a name="clientspec-enumeration"></a><span data-ttu-id="b1108-104">Énumération ClientSpec</span><span class="sxs-lookup"><span data-stu-id="b1108-104">ClientSpec enumeration</span></span>

<span data-ttu-id="b1108-105">Utilisé avec la propriété [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) pour spécifier le Protocole Bureau à distance utilisé entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="b1108-105">Used with the [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) property to specify the remote desktop protocol used between the client and the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1108-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1108-106">Syntax</span></span>


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a><span data-ttu-id="b1108-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="b1108-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b1108-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**</span><span class="sxs-lookup"><span data-stu-id="b1108-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**</span></span>
</dt> <dd>

<span data-ttu-id="b1108-109">Le protocole est un protocole Windows 8 Bureau à distance complet.</span><span class="sxs-lookup"><span data-stu-id="b1108-109">The protocol is full Windows 8 Remote Desktop protocol.</span></span>

</dd> <dt>

<span data-ttu-id="b1108-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span><span class="sxs-lookup"><span data-stu-id="b1108-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span></span>
</dt> <dd>

<span data-ttu-id="b1108-111">Le protocole est limité à l’utilisation du codec RemoteFX Windows 7 avec SP1 et d’un cache plus petit.</span><span class="sxs-lookup"><span data-stu-id="b1108-111">The protocol is limited to using the Windows 7 with SP1 RemoteFX codec and a smaller cache.</span></span> <span data-ttu-id="b1108-112">Tous les autres codecs sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="b1108-112">All other codecs are disabled.</span></span> <span data-ttu-id="b1108-113">Ce protocole présente l’encombrement mémoire le plus faible.</span><span class="sxs-lookup"><span data-stu-id="b1108-113">This protocol has the smallest memory footprint.</span></span>

</dd> <dt>

<span data-ttu-id="b1108-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span><span class="sxs-lookup"><span data-stu-id="b1108-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span></span>
</dt> <dd>

<span data-ttu-id="b1108-115">Le protocole est identique à **FullMode**, à ceci près qu’il utilise un cache plus petit.</span><span class="sxs-lookup"><span data-stu-id="b1108-115">The protocol is the same as **FullMode**, except it uses a smaller cache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1108-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1108-116">Requirements</span></span>



| <span data-ttu-id="b1108-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1108-117">Requirement</span></span> | <span data-ttu-id="b1108-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1108-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1108-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1108-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b1108-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b1108-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="b1108-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1108-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b1108-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1108-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="b1108-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b1108-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1108-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1108-124"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1108-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1108-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1108-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span><span class="sxs-lookup"><span data-stu-id="b1108-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span></span>](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





