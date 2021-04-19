---
description: Retourne la valeur passée comme paramètre HitKind à ReportHit.
ms.assetid: ''
title: HitKind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529097"
---
# <a name="hitkind"></a>HitKind

Retourne la valeur passée comme paramètre **HitKind** à [**ReportHit**](reporthit-function.md).

## <a name="syntax"></a>Syntaxe

```
uint HitKind();

```



## <a name="remarks"></a>Notes

Si l’intersection a été signalée par une intersection de triangle à fonction fixe, **HitKind** sera l’une des faces **\_ \_ \_ avant \_** du triangle du type d’accès (254) ou le type de point d’accès (255). **\_ \_ \_ \_**

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Tout nuanceur de correspondance**](any-hit-shader.md)
* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur d’intersection**](intersection-shader.md)





## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




