---
title: Structure CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT (D3dx12. h)
description: Structure d’assistance basée sur un modèle utilisée pour encapsuler le type de sous-objet et les paires de données de sous-objet en tant qu’objet unique approprié pour une description de flux.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- Structure CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d945296ae4ee09710b74b9fdf2259251632d25fb309ede2983858c0c59be72d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729479"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a>CD3DX12 structure de sous- \_ objet du flux d’État du pipeline \_ \_ \_

Structure d’assistance basée sur un modèle utilisée pour encapsuler le type de sous-objet et les paires de données de sous-objet en tant qu’objet unique approprié pour une description de flux.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**Sous \_ - \_ \_ objet de flux d’État du pipeline CD3DX12 \_**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un sous- \_ objet de flux d’état de pipeline CD3DX12 \_ \_ \_ .

</dd> <dt>

**CD3DX12 \_ \_Sous- \_ \_ objet de flux d’État du pipeline (** InnerStructType * * const &i) * *
</dt> <dd>

Crée une instance de \_ modèle de sous-objet de flux d’état de pipeline CD3DX12 \_ \_ \_ , initialisée avec un type de sous-objet de [**type de sous-objet d’état de pipeline D3D12 et des données de \_ \_ \_ \_ sous**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) -objet copiées à partir de *i*. Le type de sous-objet et le type de données de sous-objet sont spécifiés en tant que paramètres de modèle, **type** et **InnerStructType**, respectivement. Pour plus d’informations, consultez la section Notes ci-dessous.

</dd> <dt>

**opérateur = (** InnerStructType * * const& i) * *
</dt> <dd>

Opérateur d’assignation de copie.

</dd> <dt>

**const, opérateur **InnerStructType**()**
</dt> <dd>

Conversion implicite vers le type de données de sous-objet donné par le paramètre de modèle **InnerStructType** .

</dd> </dl>

## <a name="remarks"></a>Remarques

\_ \_ \_ Le sous-objet de flux d’État du pipeline CD3DX12 \_ est un modèle défini comme suit :


```C++
template <typename InnerStructType, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type, typename DefaultArg = InnerStructType>
class alignas(void*) CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
{
private:
    D3D12_PIPELINE_STATE_SUBOBJECT_TYPE _Type;
    InnerStructType _Inner;
public:
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT() : _Type(Type), _Inner(DefaultArg()) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const& i) : _Type(Type), _Inner(i) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT& operator=(InnerStructType const& i) { _Inner = i; return *this; }
    operator InnerStructType() const { return _Inner; }
};  
          
```



Le paramètre de modèle **InnerStructType** spécifie le type de données de sous-objet ; autrement dit, les détails du sous-objet à encoder dans un flux. Le **type** de paramètre de modèle spécifie le type de sous-objet. autrement dit, le type de la structure spécifiée par le paramètre de modèle **InnerStructType**. Le paramètre de modèle **defaultArg (** spécifie une valeur facultative à laquelle les données de sous-objet sont initialisées lorsqu’une instance de l’instanciation de modèle correspondante est construite par défaut ; par exemple, pour construire par défaut un [**flux d’état de pipeline CD3DX12, le \_ \_ \_ \_ \_ desc fusionné**](cd3dx12-pipeline-state-stream-blend-desc.md) est initialisé avec les valeurs par défaut d’état de fusion communes à l’aide de [**CD3DX12 \_ par défaut**](cd3dx12-default.md).

Voici les instanciations de modèle définies :

-   [**\_Indicateurs du \_ flux d’État du PIPELINe CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-flags.md)
-   [**\_Masque de \_ \_ nœud du flux d’État du pipeline CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-node-mask.md)
-   [**\_ \_ \_ Signature racine du flux d’état \_ du pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-root-signature.md)
-   [**\_ \_ \_ \_ Disposition d’entrée de flux d’état de pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-input-layout.md)
-   [**CD3DX12 de \_ flux d’état de pipeline \_ IB- \_ \_ \_ \_ valeur de coupe \_**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [**\_ \_ \_ Topologie primitive du flux d’état \_ du pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [**\_Flux d’état de pipeline CD3DX12 \_ \_ \_ et**](cd3dx12-pipeline-state-stream-vs.md)
-   [**\_Flux d’état de pipeline CD3DX12 \_ \_ \_ GS**](cd3dx12-pipeline-state-stream-gs.md)
-   [**Sortie du flux de flux d' \_ État du pipeline CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-stream-output.md)
-   [**CD3DX12 de \_ flux d’État du pipeline \_ \_ \_ HS**](cd3dx12-pipeline-state-stream-hs.md)
-   [**CD3DX12 \_ de \_ flux d’État du pipeline \_ \_**](cd3dx12-pipeline-state-stream-ds.md)
-   [**\_Flux d’État du pipeline CD3DX12 \_ \_ \_ PS**](cd3dx12-pipeline-state-stream-ps.md)
-   [**\_Flux d’État du pipeline CD3DX12 \_ \_ \_ CS**](cd3dx12-pipeline-state-stream-cs.md)
-   [**\_ \_ \_ \_ Mélange DESC du flux d’État du pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [**\_Stencil de \_ \_ profondeur du flux d’État du pipeline CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [**\_Profondeur du flux d’État du pipeline CD3DX12 \_ \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [**\_Format du \_ \_ stencil de profondeur du flux d’État du \_ \_ pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [**\_Rastériseur de \_ flux d’état de PIPELINe CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [**\_ \_ \_ \_ Formats cibles de rendu du flux d' \_ état \_ du pipeline CD3DX12**](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [**\_Exemple de flux d’état de pipeline CD3DX12 \_ \_ \_ \_ desc**](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [**\_Exemple de \_ masque de \_ flux d’état de \_ pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [**\_Flux d' \_ État du pipeline CD3DX12 \_ \_ mis en cache \_**](cd3dx12-pipeline-state-stream-cached-pso.md)

Le CD3DX12 de pipeline d’état de pipeline [**\_ \_ \_ \_ \_ desc**](cd3dx12-pipeline-state-stream-blend-desc.md), le [**\_ \_ \_ \_ \_ stencil de profondeur**](cd3dx12-pipeline-state-stream-depth-stencil.md)de flux d’état de pipeline CD3DX12, les structures de de flux d’état de [**\_ pipeline CD3DX12 \_ \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)et les structures de rastérisation de [**flux d' \_ \_ état \_ \_ de pipeline CD3DX12**](cd3dx12-pipeline-state-stream-rasterizer.md) sont définis pour initialiser leurs données de sous-objet avec les valeurs par défaut communes utilisant [**CD3DX12 \_ par défaut**](cd3dx12-default.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Type de \_ \_ sous-objet état \_ du pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

