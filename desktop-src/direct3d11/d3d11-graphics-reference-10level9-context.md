---
title: Méthodes 10Level9 ID3D11DeviceContext
description: Cette section répertorie les différences entre chaque niveau de fonctionnalité 10Level9 et le niveau de fonctionnalité D3D \_ \_ \_ 11 \_ 0 et supérieur pour les méthodes ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e268f45465139e49afe0f81a64eeeb93939734e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473125"
---
# <a name="10level9-id3d11devicecontext-methods"></a>Méthodes 10Level9 ID3D11DeviceContext

Cette section répertorie les différences entre chaque niveau de fonctionnalité 10Level9 et le niveau de fonctionnalité D3D \_ \_ \_ 11 \_ 0 et supérieur pour les méthodes [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

-   [ID3D11DeviceContext :: CopySubresourceRegion](#id3d11devicecontextcopysubresourceregion)
-   [ID3D11DeviceContext :: CopyResource](#id3d11devicecontextcopyresource)
-   [ID3D11DeviceContext :: CopyStructureCount](#id3d11devicecontextcopystructurecount)
-   [ID3D11DeviceContext :: ClearUnorderedAccessViewFloat](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [ID3D11DeviceContext :: ClearUnorderedAccessViewUint](#id3d11devicecontextclearunorderedaccessviewuint)
-   [ID3D11DeviceContext :: ClearRenderTargetView](#id3d11devicecontextclearrendertargetview)
-   [ID3D11DeviceContext :: CSSetConstantBuffers](#id3d11devicecontextcssetconstantbuffers)
-   [ID3D11DeviceContext :: CSSetSamplers](#id3d11devicecontextcssetsamplers)
-   [ID3D11DeviceContext :: CSSetShader](#id3d11devicecontextcssetshader)
-   [ID3D11DeviceContext :: CSSetShaderResources](#id3d11devicecontextcssetshaderresources)
-   [ID3D11DeviceContext :: CSSetUnorderedAccessViews](#id3d11devicecontextcssetunorderedaccessviews)
-   [ID3D11DeviceContext ::D ispatch](#id3d11devicecontextdispatch)
-   [ID3D11DeviceContext ::D ispatchIndirect](#id3d11devicecontextdispatchindirect)
-   [ID3D11DeviceContext ::D RAW](#id3d11devicecontextdraw)
-   [ID3D11DeviceContext ::D rawAuto](#id3d11devicecontextdrawauto)
-   [ID3D11DeviceContext ::D rawIndexed](#id3d11devicecontextdrawindexed)
-   [ID3D11DeviceContext ::D rawIndexedInstanced](#id3d11devicecontextdrawindexedinstanced)
-   [ID3D11DeviceContext ::D rawIndexedInstancedIndirect](#id3d11devicecontextdrawindexedinstancedindirect)
-   [ID3D11DeviceContext ::D rawInstanced](#id3d11devicecontextdrawinstanced)
-   [ID3D11DeviceContext ::D rawInstancedIndirect](#id3d11devicecontextdrawinstancedindirect)
-   [ID3D11DeviceContext ::D SSetConstantBuffers](#id3d11devicecontextdssetconstantbuffers)
-   [ID3D11DeviceContext ::D SSetSamplers](#id3d11devicecontextdssetsamplers)
-   [ID3D11DeviceContext ::D SSetShader](#id3d11devicecontextdssetshader)
-   [ID3D11DeviceContext ::D SSetShaderResources](#id3d11devicecontextdssetshaderresources)
-   [ID3D11DeviceContext :: GSSetConstantBuffers](#id3d11devicecontextgssetconstantbuffers)
-   [ID3D11DeviceContext :: GSSetSamplers](#id3d11devicecontextgssetsamplers)
-   [ID3D11DeviceContext :: GSSetShader](#id3d11devicecontextgssetshader)
-   [ID3D11DeviceContext :: GSSetShaderResources](#id3d11devicecontextgssetshaderresources)
-   [ID3D11DeviceContext :: HSSetConstantBuffers](#id3d11devicecontexthssetconstantbuffers)
-   [ID3D11DeviceContext :: HSSetSamplers](#id3d11devicecontexthssetsamplers)
-   [ID3D11DeviceContext :: HSSetShader](#id3d11devicecontexthssetshader)
-   [ID3D11DeviceContext :: HSSetShaderResources](#id3d11devicecontexthssetshaderresources)
-   [ID3D11DeviceContext::IASetIndexBuffer](#id3d11devicecontextiasetindexbuffer)
-   [ID3D11DeviceContext :: IASetPrimitiveTopology](#id3d11devicecontextiasetprimitivetopology)
-   [ID3D11DeviceContext :: OMSetBlendState](#id3d11devicecontextomsetblendstate)
-   [ID3D11DeviceContext :: OMSetRenderTargets](#id3d11devicecontextomsetrendertargets)
-   [ID3D11DeviceContext :: OMSetRenderTargetsAndUnorderedAccessViews](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [ID3D11DeviceContext ::P SSetConstantBuffers](#id3d11devicecontextpssetconstantbuffers)
-   [ID3D11DeviceContext ::P SSetSamplers](#id3d11devicecontextpssetsamplers)
-   [ID3D11DeviceContext ::P SSetShader](#id3d11devicecontextpssetshader)
-   [ID3D11DeviceContext ::P SSetShaderResources](#id3d11devicecontextpssetshaderresources)
-   [ID3D11DeviceContext :: RSSetScissorRects](#id3d11devicecontextrssetscissorrects)
-   [ID3D11DeviceContext :: RSSetViewports](#id3d11devicecontextrssetviewports)
-   [ID3D11DeviceContext :: SetPredication](#id3d11devicecontextsetpredication)
-   [ID3D11DeviceContext :: SOSetTargets](#id3d11devicecontextsosettargets)
-   [ID3D11DeviceContext :: VSSetConstantBuffers](#id3d11devicecontextvssetconstantbuffers)
-   [ID3D11DeviceContext :: VSSetSamplers](#id3d11devicecontextvssetsamplers)
-   [ID3D11DeviceContext :: VSSetShader](#id3d11devicecontextvssetshader)
-   [ID3D11DeviceContext :: VSSetShaderResources](#id3d11devicecontextvssetshaderresources)
-   [Rubriques connexes](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a>ID3D11DeviceContext :: CopySubresourceRegion




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Seuls les Texture2D et les tampons peuvent être copiés dans la mémoire accessible par le GPU.<br /> Les Texture3D ne peuvent pas être copiés de la mémoire accessible par le GPU vers la mémoire accessible par le processeur.<br /> Toutes les ressources qui ont uniquement des D3D10_BIND_SHADER_RESOURCE ne peuvent pas être copiées de la mémoire accessible par le GPU vers la mémoire accessible par le processeur.<br /> Vous ne pouvez pas copier les textures de volume mipmapped. <br /> $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcopyresource"></a>ID3D11DeviceContext :: CopyResource




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Seuls les Texture2D et les tampons peuvent être copiés dans la mémoire accessible par le GPU.<br /> Les Texture3D ne peuvent pas être copiés de la mémoire accessible par le GPU vers la mémoire accessible par le processeur.<br /> Toutes les ressources qui ont uniquement des D3D10_BIND_SHADER_RESOURCE ne peuvent pas être copiées de la mémoire accessible par le GPU vers la mémoire accessible par le processeur.<br /> $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcopystructurecount"></a>ID3D11DeviceContext :: CopyStructureCount




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a>ID3D11DeviceContext :: ClearUnorderedAccessViewFloat




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a>ID3D11DeviceContext :: ClearUnorderedAccessViewUint




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearrendertargetview"></a>ID3D11DeviceContext :: ClearRenderTargetView




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Seule la première tranche du tableau sera effacée. Les applications doivent créer une vue de la cible de rendu pour chaque face ou tranche de tableau, puis effacer chaque vue individuellement. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetconstantbuffers"></a>ID3D11DeviceContext :: CSSetConstantBuffers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetsamplers"></a>ID3D11DeviceContext :: CSSetSamplers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetshader"></a>ID3D11DeviceContext :: CSSetShader




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetshaderresources"></a>ID3D11DeviceContext :: CSSetShaderResources




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a>ID3D11DeviceContext :: CSSetUnorderedAccessViews




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdispatch"></a>ID3D11DeviceContext ::D ispatch




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdispatchindirect"></a>ID3D11DeviceContext ::D ispatchIndirect




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdraw"></a>ID3D11DeviceContext ::D RAW



| Niveau de fonctionnalité             | Différences de comportement                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1 | Le nombre de primitives ne peut pas dépasser 65535.<br/> Les textures ne peuvent pas se répéter sur une primitive plus de 128 fois.<br/>    |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2 | Le nombre de primitives ne peut pas dépasser 1048575.<br/> Les textures ne peuvent pas se répéter sur une primitive plus de 2048 fois.<br/> |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3 | Le nombre de primitives ne peut pas dépasser 1048575.<br/> Les textures ne peuvent pas se répéter sur une primitive plus de 8192 fois.<br/> |



 

## <a name="id3d11devicecontextdrawauto"></a>ID3D11DeviceContext ::D rawAuto




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdrawindexed"></a>ID3D11DeviceContext ::D rawIndexed



| Niveau de fonctionnalité             | Différences de comportement                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 1 | Le nombre de primitives ne peut pas dépasser 65535.<br/> Les textures ne peuvent pas se répéter sur une primitive plus de 128 fois.<br/> Les valeurs d’index ne peuvent pas dépasser 65534.<br/> Listes de points indexées non prises en charge.<br/>      |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 2 | Le nombre de primitives ne peut pas dépasser 1048575.<br/> Les textures ne peuvent pas se répéter sur une primitive plus de 2048 fois.<br/> Les valeurs d’index ne peuvent pas dépasser 1048575.<br/> Listes de points indexées non prises en charge.<br/> |
| \_Niveau de fonctionnalité D3D \_ \_ 9 \_ 3 | Le nombre de primitives ne peut pas dépasser 1048575.<br/> Les textures ne peuvent pas se répéter sur une primitive plus de 8192 fois.<br/> Les valeurs d’index ne peuvent pas dépasser 1048575.<br/> Listes de points indexées non prises en charge.<br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a>ID3D11DeviceContext ::D rawIndexedInstanced




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Le nombre de primitives ne peut pas dépasser 1048575.<br /> Les textures ne peuvent pas se répéter sur une primitive plus de 8192 fois.<br /> Les valeurs d’index ne peuvent pas dépasser 1048575.<br /><blockquote>[!Note]<br />Quand vous appelez la méthode <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> avec un nuanceur de sommets qui est lié au pipeline et qui n’importe pas de données par instance, certains matériels graphiques Direct3D 9 peuvent ne rien dessiner. En particulier, si le nuanceur vertex n’utilise pas de données par instance, l’appel de <strong>DrawIndexedInstanced</strong> avec 1 instance n’est pas équivalent à l’appel de <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</blockquote><br /> | 




 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a>ID3D11DeviceContext ::D rawIndexedInstancedIndirect




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur les 9. * ou 10. * niveau de fonctionnalité. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdrawinstanced"></a>ID3D11DeviceContext ::D rawInstanced




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdrawinstancedindirect"></a>ID3D11DeviceContext ::D rawInstancedIndirect




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur les 9. * ou 10. * niveau de fonctionnalité. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetconstantbuffers"></a>ID3D11DeviceContext ::D SSetConstantBuffers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur les 9. * ou 10. * niveau de fonctionnalité. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetsamplers"></a>ID3D11DeviceContext ::D SSetSamplers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur les 9. * ou 10. * niveau de fonctionnalité. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetshader"></a>ID3D11DeviceContext ::D SSetShader




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur les 9. * ou 10. * niveau de fonctionnalité. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetshaderresources"></a>ID3D11DeviceContext ::D SSetShaderResources




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur les 9. * ou 10. * niveau de fonctionnalité. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextgssetconstantbuffers"></a>ID3D11DeviceContext :: GSSetConstantBuffers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetsamplers"></a>ID3D11DeviceContext :: GSSetSamplers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetshader"></a>ID3D11DeviceContext :: GSSetShader




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetshaderresources"></a>ID3D11DeviceContext :: GSSetShaderResources




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontexthssetconstantbuffers"></a>ID3D11DeviceContext :: HSSetConstantBuffers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur les 9. * ou 10. * niveau de fonctionnalité. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetsamplers"></a>ID3D11DeviceContext :: HSSetSamplers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur les 9. * ou 10. * niveau de fonctionnalité. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetshader"></a>ID3D11DeviceContext :: HSSetShader




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur les 9. * ou 10. * niveau de fonctionnalité. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetshaderresources"></a>ID3D11DeviceContext :: HSSetShaderResources




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur les 9. * ou 10. * niveau de fonctionnalité. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextiasetindexbuffer"></a>ID3D11DeviceContext::IASetIndexBuffer




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Le format peut être différent de celui spécifié lors de la création de la mémoire tampon, mais une traduction coûteuse sera encourue.<br /> Autorise uniquement les mémoires tampons d’index avec le format DXGI_FORMAT_R16_UINT. <br /> | 
| D3D_FEATURE_LEVEL_9_2 |  Le format peut être différent de celui spécifié lors de la création de la mémoire tampon, mais une traduction coûteuse sera encourue.<br /> Permet aux mémoires tampons d’index avec les formats DXGI_FORMAT_R16_UINT et DXGI_FORMAT_R32_UINT comme D3D_FEATURE_LEVEL_10_0 et versions ultérieures. <br /> $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextiasetprimitivetopology"></a>ID3D11DeviceContext :: IASetPrimitiveTopology




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Les topologies de primitives avec contiguïté ne sont pas prises en charge $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextomsetblendstate"></a>ID3D11DeviceContext :: OMSetBlendState




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | SampleMask ne peut pas être égal à zéro $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextomsetrendertargets"></a>ID3D11DeviceContext :: OMSetRenderTargets




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Une seule cible de rendu prise en charge $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Seules quatre cibles de rendu sont prises en charge, et toutes les ressources liées doivent avoir la même profondeur de bits. | 




 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a>ID3D11DeviceContext :: OMSetRenderTargetsAndUnorderedAccessViews




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetconstantbuffers"></a>ID3D11DeviceContext ::P SSetConstantBuffers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Consultez le niveau de fonctionnalité 10,0, mais le nombre total de constantes utilisées par le nuanceur ne peut pas dépasser 32 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetsamplers"></a>ID3D11DeviceContext ::P SSetSamplers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Vous ne pouvez pas lier plus de 16 échantillonneurs $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetshader"></a>ID3D11DeviceContext ::P SSetShader




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Uniquement ps_4_0_level_9_1 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Ps_4_0_level_9_3 ou ps_4_0_level_9_1 uniquement | 




 

## <a name="id3d11devicecontextpssetshaderresources"></a>ID3D11DeviceContext ::P SSetShaderResources




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Pas plus de 8 ressources de nuanceur liées simultanément $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextrssetscissorrects"></a>ID3D11DeviceContext :: RSSetScissorRects




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Seul le rectangle avant toute chose ciseaux est disponible $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextrssetviewports"></a>ID3D11DeviceContext :: RSSetViewports




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Seule la fenêtre d’affichage avant toute chose est disponible $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

Même si vous spécifiez des valeurs float pour les membres de la structure de la [**\_ fenêtre d’affichage d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) pour le tableau *pViewports* dans un appel à [**ID3D11DeviceContext :: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) pour les [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, **RSSetViewports** utilise des DWORD en interne. En raison de ce comportement, lorsque vous utilisez un coin supérieur gauche négatif pour la fenêtre d’affichage, l’appel à **RSSetViewports** pour les niveaux de fonctionnalité 9 \_ x échoue. Cet échec se produit parce que **RSSetViewports** pour 9 \_ x convertit les valeurs à virgule flottante en entiers non signés sans validation, ce qui entraîne un dépassement sur les entiers.

L’appel à [**ID3D11DeviceContext :: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) pour les [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ x et 11 \_ x fonctionne comme prévu, même quand vous utilisez un coin supérieur gauche négatif pour la fenêtre d’affichage.

## <a name="id3d11devicecontextsetpredication"></a>ID3D11DeviceContext :: SetPredication




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextsosettargets"></a>ID3D11DeviceContext :: SOSetTargets




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetconstantbuffers"></a>ID3D11DeviceContext :: VSSetConstantBuffers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Consultez le niveau de fonctionnalité 10,0, mais le nombre total de constantes utilisées par le nuanceur ne peut pas dépasser 255 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetsamplers"></a>ID3D11DeviceContext :: VSSetSamplers




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetshader"></a>ID3D11DeviceContext :: VSSetShader




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Uniquement vs_4_0_level_9_1 $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Vs_4_0_level_9_3 ou vs_4_0_level_9_1 uniquement | 




 

## <a name="id3d11devicecontextvssetshaderresources"></a>ID3D11DeviceContext :: VSSetShaderResources




| Niveau de fonctionnalité | Différences de comportement | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non pris en charge sur un niveau de fonctionnalité 9. *. $ {REMOVE} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





