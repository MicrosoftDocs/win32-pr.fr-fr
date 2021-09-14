---
description: Appelé par un nuanceur d’intersection pour signaler une intersection de rayon.
ms.assetid: ''
title: Fonction ReportHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012891"
---
# <a name="reporthit-function"></a>Fonction ReportHit

Appelé par un [nuanceur d’intersection](intersection-shader.md) pour signaler une intersection de rayon.

## <a name="syntax"></a>Syntaxe
Cette définition de fonction intrinsèque est équivalente au modèle de fonction suivant :

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a>Paramètres

`THit`

Valeur float spécifiant la distance paramétrique de l’intersection.

`HitKind`

Entier non signé qui identifie le type d’accès qui s’est produit.  Il s’agit d’une valeur spécifiée par l’utilisateur dans la plage 0-127.  La valeur peut être lue par [n’importe quel](any-hit-shader.md) nuanceur de correspondance ou d' [accès le plus proche](closest-hit-shader.md) avec l’intrinsèque **HitKind** .

`Attributes`

Structure de structure d' [**attribut d’intersection**](intersection-attributes.md) définie par l’utilisateur qui spécifie les attributs d’intersection.  

## <a name="return-value"></a>Valeur renvoyée

valeur **booléenne** True si l’accès a été accepté.  Un accès est rejeté si *cela* est en dehors de l’intervalle de rayon actuel, ou si le nuanceur de correspondance n’appelle [**IgnoreHit**](ignorehit-function.md).  L’intervalle de rayon actuel est défini par **RayTMin** et **RayTCurrent**.

## <a name="remarks"></a>Notes

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Nuanceur d’intersection**](intersection-shader.md)





## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




