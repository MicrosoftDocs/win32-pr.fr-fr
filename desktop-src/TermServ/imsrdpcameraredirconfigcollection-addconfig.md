---
title: IMsRdpCameraRedirConfigCollection AddConfig, méthode
description: Ajoute un objet IMsRdpCameraRedirConfig à la collection (la caméra correspondante n’a pas besoin d’être connectée).
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddConfig
- Méthode AddConfig Services Bureau à distance, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, méthode AddConfig
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520303"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a><span data-ttu-id="dff07-106">IMsRdpCameraRedirConfigCollection :: AddConfig, méthode</span><span class="sxs-lookup"><span data-stu-id="dff07-106">IMsRdpCameraRedirConfigCollection::AddConfig method</span></span>

<span data-ttu-id="dff07-107">Ajoute un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) à la collection (la caméra correspondante n’a pas besoin d’être connectée).</span><span class="sxs-lookup"><span data-stu-id="dff07-107">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>

## <a name="syntax"></a><span data-ttu-id="dff07-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dff07-108">Syntax</span></span>

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a><span data-ttu-id="dff07-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dff07-109">Parameters</span></span>

<span data-ttu-id="dff07-110">*symbolicLink* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dff07-110">*symbolicLink* \[in\]</span></span>

<span data-ttu-id="dff07-111">Lien symbolique pour le nouvel objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="dff07-111">The symbolic link for the new [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object.</span></span>

<span data-ttu-id="dff07-112">*fRedirected* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dff07-112">*fRedirected* \[in\]</span></span>

<span data-ttu-id="dff07-113">Spécifie si la nouvelle caméra est redirigée par défaut.</span><span class="sxs-lookup"><span data-stu-id="dff07-113">Specifies whether or not the new camera gets redirected by default.</span></span>

## <a name="return-value"></a><span data-ttu-id="dff07-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dff07-114">Return value</span></span>

<span data-ttu-id="dff07-115">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="dff07-115">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="dff07-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dff07-116">Requirements</span></span>

| <span data-ttu-id="dff07-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dff07-117">Requirement</span></span> | <span data-ttu-id="dff07-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dff07-118">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="dff07-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dff07-119">Minimum supported client</span></span>| <span data-ttu-id="dff07-120">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="dff07-120">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="dff07-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="dff07-121">Type library</span></span>            | <span data-ttu-id="dff07-122">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="dff07-122">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="dff07-123">DLL</span><span class="sxs-lookup"><span data-stu-id="dff07-123">DLL</span></span>                  | <span data-ttu-id="dff07-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="dff07-124">MsTscAx.dll</span></span>     |
| <span data-ttu-id="dff07-125">IID</span><span class="sxs-lookup"><span data-stu-id="dff07-125">IID</span></span>                      | <span data-ttu-id="dff07-126">IID \_ IMsRdpCameraRedirConfigCollection est défini en tant que AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="dff07-126">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="dff07-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dff07-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff07-128">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="dff07-128">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>