---
description: Appelle un autre nuanceur à partir d’un nuanceur.
ms.assetid: ''
title: Fonction CallShader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: e411ef61c34eafcef71f3e68f6700651e4b3073423afd40451f139f02826e504
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119280349"
---
# <a name="callshader-function"></a>Fonction CallShader

Appelle un autre nuanceur à partir d’un nuanceur.

## <a name="syntax"></a>Syntaxe
Cette définition de fonction intrinsèque est équivalente au modèle de fonction suivant :

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a>Paramètres

`ShaderIndex`

Entier non signé représentant l’index dans la table de [nuanceur pouvant être appelé](callable-shader.md) spécifiée dans l’appel à [**DispatchRays**] (/Windows/Desktop/API/d3d12/NF-d3d12-id3d12graphicscommandlist4-dispatchrays.

`Parameter`

Paramètres définis par l’utilisateur à passer au nuanceur pouvant être appelé.  Cette structure de paramètre doit correspondre à la structure de paramètre utilisée dans le nuanceur pouvant être appelé dans la table du nuanceur.


## <a name="return-value"></a>Valeur renvoyée

**nullité**

## <a name="remarks"></a>Remarques

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Nuanceur pouvant être appelé**](callable-shader.md)
* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur manque**](miss-shader.md)
* [**Nuanceur de création de rayon**](ray-generation-shader.md)



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




