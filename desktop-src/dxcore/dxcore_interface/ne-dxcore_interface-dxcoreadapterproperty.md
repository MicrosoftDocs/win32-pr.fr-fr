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
# <a name="dxcoreadapterproperty-enum"></a>Énumération DXCoreAdapterProperty

Définit des constantes qui spécifient les propriétés de l’adaptateur DXCore. Transmettez l’une de ces constantes à la méthode [IDXCoreAdapter :: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) pour récupérer la taille de mémoire tampon nécessaire pour recevoir la valeur de la propriété correspondante ; Transmettez ensuite la même constante à la méthode [IDXCoreAdapter :: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) pour récupérer la valeur de la propriété dans une mémoire tampon que vous allouez.

## <a name="syntax"></a>Syntaxe

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

## <a name="constants"></a>Constantes

### <a name="instanceluid"></a>InstanceLuid

Spécifie la propriété de l’adaptateur <em>InstanceLuid</em> , qui contient un identificateur unique local représentant l’adaptateur. Cette valeur reste constante pendant la durée de vie de cet adaptateur. Le LUID d’un adaptateur change au redémarrage, à la mise à niveau du pilote ou à la désactivation/activation de l’appareil.

La propriété de l’adaptateur <em>InstanceLuid</em> a le type <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.

### <a name="driverversion"></a>DriverVersion

Spécifie la propriété de l’adaptateur <em>DriverVersion</em> , qui contient la version du pilote, représentée dans <b>Word</b>s comme un <b>LARGE_INTEGER</b>.

La propriété de l’adaptateur <em>DriverVersion</em> a le type <b>uint64_t</b>, qui représente une valeur booléenne.

### <a name="driverdescription"></a>DriverDescription

Spécifie la propriété de l’adaptateur <em>DriverDescription</em> , qui contient un tableau de <b>caractères</b>se terminant par un caractère null, qui décrit le pilote, comme spécifié par le pilote, dans l’encodage <a href="/windows/win32/intl/unicode">UTF-8</a> .

La propriété de l’adaptateur <em>DriverDescription</em> est de type <b>char *</b>.

### <a name="hardwareid"></a>HardwareID

Spécifie la propriété de l’adaptateur <em>HardwareID</em> , qui représente les parties de l’ID de matériel PNP.

La propriété de l’adaptateur <em>HardwareID</em> a le type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.

### <a name="kmdmodelversion"></a>KmdModelVersion

Spécifie la propriété de l’adaptateur <em>KmdModelVersion</em> , qui représente le modèle de pilote.

La propriété de l’adaptateur <em>KmdModelVersion</em> a le type <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.

### <a name="computepreemptiongranularity"></a>ComputePreemptionGranularity

Spécifie la propriété de l’adaptateur <em>ComputePreemptionGranularity</em> , qui représente la granularité de préemption du calcul.

La propriété de l’adaptateur <em>ComputePreemptionGranularity</em> a le type <b>uint16_t</b>, représentant une valeur de <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> .

### <a name="graphicspreemptiongranularity"></a>GraphicsPreemptionGranularity

Spécifie la propriété de l’adaptateur <em>GraphicsPreemptionGranularity</em> , qui représente la granularité de préemption des graphiques.

La propriété de l’adaptateur <em>GraphicsPreemptionGranularity</em> a le type <b>uint16_t</b>, représentant une valeur de <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> .

### <a name="dedicatedadaptermemory"></a>DedicatedAdapterMemory

Spécifie la propriété de l’adaptateur <em>DedicatedAdapterMemory</em> , qui représente le nombre d’octets de mémoire d’adaptateur dédiée qui ne sont pas partagés avec l’UC.

La propriété de l’adaptateur <em>DedicatedVideoMemory</em> a le type <b>uint64_t</b>.

### <a name="dedicatedsystemmemory"></a>DedicatedSystemMemory

Spécifie la propriété de l’adaptateur <em>DedicatedSystemMemory</em> , qui représente le nombre d’octets de mémoire système dédiée qui ne sont pas partagés avec l’UC. Cette mémoire est allouée à partir de la mémoire système disponible au moment du démarrage.

La propriété de l’adaptateur <em>DedicatedSystemMemory</em> a le type <b>uint64_t</b>.

### <a name="sharedsystemmemory"></a>SharedSystemMemory

Spécifie la propriété de l’adaptateur <em>SharedSystemMemory</em> , qui représente le nombre d’octets de mémoire système partagée. Il s’agit de la valeur maximale de la mémoire système qui peut être consommée par l’adaptateur lors de l’opération. Toute mémoire accessoire consommée par le pilote lorsqu’il gère et utilise la mémoire vidéo est supplémentaire.

La propriété de l’adaptateur <em>SharedSystemMemory</em> a le type <b>uint64_t</b>.

### <a name="acgcompatible"></a>AcgCompatible

Spécifie la propriété de l’adaptateur <em>AcgCompatible</em> , qui indique si l’adaptateur est compatible avec les processus qui appliquent la protection de code arbitraire.

La propriété de l’adaptateur <em>AcgCompatible</em> est de type <b>bool</b>.

### <a name="ishardware"></a>IsHardware

Spécifie la propriété de l’adaptateur <em>IsHardware</em> , qui détermine s’il s’agit ou non d’un adaptateur matériel. Un adaptateur qui n’est pas une carte matérielle est un adaptateur logiciel.

La propriété de l’adaptateur <em>IsHardware</em> est de type <b>bool</b>.

### <a name="isintegrated"></a>IsIntegrated

Spécifie la propriété de l’adaptateur <em>IsIntegrated</em> , qui détermine si l’adaptateur est signalé comme étant un processeur graphique intégré (iGPU).

La propriété de l’adaptateur <em>IsIntegrated</em> est de type <b>bool</b>.

### <a name="isdetachable"></a>IsDetachable

Spécifie la propriété de l’adaptateur <em>IsDetachable</em> , qui détermine si l’adaptateur a été signalé comme pouvant être détaché ou amovible.

La propriété de l’adaptateur <em>IsDetachable</em> est de type <b>bool</b>.

<b>Remarque</b>: Même si <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter :: GetProperty</a> indique `false` pour cette propriété, l’adaptateur a toujours la possibilité d’être signalé comme étant supprimé, comme dans le cas d’un dysfonctionnement ou d’une mise à jour de pilote.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter :: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter :: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)