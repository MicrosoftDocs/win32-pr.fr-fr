---
UID: NF:directml.DMLCreateDevice1
title: Fonction DMLCreateDevice1
description: Crée un appareil DirectML pour un appareil Direct3D 12 donné.
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f40c7e6aa82644b67303bc60f6a8b41fa08c6f8d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106531443"
---
# <a name="dmlcreatedevice1-function-directmlh"></a><span data-ttu-id="080b3-103">DMLCreateDevice1, fonction (directml. h)</span><span class="sxs-lookup"><span data-stu-id="080b3-103">DMLCreateDevice1 function (directml.h)</span></span>

<span data-ttu-id="080b3-104">Crée un appareil DirectML pour un appareil Direct3D 12 donné.</span><span class="sxs-lookup"><span data-stu-id="080b3-104">Creates a DirectML device for a given Direct3D 12 device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="080b3-105">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="080b3-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="080b3-106">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="080b3-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="080b3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="080b3-107">Syntax</span></span>

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="080b3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="080b3-108">Parameters</span></span>

`d3d12Device`

<span data-ttu-id="080b3-109">Type : <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span><span class="sxs-lookup"><span data-stu-id="080b3-109">Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span></span>

<span data-ttu-id="080b3-110">Pointeur vers un [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) représentant le périphérique Direct3D 12 sur lequel créer l’appareil DirectML.</span><span class="sxs-lookup"><span data-stu-id="080b3-110">A pointer to an [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) representing the Direct3D 12 device to create the DirectML device over.</span></span> <span data-ttu-id="080b3-111">DirectML prend en charge tous les niveaux de fonctionnalité D3D et les périphériques Direct3D 12 créés sur n’importe quelle carte, y compris WARP.</span><span class="sxs-lookup"><span data-stu-id="080b3-111">DirectML supports any D3D feature level, and Direct3D 12 devices created on any adapter, including WARP.</span></span> <span data-ttu-id="080b3-112">Toutefois, toutes les fonctionnalités de DirectML peuvent ne pas être disponibles en fonction des fonctionnalités de l’appareil Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="080b3-112">However, not all features in DirectML may be available depending on the capabilities of the Direct3D 12 device.</span></span> <span data-ttu-id="080b3-113">Pour plus d’informations, consultez [IDMLDevice :: CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) .</span><span class="sxs-lookup"><span data-stu-id="080b3-113">See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) for more info.</span></span>

<span data-ttu-id="080b3-114">Si l’appel à **DMLCreateDevice1** réussit, l’appareil DirectML gère une référence forte au périphérique Direct3D 12 fourni.</span><span class="sxs-lookup"><span data-stu-id="080b3-114">If the call to **DMLCreateDevice1** is successful, then the DirectML device maintains a strong reference to the supplied Direct3D 12 device.</span></span>

`flags`

<span data-ttu-id="080b3-115">Type : <b>DML_CREATE_DEVICE_FLAGS</b></span><span class="sxs-lookup"><span data-stu-id="080b3-115">Type: <b>DML_CREATE_DEVICE_FLAGS</b></span></span>

<span data-ttu-id="080b3-116">Valeur [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) spécifiant des options de création d’appareils supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="080b3-116">A [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) value specifying additional device creation options.</span></span>

`minimumFeatureLevel`

<span data-ttu-id="080b3-117">Type : <b>DML_FEATURE_LEVEL</b></span><span class="sxs-lookup"><span data-stu-id="080b3-117">Type: <b>DML_FEATURE_LEVEL</b></span></span>

<span data-ttu-id="080b3-118">Valeur [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) spécifiant la prise en charge de niveau de fonctionnalité minimale requise.</span><span class="sxs-lookup"><span data-stu-id="080b3-118">A [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) value specifying the minimum feature level support required.</span></span>

