---
description: Crée un énumérateur pour les formats de transfert pris en charge par l’appareil WIA (Windows Image Acquisition) 2,0.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'IWiaTransfer :: EnumWIA_FORMAT_INFO, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527613"
---
# <a name="iwiatransferenumwia_format_info-method"></a><span data-ttu-id="b7983-103">IWiaTransfer :: EnumWIA \_ , \_ méthode des informations de format</span><span class="sxs-lookup"><span data-stu-id="b7983-103">IWiaTransfer::EnumWIA\_FORMAT\_INFO method</span></span>

<span data-ttu-id="b7983-104">Crée un énumérateur pour les formats de transfert pris en charge par l’appareil WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="b7983-104">Creates an enumerator for the transfer formats that the Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7983-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7983-105">Syntax</span></span>


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="b7983-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7983-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7983-107">*ppIEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b7983-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7983-108">Type : **[ **\_ \_ informations sur le format IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="b7983-108">Type: **[**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span></span>

<span data-ttu-id="b7983-109">Adresse du pointeur vers l’interface d' [**\_ \_ informations de format IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) pour l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="b7983-109">The address of the pointer to the [**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) interface for the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7983-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7983-110">Return value</span></span>

<span data-ttu-id="b7983-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b7983-111">Type: **HRESULT**</span></span>

<span data-ttu-id="b7983-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b7983-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7983-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7983-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7983-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b7983-114">Remarks</span></span>

<span data-ttu-id="b7983-115">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur d’interface reçu via le paramètre *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="b7983-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointer received through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7983-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7983-116">Requirements</span></span>



| <span data-ttu-id="b7983-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7983-117">Requirement</span></span> | <span data-ttu-id="b7983-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7983-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7983-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7983-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b7983-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7983-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b7983-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7983-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b7983-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7983-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b7983-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7983-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7983-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7983-124"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="b7983-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="b7983-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7983-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7983-126"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="b7983-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b7983-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7983-128"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7983-128"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
