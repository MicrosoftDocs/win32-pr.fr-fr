---
description: Fonction de rappel utilisée pour informer l’hôte des interfaces prises en charge.
MS-HAID: vspixengine.IVersionCallback\_VersionTableReady\_GUID\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IVersionCallback :: VersionTableReady, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 58D5E6B4-2CF8-4C13-9A62-93418D46CBCF
api_name:
- IVersionCallback.VersionTableReady
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4f31f8b4619d74f6f491f6be8faf7ddd457ee82c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109295"
---
# <a name="span-idvspixengineiversioncallback_versiontableready_guid_arr_uintspaniversioncallbackversiontableready-method"></a><span data-ttu-id="36b92-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback :: VersionTableReady, méthode</span><span class="sxs-lookup"><span data-stu-id="36b92-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback::VersionTableReady method</span></span>

<span data-ttu-id="36b92-104">Fonction de rappel utilisée pour informer l’hôte des interfaces prises en charge.</span><span class="sxs-lookup"><span data-stu-id="36b92-104">A callback function used to notify the host of which interfaces are supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="36b92-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36b92-105">Syntax</span></span>


```C++
HRESULT VersionTableReady(
   GUID [] count1_interfaceIds,
   UINT    count
);
```

## <a name="parameters"></a><span data-ttu-id="36b92-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36b92-106">Parameters</span></span>

<span data-ttu-id="36b92-107">*count1 \_ interfaceIds* </span><span class="sxs-lookup"><span data-stu-id="36b92-107">*count1\_interfaceIds* </span></span>  
<span data-ttu-id="36b92-108">Tableau contenant les GUID des ID d’interface pris en charge.</span><span class="sxs-lookup"><span data-stu-id="36b92-108">An array containing the GUIDs of supported interface IDs.</span></span>

<span data-ttu-id="36b92-109">*saut* </span><span class="sxs-lookup"><span data-stu-id="36b92-109">*count* </span></span>  
<span data-ttu-id="36b92-110">Nombre de GUID transmis dans count1 \_ interfaceIds.</span><span class="sxs-lookup"><span data-stu-id="36b92-110">The number of GUIDs passed in count1\_interfaceIds.</span></span>

## <a name="return-value"></a><span data-ttu-id="36b92-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36b92-111">Return value</span></span>

<span data-ttu-id="36b92-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="36b92-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="36b92-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="36b92-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="36b92-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36b92-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="36b92-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="36b92-115">Header</span></span></p></td><td><span data-ttu-id="36b92-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="36b92-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="36b92-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36b92-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="36b92-118">**IVersionCallback**</span><span class="sxs-lookup"><span data-stu-id="36b92-118">**IVersionCallback**</span></span>](/windows/desktop/direct3dtools/iversioncallback)

 

 
