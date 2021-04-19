---
description: Obtient le IMFDXGIDeviceManager à partir du récepteur de rendu vidéo Microsoft Media Foundation.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: 'IMFDXGIDeviceManagerSource :: GetManager, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524612"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a><span data-ttu-id="f084b-103">IMFDXGIDeviceManagerSource :: GetManager, méthode</span><span class="sxs-lookup"><span data-stu-id="f084b-103">IMFDXGIDeviceManagerSource::GetManager method</span></span>

<span data-ttu-id="f084b-104">Obtient le [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) à partir du récepteur de rendu vidéo Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f084b-104">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="f084b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f084b-105">Syntax</span></span>


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="f084b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f084b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f084b-107">*ppManager* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f084b-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f084b-108">Objet [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="f084b-108">The [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f084b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f084b-109">Return value</span></span>

<span data-ttu-id="f084b-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f084b-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f084b-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f084b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f084b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f084b-112">Requirements</span></span>



| <span data-ttu-id="f084b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f084b-113">Requirement</span></span> | <span data-ttu-id="f084b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f084b-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f084b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f084b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f084b-116">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f084b-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="f084b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f084b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f084b-118">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f084b-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="f084b-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="f084b-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f084b-120"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f084b-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f084b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f084b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f084b-122">**IMFDXGIDeviceManagerSource**</span><span class="sxs-lookup"><span data-stu-id="f084b-122">**IMFDXGIDeviceManagerSource**</span></span>](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