<span data-ttu-id="080b3-119">Ce paramètre peut être utile pour les appelants qui requièrent une version spécifique de DirectML, mais qui peuvent se trouver dans une version antérieure de DirectML.</span><span class="sxs-lookup"><span data-stu-id="080b3-119">This parameter can be useful for callers that require a specific version of DirectML, but who may find themselves calling into an older version of DirectML.</span></span> <span data-ttu-id="080b3-120">Cela peut se produire, par exemple, lorsque l’utilisateur exécute votre application sur une version antérieure de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="080b3-120">This can happen, for example, when the user runs your application on an older version of Windows 10.</span></span>

<span data-ttu-id="080b3-121">Les applications qui dépendent explicitement de la fonctionnalité introduite dans un niveau de fonctionnalité particulier peuvent la spécifier en tant que *minimumFeatureLevel*.</span><span class="sxs-lookup"><span data-stu-id="080b3-121">Applications that explicitly depend on functionality introduced in a particular feature level can specify it as a *minimumFeatureLevel*.</span></span> <span data-ttu-id="080b3-122">Cela permet de garantir que **DMLCreateDevice1** ne fonctionnera pas, sauf si l’implémentation sous-jacente est *au moins* aussi efficace que le niveau de fonctionnalité minimal requis.</span><span class="sxs-lookup"><span data-stu-id="080b3-122">This will guarantee that **DMLCreateDevice1** won't succeed unless the underlying implementation is *at least* as capable as this requested minimum feature level.</span></span>

