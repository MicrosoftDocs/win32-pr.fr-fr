---
description: Lance un téléchargement de données vers l’appelant.
ms.assetid: e639fabb-2c13-4009-affa-1c2b06c0d4c8
title: IWiaTransfer ::D méthode lécharger (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Download
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 2863915b850588d4db018693d9081ed2907d644a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526457"
---
# <a name="iwiatransferdownload-method"></a><span data-ttu-id="b6bb9-103">IWiaTransfer ::D méthode lécharger</span><span class="sxs-lookup"><span data-stu-id="b6bb9-103">IWiaTransfer::Download method</span></span>

<span data-ttu-id="b6bb9-104">Lance un téléchargement de données vers l’appelant.</span><span class="sxs-lookup"><span data-stu-id="b6bb9-104">Initiates a data download to the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6bb9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6bb9-105">Syntax</span></span>


```C++
HRESULT Download(
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="b6bb9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6bb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6bb9-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6bb9-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6bb9-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="b6bb9-108">Type: **LONG**</span></span>

<span data-ttu-id="b6bb9-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="b6bb9-109">Currently unused.</span></span> <span data-ttu-id="b6bb9-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="b6bb9-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b6bb9-111">*pIWiaTransferCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6bb9-111">*pIWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6bb9-112">Tapez : \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="b6bb9-112">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="b6bb9-113">Spécifie un pointeur vers l’interface [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="b6bb9-113">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6bb9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6bb9-114">Return value</span></span>

<span data-ttu-id="b6bb9-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b6bb9-115">Type: **HRESULT**</span></span>

<span data-ttu-id="b6bb9-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b6bb9-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b6bb9-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b6bb9-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6bb9-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b6bb9-118">Remarks</span></span>

<span data-ttu-id="b6bb9-119">Si un dossier est téléchargé, tous les éléments enfants de ce dossier sont également transférés.</span><span class="sxs-lookup"><span data-stu-id="b6bb9-119">If a folder is downloaded, then all the child items of that folder are also transferred.</span></span> <span data-ttu-id="b6bb9-120">Chaque élément est transféré dans un flux distinct.</span><span class="sxs-lookup"><span data-stu-id="b6bb9-120">Each item is transferred in a separate stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6bb9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6bb9-121">Requirements</span></span>



| <span data-ttu-id="b6bb9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6bb9-122">Requirement</span></span> | <span data-ttu-id="b6bb9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6bb9-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6bb9-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6bb9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b6bb9-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6bb9-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b6bb9-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6bb9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b6bb9-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6bb9-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b6bb9-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6bb9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6bb9-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6bb9-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="b6bb9-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="b6bb9-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6bb9-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6bb9-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="b6bb9-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6bb9-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6bb9-133"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6bb9-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




