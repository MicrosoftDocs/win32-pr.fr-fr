---
title: 'DXCoreAdapterProperty '
description: Définit des constantes qui spécifient les propriétés de l’adaptateur DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 645f0a890aac9a50cdf2987c0736a85142a91aff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511083"
---
# <a name="dxcoreadapterproperty-enum"></a><span data-ttu-id="ff660-103">Énumération DXCoreAdapterProperty</span><span class="sxs-lookup"><span data-stu-id="ff660-103">DXCoreAdapterProperty enum</span></span>

<span data-ttu-id="ff660-104">Définit des constantes qui spécifient les propriétés de l’adaptateur DXCore.</span><span class="sxs-lookup"><span data-stu-id="ff660-104">Defines constants that specify DXCore adapter properties.</span></span> <span data-ttu-id="ff660-105">Transmettez l’une de ces constantes à la méthode [IDXCoreAdapter :: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) pour récupérer la taille de mémoire tampon nécessaire pour recevoir la valeur de la propriété correspondante ; Transmettez ensuite la même constante à la méthode [IDXCoreAdapter :: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) pour récupérer la valeur de la propriété dans une mémoire tampon que vous allouez.</span><span class="sxs-lookup"><span data-stu-id="ff660-105">Pass one of these constants to the [IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) method to retrieve the buffer size necessary to receive the value of the corresponding property; then pass the same constant to the [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) method to retrieve the property's value in a buffer that you allocate.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff660-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff660-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterProperty : uint32_t
{
  InstanceLuid = 0,
  DriverVersion = 1,
  DriverDescription = 2,
  HardwareID = 3,
  KmdModelVersion = 4,
  ComputePreemptionGranularity = 5,
  GraphicsPreemptionGranularity = 6,
  DedicatedAdapterMemory = 7,
  DedicatedSystemMemory = 8,
  SharedSystemMemory = 9,
  AcgCompatible = 10,
  IsHardware = 11,
  IsIntegrated = 12,
  IsDetachable = 13
};
```

## <a name="constants"></a><span data-ttu-id="ff660-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="ff660-107">Constants</span></span>

### <a name="instanceluid"></a><span data-ttu-id="ff660-108">InstanceLuid</span><span class="sxs-lookup"><span data-stu-id="ff660-108">InstanceLuid</span></span>

<span data-ttu-id="ff660-109">Spécifie la propriété de l’adaptateur <em>InstanceLuid</em> , qui contient un identificateur unique local représentant l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="ff660-109">Specifies the <em>InstanceLuid</em> adapter property, which contains a locally unique identifier representing the adapter.</span></span> <span data-ttu-id="ff660-110">Cette valeur reste constante pendant la durée de vie de cet adaptateur.</span><span class="sxs-lookup"><span data-stu-id="ff660-110">This value remains constant for the lifetime of this adapter.</span></span> <span data-ttu-id="ff660-111">Le LUID d’un adaptateur change au redémarrage, à la mise à niveau du pilote ou à la désactivation/activation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ff660-111">The LUID of an adapter changes on reboot, driver upgrade, or device disablement/enablement.</span></span>

<span data-ttu-id="ff660-112">La propriété de l’adaptateur <em>InstanceLuid</em> a le type <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span><span class="sxs-lookup"><span data-stu-id="ff660-112">The <em>InstanceLuid</em> adapter property has type <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span></span>

### <a name="driverversion"></a><span data-ttu-id="ff660-113">DriverVersion</span><span class="sxs-lookup"><span data-stu-id="ff660-113">DriverVersion</span></span>

<span data-ttu-id="ff660-114">Spécifie la propriété de l’adaptateur <em>DriverVersion</em> , qui contient la version du pilote, représentée dans <b>Word</b>s comme un <b>LARGE_INTEGER</b>.</span><span class="sxs-lookup"><span data-stu-id="ff660-114">Specifies the <em>DriverVersion</em> adapter property, which contains the driver version, represented in <b>WORD</b>s as a <b>LARGE_INTEGER</b>.</span></span>

<span data-ttu-id="ff660-115">La propriété de l’adaptateur <em>DriverVersion</em> a le type <b>uint64_t</b>, qui représente une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="ff660-115">The <em>DriverVersion</em> adapter property has type <b>uint64_t</b>, representing a Boolean value.</span></span>

### <a name="driverdescription"></a><span data-ttu-id="ff660-116">DriverDescription</span><span class="sxs-lookup"><span data-stu-id="ff660-116">DriverDescription</span></span>

<span data-ttu-id="ff660-117">Spécifie la propriété de l’adaptateur <em>DriverDescription</em> , qui contient un tableau de <b>caractères</b>se terminant par un caractère null, qui décrit le pilote, comme spécifié par le pilote, dans l’encodage <a href="/windows/win32/intl/unicode">UTF-8</a> .</span><span class="sxs-lookup"><span data-stu-id="ff660-117">Specifies the <em>DriverDescription</em> adapter property, which contains a NULL-terminated array of <b>CHAR</b>s describing the driver, as specified by the driver, in <a href="/windows/win32/intl/unicode">UTF-8</a> encoding.</span></span>

<span data-ttu-id="ff660-118">La propriété de l’adaptateur <em>DriverDescription</em> est de type <b>char \*</b>.</span><span class="sxs-lookup"><span data-stu-id="ff660-118">The <em>DriverDescription</em> adapter property has type <b>char\*</b>.</span></span>

### <a name="hardwareid"></a><span data-ttu-id="ff660-119">HardwareID</span><span class="sxs-lookup"><span data-stu-id="ff660-119">HardwareID</span></span>

<span data-ttu-id="ff660-120">Spécifie la propriété de l’adaptateur <em>HardwareID</em> , qui représente les parties de l’ID de matériel PNP.</span><span class="sxs-lookup"><span data-stu-id="ff660-120">Specifies the <em>HardwareID</em> adapter property, which represents the PnP hardware ID parts.</span></span>

<span data-ttu-id="ff660-121">La propriété de l’adaptateur <em>HardwareID</em> a le type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.</span><span class="sxs-lookup"><span data-stu-id="ff660-121">The <em>HardwareID</em> adapter property has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.</span></span>

### <a name="kmdmodelversion"></a><span data-ttu-id="ff660-122">KmdModelVersion</span><span class="sxs-lookup"><span data-stu-id="ff660-122">KmdModelVersion</span></span>

<span data-ttu-id="ff660-123">Spécifie la propriété de l’adaptateur <em>KmdModelVersion</em> , qui représente le modèle de pilote.</span><span class="sxs-lookup"><span data-stu-id="ff660-123">Specifies the <em>KmdModelVersion</em> adapter property, which represents the driver model.</span></span>

<span data-ttu-id="ff660-124">La propriété de l’adaptateur <em>KmdModelVersion</em> a le type <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span><span class="sxs-lookup"><span data-stu-id="ff660-124">The <em>KmdModelVersion</em> adapter property has type <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span></span>

### <a name="computepreemptiongranularity"></a><span data-ttu-id="ff660-125">ComputePreemptionGranularity</span><span class="sxs-lookup"><span data-stu-id="ff660-125">ComputePreemptionGranularity</span></span>

<span data-ttu-id="ff660-126">Spécifie la propriété de l’adaptateur <em>ComputePreemptionGranularity</em> , qui représente la granularité de préemption du calcul.</span><span class="sxs-lookup"><span data-stu-id="ff660-126">Specifies the <em>ComputePreemptionGranularity</em> adapter property, which represents the compute preemption granularity.</span></span>

<span data-ttu-id="ff660-127">La propriété de l’adaptateur <em>ComputePreemptionGranularity</em> a le type <b>uint16_t</b>, représentant une valeur de <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> .</span><span class="sxs-lookup"><span data-stu-id="ff660-127">The <em>ComputePreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="graphicspreemptiongranularity"></a><span data-ttu-id="ff660-128">GraphicsPreemptionGranularity</span><span class="sxs-lookup"><span data-stu-id="ff660-128">GraphicsPreemptionGranularity</span></span>

<span data-ttu-id="ff660-129">Spécifie la propriété de l’adaptateur <em>GraphicsPreemptionGranularity</em> , qui représente la granularité de préemption des graphiques.</span><span class="sxs-lookup"><span data-stu-id="ff660-129">Specifies the <em>GraphicsPreemptionGranularity</em> adapter property, which represents the graphics preemption granularity.</span></span>

<span data-ttu-id="ff660-130">La propriété de l’adaptateur <em>GraphicsPreemptionGranularity</em> a le type <b>uint16_t</b>, représentant une valeur de <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> .</span><span class="sxs-lookup"><span data-stu-id="ff660-130">The <em>GraphicsPreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="dedicatedadaptermemory"></a><span data-ttu-id="ff660-131">DedicatedAdapterMemory</span><span class="sxs-lookup"><span data-stu-id="ff660-131">DedicatedAdapterMemory</span></span>

<span data-ttu-id="ff660-132">Spécifie la propriété de l’adaptateur <em>DedicatedAdapterMemory</em> , qui représente le nombre d’octets de mémoire d’adaptateur dédiée qui ne sont pas partagés avec l’UC.</span><span class="sxs-lookup"><span data-stu-id="ff660-132">Specifies the <em>DedicatedAdapterMemory</em> adapter property, which represents the number of bytes of dedicated adapter memory that are not shared with the CPU.</span></span>

<span data-ttu-id="ff660-133">La propriété de l’adaptateur <em>DedicatedVideoMemory</em> a le type <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="ff660-133">The <em>DedicatedVideoMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="dedicatedsystemmemory"></a><span data-ttu-id="ff660-134">DedicatedSystemMemory</span><span class="sxs-lookup"><span data-stu-id="ff660-134">DedicatedSystemMemory</span></span>

<span data-ttu-id="ff660-135">Spécifie la propriété de l’adaptateur <em>DedicatedSystemMemory</em> , qui représente le nombre d’octets de mémoire système dédiée qui ne sont pas partagés avec l’UC.</span><span class="sxs-lookup"><span data-stu-id="ff660-135">Specifies the <em>DedicatedSystemMemory</em> adapter property, which represents the number of bytes of dedicated system memory that are not shared with the CPU.</span></span> <span data-ttu-id="ff660-136">Cette mémoire est allouée à partir de la mémoire système disponible au moment du démarrage.</span><span class="sxs-lookup"><span data-stu-id="ff660-136">This memory is allocated from available system memory at boot time.</span></span>

<span data-ttu-id="ff660-137">La propriété de l’adaptateur <em>DedicatedSystemMemory</em> a le type <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="ff660-137">The <em>DedicatedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="sharedsystemmemory"></a><span data-ttu-id="ff660-138">SharedSystemMemory</span><span class="sxs-lookup"><span data-stu-id="ff660-138">SharedSystemMemory</span></span>

<span data-ttu-id="ff660-139">Spécifie la propriété de l’adaptateur <em>SharedSystemMemory</em> , qui représente le nombre d’octets de mémoire système partagée.</span><span class="sxs-lookup"><span data-stu-id="ff660-139">Specifies the <em>SharedSystemMemory</em> adapter property, which represents the number of bytes of shared system memory.</span></span> <span data-ttu-id="ff660-140">Il s’agit de la valeur maximale de la mémoire système qui peut être consommée par l’adaptateur lors de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ff660-140">This is the maximum value of system memory that may be consumed by the adapter during operation.</span></span> <span data-ttu-id="ff660-141">Toute mémoire accessoire consommée par le pilote lorsqu’il gère et utilise la mémoire vidéo est supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ff660-141">Any incidental memory consumed by the driver as it manages and uses video memory is additional.</span></span>

<span data-ttu-id="ff660-142">La propriété de l’adaptateur <em>SharedSystemMemory</em> a le type <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="ff660-142">The <em>SharedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="acgcompatible"></a><span data-ttu-id="ff660-143">AcgCompatible</span><span class="sxs-lookup"><span data-stu-id="ff660-143">AcgCompatible</span></span>

<span data-ttu-id="ff660-144">Spécifie la propriété de l’adaptateur <em>AcgCompatible</em> , qui indique si l’adaptateur est compatible avec les processus qui appliquent la protection de code arbitraire.</span><span class="sxs-lookup"><span data-stu-id="ff660-144">Specifies the <em>AcgCompatible</em> adapter property, which indicates whether the adapter is compatible with processes that enforce Arbitrary Code Guard.</span></span>

<span data-ttu-id="ff660-145">La propriété de l’adaptateur <em>AcgCompatible</em> est de type <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="ff660-145">The <em>AcgCompatible</em> adapter property has type <b>bool</b>.</span></span>

### <a name="ishardware"></a><span data-ttu-id="ff660-146">IsHardware</span><span class="sxs-lookup"><span data-stu-id="ff660-146">IsHardware</span></span>

<span data-ttu-id="ff660-147">Spécifie la propriété de l’adaptateur <em>IsHardware</em> , qui détermine s’il s’agit ou non d’un adaptateur matériel.</span><span class="sxs-lookup"><span data-stu-id="ff660-147">Specifies the <em>IsHardware</em> adapter property, which determines whether or not this is a hardware adapter.</span></span> <span data-ttu-id="ff660-148">Un adaptateur qui n’est pas une carte matérielle est un adaptateur logiciel.</span><span class="sxs-lookup"><span data-stu-id="ff660-148">An adapter that's not a hardware adapter is a software adapter.</span></span>

<span data-ttu-id="ff660-149">La propriété de l’adaptateur <em>IsHardware</em> est de type <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="ff660-149">The <em>IsHardware</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isintegrated"></a><span data-ttu-id="ff660-150">IsIntegrated</span><span class="sxs-lookup"><span data-stu-id="ff660-150">IsIntegrated</span></span>

<span data-ttu-id="ff660-151">Spécifie la propriété de l’adaptateur <em>IsIntegrated</em> , qui détermine si l’adaptateur est signalé comme étant un processeur graphique intégré (iGPU).</span><span class="sxs-lookup"><span data-stu-id="ff660-151">Specifies the <em>IsIntegrated</em> adapter property, which determines whether the adapter is reported to be an integrated graphics processor (iGPU).</span></span>

<span data-ttu-id="ff660-152">La propriété de l’adaptateur <em>IsIntegrated</em> est de type <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="ff660-152">The <em>IsIntegrated</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isdetachable"></a><span data-ttu-id="ff660-153">IsDetachable</span><span class="sxs-lookup"><span data-stu-id="ff660-153">IsDetachable</span></span>

<span data-ttu-id="ff660-154">Spécifie la propriété de l’adaptateur <em>IsDetachable</em> , qui détermine si l’adaptateur a été signalé comme pouvant être détaché ou amovible.</span><span class="sxs-lookup"><span data-stu-id="ff660-154">Specifies the <em>IsDetachable</em> adapter property, which determines whether the adapter has been reported to be detachable, or removable.</span></span>

<span data-ttu-id="ff660-155">La propriété de l’adaptateur <em>IsDetachable</em> est de type <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="ff660-155">The <em>IsDetachable</em> adapter property has type <b>bool</b>.</span></span>

<span data-ttu-id="ff660-156"><b>Remarque</b>:</span><span class="sxs-lookup"><span data-stu-id="ff660-156"><b>Note</b>.</span></span> <span data-ttu-id="ff660-157">Même si <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter :: GetProperty</a> indique `false` pour cette propriété, l’adaptateur a toujours la possibilité d’être signalé comme étant supprimé, comme dans le cas d’un dysfonctionnement ou d’une mise à jour de pilote.</span><span class="sxs-lookup"><span data-stu-id="ff660-157">Even if <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> indicates `false` for this property, the adapter still has the ability to be reported as removed, such as in the case of malfunction, or driver update.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff660-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff660-158">See also</span></span>

<span data-ttu-id="ff660-159">[IDXCoreAdapter :: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter :: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="ff660-159">[IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>