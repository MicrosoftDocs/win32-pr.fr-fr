---
description: Appelée à partir d’un nuanceur d’accès quelconque pour rejeter l’accès et terminer le nuanceur.
ms.assetid: ''
title: Fonction IgnoreHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414473"
---
# <a name="ignorehit-function"></a>Fonction IgnoreHit

Appelée à partir d’un [nuanceur d’accès quelconque](any-hit-shader.md) pour rejeter l’accès et terminer le nuanceur. La recherche d’accès se poursuit sans valider la distance et les attributs pour l’accès actuel.  L’appel [**ReportHit**](reporthit-function.md) dans le [nuanceur d’intersection](intersection-shader.md), le cas échéant, retourne la valeur false.  Toutes les modifications apportées à la charge utile de rayon jusqu’à ce point dans le nuanceur d’accès sont conservées.

## <a name="syntax"></a>Syntaxe

```
void IgnoreHit();

```


## <a name="return-value"></a>Valeur de retour

**nullité**

## <a name="remarks"></a>Notes

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Tout nuanceur de correspondance**](any-hit-shader.md)




## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




