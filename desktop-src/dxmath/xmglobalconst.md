---
description: Déclare un objet comme constante de sélection, afin d’éviter les rechargements redondants de cet objet s’il est utilisé (et déclaré) à plusieurs emplacements dans la bibliothèque DirectXMath.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: XMGLOBALCONST macro)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529731"
---
# <a name="xmglobalconst-macro"></a>XMGLOBALCONST macro)

Déclare un objet comme constante de *sélection* , afin d’éviter les rechargements redondants de cet objet s’il est utilisé (et déclaré) à plusieurs emplacements dans la bibliothèque DirectXMath.

## <a name="syntax"></a>Syntaxe

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a>Notes

L’utilisation de XMGLOBALCONST permet de spécifier des constantes globales. Cela permet de réduire la taille du segment de données d’une application, d’éviter la création et la destruction d’objets redondants, et de réduire les opérations de chargement et de stockage.

## <a name="requirements"></a>Configuration requise

**En-tête :** Déclaré dans DirectXMath. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Macros de la bibliothèque DirectXMath](ovw-xnamath-reference-macros.md)
</dt> <dt>

[Constantes globales dans la bibliothèque DirectXMath](pg-xnamath-internals.md)
</dt> <dt>

[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))
</dt> <dt>

[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))
</dt> </dl>

 

 
