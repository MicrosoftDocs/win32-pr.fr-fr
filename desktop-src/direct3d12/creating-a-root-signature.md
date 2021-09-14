---
title: Création d’une signature racine
description: Les signatures racines sont une structure de données complexe contenant des structures imbriquées.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87209dfc324b950a74d2b31e5f1a1f6326792b9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216492"
---
# <a name="creating-a-root-signature"></a>Création d’une signature racine

Les signatures racines sont une structure de données complexe contenant des structures imbriquées. Celles-ci peuvent être définies par programme à l’aide de la définition de la structure de données ci-dessous (qui comprend des méthodes pour aider à initialiser les membres). Elles peuvent également être créées dans le langage HLSL (High Level Shading Language), ce qui donne l’avantage que le compilateur validera tôt que la disposition soit compatible avec le nuanceur.

L’API pour la création d’une signature racine utilise une version sérialisée (autonome, à pointeur libre) de la description de la disposition décrite ci-dessous. Une méthode est fournie pour générer cette version sérialisée à partir de la structure de données C++, mais une autre façon d’obtenir une définition de signature racine sérialisée est de la récupérer à partir d’un nuanceur qui a été compilé avec une signature racine.

Si vous souhaitez tirer parti des optimisations de pilotes pour les descripteurs de signature racine et les données, reportez-vous à la [signature racine Version 1,1](root-signature-version-1-1.md)

