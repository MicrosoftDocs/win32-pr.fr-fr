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
# <a name="dmlcreatedevice1-function-directmlh"></a>DMLCreateDevice1, fonction (directml. h)

Crée un appareil DirectML pour un appareil Direct3D 12 donné.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a>Paramètres

`d3d12Device`

Type : <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>*</b>

Pointeur vers un [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) représentant le périphérique Direct3D 12 sur lequel créer l’appareil DirectML. DirectML prend en charge tous les niveaux de fonctionnalité D3D et les périphériques Direct3D 12 créés sur n’importe quelle carte, y compris WARP. Toutefois, toutes les fonctionnalités de DirectML peuvent ne pas être disponibles en fonction des fonctionnalités de l’appareil Direct3D 12. Pour plus d’informations, consultez [IDMLDevice :: CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) .

Si l’appel à **DMLCreateDevice1** réussit, l’appareil DirectML gère une référence forte au périphérique Direct3D 12 fourni.

`flags`

Type : <b>DML_CREATE_DEVICE_FLAGS</b>

Valeur [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) spécifiant des options de création d’appareils supplémentaires.

`minimumFeatureLevel`

Type : <b>DML_FEATURE_LEVEL</b>

Valeur [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) spécifiant la prise en charge de niveau de fonctionnalité minimale requise.

Ce paramètre peut être utile pour les appelants qui requièrent une version spécifique de DirectML, mais qui peuvent se trouver dans une version antérieure de DirectML. Cela peut se produire, par exemple, lorsque l’utilisateur exécute votre application sur une version antérieure de Windows 10.

Les applications qui dépendent explicitement de la fonctionnalité introduite dans un niveau de fonctionnalité particulier peuvent la spécifier en tant que *minimumFeatureLevel*. Cela permet de garantir que **DMLCreateDevice1** ne fonctionnera pas, sauf si l’implémentation sous-jacente est *au moins* aussi efficace que le niveau de fonctionnalité minimal requis.

Notez que comme ce paramètre spécifie un niveau de fonctionnalité *minimal* , l’appareil DirectML sous-jacent peut en fait prendre en charge un niveau de fonctionnalité supérieur à la valeur minimale demandée. Une fois la création de l’appareil réussie, vous pouvez interroger tous les niveaux de fonctionnalité pris en charge par cet appareil à l’aide de [IDMLDevice :: CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).

`riid`

Type : <b>REFIID</b>

Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans l' <i>appareil</i>. Il doit s’agir du GUID de [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).

`ppv`

Type : \_ com \_ Outptr \_ OPT \_ <b>void * *</b>

Pointeur vers un bloc de mémoire qui reçoit un pointeur vers l’appareil. Il s’agit de l’adresse d’un pointeur vers un [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), représentant l’appareil DirectML créé.


## <a name="return-value"></a>Valeur retournée

Type : [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Si la fonction est réussie, elle retourne <b>S_OK</b>. Sinon, elle retourne un code d’erreur [HRESULT](/windows/desktop/winprog/windows-data-types) .

Si cette version de DirectML ne prend pas en charge les *minimumFeatureLevel* demandés, cette fonction retourne **DXGI_ERROR_UNSUPPORTED**.

La fonctionnalité outils Graphics à la demande (DOM) doit être installée pour pouvoir utiliser les couches de débogage DirectML. Si l’indicateur de [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) est spécifié dans *Flags* et que les couches de débogage ne sont pas installées, **DMLCreateDevice1** retourne **DXGI_ERROR_SDK_COMPONENT_MISSING**.

## <a name="remarks"></a>Notes

Une version plus récente de cette fonction, [DMLCreateDevice1](), a été introduite dans DirectML version 1.1.0. **DMLCreateDevice1** est équivalent à l’appel de **DMLCreateDevice1** et à la fourniture d’un *minimumFeatureLevel* de [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).

## <a name="availability"></a>Disponibilité

Cette API a été introduite dans la version DirectML `1.1.0` .

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | directml. h |
| **Bibliothèque** | DirectML. lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>Voir aussi

* [Énumération DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Historique des versions DirectML](../dml-version-history.md)
* [Historique des niveaux de fonctionnalité DirectML](/windows/win32/direct3d12/dml-feature_level-history)    
* [Utilisation de la couche de débogage DirectML](../dml-debug-layer.md)