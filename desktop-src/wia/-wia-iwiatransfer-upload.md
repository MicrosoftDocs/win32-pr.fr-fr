---
description: Lance un chargement de données d’un élément unique à partir de l’appelant.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'IWiaTransfer :: upload, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201490"
---
# <a name="iwiatransferupload-method"></a><span data-ttu-id="fa266-103">IWiaTransfer :: upload, méthode</span><span class="sxs-lookup"><span data-stu-id="fa266-103">IWiaTransfer::Upload method</span></span>

<span data-ttu-id="fa266-104">Lance un chargement de données d’un élément unique à partir de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="fa266-104">Initiates a data upload of a single item from the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa266-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa266-105">Syntax</span></span>


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="fa266-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa266-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa266-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa266-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa266-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="fa266-108">Type: **LONG**</span></span>

<span data-ttu-id="fa266-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="fa266-109">Currently unused.</span></span> <span data-ttu-id="fa266-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="fa266-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fa266-111">*pSource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa266-111">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa266-112">Type : \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="fa266-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="fa266-113">Spécifie un pointeur vers les données [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="fa266-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) data.</span></span>

</dd> <dt>

<span data-ttu-id="fa266-114">_pIWiaTransferCallback \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa266-114">_pIWiaTransferCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa266-115">Tapez : \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="fa266-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="fa266-116">Spécifie un pointeur vers l’interface [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="fa266-116">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa266-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa266-117">Return value</span></span>

<span data-ttu-id="fa266-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fa266-118">Type: **HRESULT**</span></span>

<span data-ttu-id="fa266-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fa266-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa266-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa266-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa266-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa266-121">Requirements</span></span>



| <span data-ttu-id="fa266-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa266-122">Requirement</span></span> | <span data-ttu-id="fa266-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa266-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa266-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa266-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fa266-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa266-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fa266-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa266-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fa266-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa266-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fa266-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa266-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa266-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa266-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="fa266-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="fa266-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa266-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa266-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="fa266-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fa266-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa266-133"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa266-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