<span data-ttu-id="080b3-123">Notez que comme ce paramètre spécifie un niveau de fonctionnalité *minimal* , l’appareil DirectML sous-jacent peut en fait prendre en charge un niveau de fonctionnalité supérieur à la valeur minimale demandée.</span><span class="sxs-lookup"><span data-stu-id="080b3-123">Note that as this parameter specifies a *minimum* feature level, the underlying DirectML device may in fact support a higher feature level than the requested minimum.</span></span> <span data-ttu-id="080b3-124">Une fois la création de l’appareil réussie, vous pouvez interroger tous les niveaux de fonctionnalité pris en charge par cet appareil à l’aide de [IDMLDevice :: CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="080b3-124">Once device creation succeeds, you can query all of the feature levels supported by this device using [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span></span>

`riid`

<span data-ttu-id="080b3-125">Type : <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="080b3-125">Type: <b>REFIID</b></span></span>

<span data-ttu-id="080b3-126">Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans l' <i>appareil</i>.</span><span class="sxs-lookup"><span data-stu-id="080b3-126">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>device</i>.</span></span> <span data-ttu-id="080b3-127">Il doit s’agir du GUID de [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span><span class="sxs-lookup"><span data-stu-id="080b3-127">This is expected to be the GUID of [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

`ppv`

<span data-ttu-id="080b3-128">Type : \_ com \_ Outptr \_ OPT \_ <b>void \* \*</b></span><span class="sxs-lookup"><span data-stu-id="080b3-128">Type: \_COM\_Outptr\_opt\_ <b>void\*\*</b></span></span>

<span data-ttu-id="080b3-129">Pointeur vers un bloc de mémoire qui reçoit un pointeur vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="080b3-129">A pointer to a memory block that receives a pointer to the device.</span></span> <span data-ttu-id="080b3-130">Il s’agit de l’adresse d’un pointeur vers un [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), représentant l’appareil DirectML créé.</span><span class="sxs-lookup"><span data-stu-id="080b3-130">This is the address of a pointer to an [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), representing  the DirectML device created.</span></span>


## <a name="return-value"></a><span data-ttu-id="080b3-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="080b3-131">Return value</span></span>

<span data-ttu-id="080b3-132">Type : [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="080b3-132">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="080b3-133">Si la fonction est réussie, elle retourne <b>S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="080b3-133">If the function succeeds, it returns <b>S_OK</b>.</span></span> <span data-ttu-id="080b3-134">Sinon, elle retourne un code d’erreur [HRESULT](/windows/desktop/winprog/windows-data-types) .</span><span class="sxs-lookup"><span data-stu-id="080b3-134">Otherwise, it returns an [HRESULT](/windows/desktop/winprog/windows-data-types) error code.</span></span>

<span data-ttu-id="080b3-135">Si cette version de DirectML ne prend pas en charge les *minimumFeatureLevel* demandés, cette fonction retourne **DXGI_ERROR_UNSUPPORTED**.</span><span class="sxs-lookup"><span data-stu-id="080b3-135">If this version of DirectML doesn't support the *minimumFeatureLevel* requested, then this function will return **DXGI_ERROR_UNSUPPORTED**.</span></span>

<span data-ttu-id="080b3-136">La fonctionnalité outils Graphics à la demande (DOM) doit être installée pour pouvoir utiliser les couches de débogage DirectML.</span><span class="sxs-lookup"><span data-stu-id="080b3-136">The Graphics Tools Feature on Demand (FOD) must be installed in order to use the DirectML debug layers.</span></span> <span data-ttu-id="080b3-137">Si l’indicateur de [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) est spécifié dans *Flags* et que les couches de débogage ne sont pas installées, **DMLCreateDevice1** retourne **DXGI_ERROR_SDK_COMPONENT_MISSING**.</span><span class="sxs-lookup"><span data-stu-id="080b3-137">If the [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) flag is specified in *flags* and the debug layers are not installed, then **DMLCreateDevice1** returns **DXGI_ERROR_SDK_COMPONENT_MISSING**.</span></span>

## <a name="remarks"></a><span data-ttu-id="080b3-138">Notes</span><span class="sxs-lookup"><span data-stu-id="080b3-138">Remarks</span></span>

<span data-ttu-id="080b3-139">Une version plus récente de cette fonction, [DMLCreateDevice1](), a été introduite dans DirectML version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="080b3-139">A newer version of this function, [DMLCreateDevice1](), was introduced in DirectML version 1.1.0.</span></span> <span data-ttu-id="080b3-140">**DMLCreateDevice1** est équivalent à l’appel de **DMLCreateDevice1** et à la fourniture d’un *minimumFeatureLevel* de [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span><span class="sxs-lookup"><span data-stu-id="080b3-140">**DMLCreateDevice1** is equivalent to calling **DMLCreateDevice1** and supplying a *minimumFeatureLevel* of [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span></span>

## <a name="availability"></a><span data-ttu-id="080b3-141">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="080b3-141">Availability</span></span>

<span data-ttu-id="080b3-142">Cette API a été introduite dans la version DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="080b3-142">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="requirements"></a><span data-ttu-id="080b3-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="080b3-143">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="080b3-144">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="080b3-144">**Target Platform**</span></span> | <span data-ttu-id="080b3-145">Windows</span><span class="sxs-lookup"><span data-stu-id="080b3-145">Windows</span></span> |
| <span data-ttu-id="080b3-146">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="080b3-146">**Header**</span></span> | <span data-ttu-id="080b3-147">directml. h</span><span class="sxs-lookup"><span data-stu-id="080b3-147">directml.h</span></span> |
| <span data-ttu-id="080b3-148">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="080b3-148">**Library**</span></span> | <span data-ttu-id="080b3-149">DirectML. lib</span><span class="sxs-lookup"><span data-stu-id="080b3-149">DirectML.lib</span></span> |
| <span data-ttu-id="080b3-150">**DLL**</span><span class="sxs-lookup"><span data-stu-id="080b3-150">**DLL**</span></span> | <span data-ttu-id="080b3-151">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="080b3-151">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="080b3-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="080b3-152">See also</span></span>

* [<span data-ttu-id="080b3-153">Énumération DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="080b3-153">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="080b3-154">Historique des versions DirectML</span><span class="sxs-lookup"><span data-stu-id="080b3-154">DirectML version history</span></span>](../dml-version-history.md)
* [<span data-ttu-id="080b3-155">Historique des niveaux de fonctionnalité DirectML</span><span class="sxs-lookup"><span data-stu-id="080b3-155">DirectML feature level history</span></span>](/windows/win32/direct3d12/dml-feature_level-history)    
* [<span data-ttu-id="080b3-156">Utilisation de la couche de débogage DirectML</span><span class="sxs-lookup"><span data-stu-id="080b3-156">Using the DirectML debug layer</span></span>](../dml-debug-layer.md)