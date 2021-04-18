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
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519211"
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

**void**

## <a name="remarks"></a>Notes

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Nuanceur pouvant être appelé**](callable-shader.md)
* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur manque**](miss-shader.md)
* [**Nuanceur de création de rayon**](ray-generation-shader.md)



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




