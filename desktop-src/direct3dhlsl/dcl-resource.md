---
title: dcl_resource (SM4-ASM)
description: '\_ressource DCL (SM4-ASM)'
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232518"
---
# <a name="dcl_resource-sm4---asm"></a>\_ressource DCL (SM4-ASM)

Déclare une ressource d’entrée de nuanceur non multiéchantillonnée.



| DCL \_ Resource *TN*, *resourceType*, *ReturnType (s)* |
|-----------------------------------------------------|



 

Déclare une ressource d’entrée de nuanceur à échantillonnages.



| DCL \_ Resource *TN*, *resourceType \[ size \] nn*, *ReturnType (s)* |
|---------------------------------------------------------------|



 



| Élément                                                                                                                                                     | Description                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*<br/>                                                                           | \[dans \] le registre de texture, où *N* est un entier qui désigne le numéro du Registre.<br/>                                                                                                                                                                        |
| <span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*<br/>                                   | \[dans \] tout type d’objet figurant dans la page [texture-objet](dx-graphics-hlsl-to-type.md) .<br/>                                                                                                                                                                     |
| <span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*taille du resourceType \[ \] nn*<br/> | \[dans \] un Texture2D ou un type d’objet Texture2DArray (consultez la page [texture-objet](dx-graphics-hlsl-to-type.md) ); la *taille* est un entier facultatif qui indique le nombre d’éléments dans le tableau ; *Nn* est un entier qui indique le nombre d’échantillonnages.<br/> |
| <span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType (s)*<br/>                               | \[dans \] le type de retour par composant qui est l’un des suivants : UNORM, ronfler, Saint, uint ou float. Le nombre de types de retour peut être égal à 1 (si tous les composants sont du même type), mais peut avoir jusqu’à quatre.<br/>                                          |



 

Une ressource est accessible en HLSL à l’aide de la [charge](dx-graphics-hlsl-to-load.md); une texture non multiéchantillonnée est également accessible à l’aide de l’un des exemples de méthodes d' [objet de texture](dx-graphics-hlsl-to-type.md) HLSL.

Si une ressource est liée à une étape de nuanceur, le format de ressource est validé par rapport au type de retour.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.

## <a name="example"></a>Exemple

Voici un exemple.


```
dcl_resource t3, buffer, UNORM
```



## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