-   [Types de liaison de table de descripteur](#descriptor-table-bind-types)
-   [Plage du descripteur](#descriptor-range)
-   [Disposition du tableau de descripteurs](#descriptor-table-layout)
-   [Constantes racine](#root-constants)
-   [Descripteur racine](#root-descriptor)
-   [Visibilité du nuanceur](#shader-visibility)
-   [Définition de signature racine](#root-signature-definition)
-   [Sérialisation/désérialisation de la structure de données de la signature racine](/windows)
-   [API de création de signature racine](#root-signature-creation-api)
-   [Signature racine dans les objets d’état de pipeline](#root-signature-in-pipeline-state-objects)
-   [Code pour définir une signature racine de la version 1,1](#code-for-defining-a-version-11-root-signature)
-   [Rubriques connexes](#related-topics)

## <a name="descriptor-table-bind-types"></a>Types de liaison de table de descripteur

Le [**\_ \_ \_ type de plage**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) du descripteur D3D12 enum définit les types de descripteurs qui peuvent être référencés dans le cadre d’une définition de présentation de tableau de descripteurs.

C’est une plage dans laquelle, par exemple, si une partie d’une table de descripteur a 100 SRVs, cette plage peut être déclarée dans une entrée au lieu de 100. Par conséquent, une définition de table de descripteur est une collection de plages.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a>Plage du descripteur

La structure de la [**\_ \_ plage du descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) définit une plage de descripteurs d’un type donné (par exemple, SRVs) dans une table de descripteur.

La `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro peut généralement être utilisée pour le `OffsetInDescriptorsFromTableStart` paramètre de [**la \_ \_ plage du descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Cela signifie que vous ajoutez la plage de descripteurs qui est définie après le précédent dans la table du descripteur. Si l’application souhaite des descripteurs d’alias ou, pour une raison quelconque, souhaite ignorer des emplacements, elle peut `OffsetInDescriptorsFromTableStart` être définie sur le décalage souhaité. La définition de plages qui se chevauchent de types différents n’est pas valide.

L’ensemble de registres de nuanceur spécifié par la combinaison de, `RangeType` `NumDescriptors` , `BaseShaderRegister` et `RegisterSpace` ne peut pas entrer en conflit ou se chevaucher dans toutes les déclarations d’une signature racine qui ont une [**\_ \_ visibilité de nuanceur D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) commune (consultez la section de visibilité du nuanceur ci-dessous).

## <a name="descriptor-table-layout"></a>Disposition du tableau de descripteurs

La structure de [**\_ \_ \_ table de descripteurs racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) déclare la disposition d’une table de descripteurs sous la forme d’une collection de plages de descripteur qui apparaissent une après l’autre dans un tas de descripteur. Les échantillonneurs ne sont pas autorisés dans la même table de descripteurs que CBV/UAV/SRVs.

Ce struct est utilisé lorsque le type d’emplacement de signature racine a la valeur `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .

Pour définir un tableau de descripteurs Graphics (CBV, SRV, UAV, Sampler), utilisez [**ID3D12GraphicsCommandList :: SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).

Pour définir une table de descripteurs de calcul, utilisez [**ID3D12GraphicsCommandList :: SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).

## <a name="root-constants"></a>Constantes racine

La structure de [**\_ \_ constantes racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) déclare des constantes inline dans la signature racine qui s’affichent dans les nuanceurs comme une mémoire tampon constante.

Ce struct est utilisé lorsque le type d’emplacement de signature racine a la valeur `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .

## <a name="root-descriptor"></a>Descripteur racine

La structure du descripteur [**\_ \_ racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) déclare les descripteurs (qui apparaissent dans les nuanceurs) Inline dans la signature racine.

Ce struct est utilisé lorsque le type d’emplacement de signature racine a la valeur `D3D12_ROOT_PARAMETER_TYPE_CBV` , `D3D12_ROOT_PARAMETER_TYPE_SRV` ou `D3D12_ROOT_PARAMETER_TYPE_UAV` .

## <a name="shader-visibility"></a>Visibilité du nuanceur

Le membre de l’énumération de [**\_ \_ visibilité du nuanceur D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) défini dans le paramètre de visibilité du nuanceur du [**\_ \_ paramètre racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) détermine les nuanceurs qui voient le contenu d’un emplacement de signature racine donné. Compute utilise toujours \_ All (puisqu’il n’y a qu’une seule étape active). Les graphiques peuvent choisir, mais s’ils utilisent \_ tous, toutes les étapes de nuanceur voient tout ce qui est lié à l’emplacement de signature racine.

L’une des utilisations de la visibilité du nuanceur est l’aide pour les nuanceurs qui sont créés en attendant des liaisons différentes par étape de nuanceur à l’aide d’un espace de noms qui se chevauche. Par exemple, un nuanceur vertex peut déclarer :

```hlsl
Texture2D foo : register(t0);
```

et le nuanceur de pixels peut également déclarer :

```hlsl
Texture2D bar : register(t0);
```

Si l’application établit une liaison de signature racine avec T0 VISIBILity \_ All, les deux nuanciers voient la même texture. Si le nuanceur définit réellement que chaque nuanceur souhaite voir différentes textures, il peut définir 2 emplacements de signature racine avec un vertex de visibilité \_ et un \_ Pixel. Quelle que soit la visibilité sur un emplacement de signature racine, il a toujours le même coût (coût uniquement en fonction de l’SlotType) vers une taille de signature maximale fixe.

Sur un matériel D3D11 de bas niveau, la visibilité du NUANCEur \_ est également prise en compte lors de la validation des tailles de tables de descripteurs dans une disposition racine, car certains matériels d3d11 ne peuvent prendre en charge qu’une quantité maximale de liaisons par étape. Ces restrictions sont imposées uniquement lors de l’exécution sur du matériel de bas niveau et ne limitent pas du tout le matériel moderne.

Si une signature racine a plusieurs tables de descripteur définies qui se chevauchent dans l’espace de noms (les liaisons de Registre au nuanceur) et que l’une d’entre elles indique \_ tout pour la visibilité, la disposition n’est pas valide (la création échoue).

## <a name="root-signature-definition"></a>Définition de signature racine

La structure de la [**\_ signature racine D3D12 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) peut contenir des tables de descripteurs et des constantes incluses, chaque type d’emplacement défini par la structure de [**\_ \_ paramètres racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) et le [**\_ \_ \_ type de paramètre racine D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type)Enum.

Pour initier un emplacement de signature racine, reportez-vous aux méthodes **\* \* \* SetComputeRoot** et **SetGraphicsRoot \* \* \*** de [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

Les échantillonneurs statiques sont décrits dans la signature racine à l’aide de la structure d' [**\_ \_ échantillonneur statique D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

Un certain nombre d’indicateurs limitent l’accès de certains nuanceurs à la signature racine, reportez-vous aux [**\_ \_ \_ indicateurs de signature racine D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

## <a name="root-signature-data-structure-serialization--deserialization"></a>Sérialisation/désérialisation de la structure de données de la signature racine

Les méthodes décrites dans cette section sont exportées par D3D12Core.dll et fournissent des méthodes pour sérialiser et désérialiser une structure de données de signature racine.

La forme sérialisée est celle qui est transmise dans l’API lors de la création d’une signature racine. Si un nuanceur a été créé avec une signature racine dans celui-ci (lorsque cette fonctionnalité est ajoutée), le nuanceur compilé contient déjà une signature racine sérialisée dans celui-ci.

Si une application génère de façon procédurale une structure de données [**\_ \_ \_ desc signature racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) , elle doit établir la forme sérialisée à l’aide de [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature). Sortie de qui peut être passée dans [**ID3D12Device :: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).

Si une application a déjà une signature racine sérialisée, ou a un nuanceur compilé qui contient une signature racine et souhaite découvrir par programmation la définition de la disposition (appelée « réflexion »), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) peut être appelé. Cela génère une interface [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) , qui contient une méthode pour retourner la structure de données [**\_ \_ \_ desc de signature racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) désérialisée. L’interface possède la durée de vie de la structure de données désérialisée.

## <a name="root-signature-creation-api"></a>API de création de signature racine

L’API [**ID3D12Device :: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) prend une version sérialisée d’une signature racine.

## <a name="root-signature-in-pipeline-state-objects"></a>Signature racine dans les objets d’état de pipeline

Les méthodes permettant de créer l’état du pipeline ([**ID3D12Device :: CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) et [**ID3D12Device :: CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) prennent une interface [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) facultative comme paramètre d’entrée (stocké dans une structure [**\_ desc d' \_ \_ état \_ de pipeline Graphics D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ). Cette opération remplace toute signature racine déjà présente dans les nuanceurs.

Si une signature racine est passée dans l’une des méthodes Create Pipeline State, cette signature racine est validée par rapport à tous les nuanceurs de l’PSO pour la compatibilité et donnée au pilote à utiliser avec tous les nuanceurs. Si l’un des nuanceurs a une signature racine différente, il est remplacé par la signature racine passée dans l’API. Si aucune signature racine n’est transmise, tous les nuanceurs transmis doivent avoir une signature racine et doivent correspondre, ce qui sera attribué au pilote. La définition d’un PSO sur une liste de commandes ou une offre groupée ne modifie pas la signature racine. Cela est accompli par les méthodes [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) et [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature). À l’heure où Draw (Graphics)/Dispatch (Compute) est appelé, l’application doit s’assurer que le PSO actuel correspond à la signature racine actuelle ; dans le cas contraire, le comportement n’est pas défini.

## <a name="code-for-defining-a-version-11-root-signature"></a>Code pour définir une signature racine de la version 1,1

L’exemple ci-dessous montre comment créer une signature racine au format suivant :



| RootParameterIndex                       | Contenu                                               | Valeurs                                             |
|------------------------|------------------------------------------------|----------------------------------------------|                                              
| \[0\]                  | Constantes racine : {B2}                         | (1 CBV)                                      |
| \[1\]                  | Table du descripteur : {T2-T7, U0-U3}             | (6 SRVs + 4 UAVs)                            |
| \[2\]                  | CBV racine : {B0}                               | (1 CBV, données statiques)                         |
| \[3\]                  | Tableau du descripteur : {S0-S1}                    | (2 échantillonneurs)                                 |
| \[4\]                  | Table du descripteur : {T8-Unlimited}           | (non lié à \# SRVs, descripteurs volatils) |
| \[5\]                  | Table du descripteur : {(T0, space1)-Unlimited} | (non lié à \# SRVs, descripteurs volatils) |
| \[6\]                  | Tableau du descripteur : {B1}                       | (1 CBV, données statiques)                         |



 

Si la plupart des parties de la signature racine sont utilisées la plupart du temps, il peut être préférable d’avoir un changement trop fréquent de la signature racine. Les applications doivent trier les entrées de la signature racine le plus souvent au moins. Quand une application modifie les liaisons à n’importe quelle partie de la signature racine, il peut être nécessaire d’effectuer une copie de tout ou partie de l’état de la signature racine, ce qui peut devenir un coût non négligeable lorsqu’elle est multipliée par de nombreuses modifications d’État.

En outre, la signature racine définit un échantillonneur statique qui effectue un filtrage de texture anisotrope au registre du nuanceur S3.

Une fois cette signature racine liée, les tables de descripteurs, les CBV racines et les constantes peuvent être affectés à l' \[ espace de paramètre 0.. 6 \] . par exemple, les tables de descripteurs (plages dans un tas de descripteur) peuvent être liées à chacun des paramètres racine \[ 1 \] et \[ 3.. 6 \] .

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

Le code suivant illustre la façon dont la signature racine ci-dessus peut être utilisée dans une liste de commandes Graphics.

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(2,pHeaps);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Signatures racine](root-signatures.md)
</dt> <dt>

[Spécification de signatures racine en langage HLSL](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[Utilisation d’une signature racine](using-a-root-signature.md)
</dt> </dl>

 

 
