---
title: D1114 pointeur NULL non facultatif
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: 'Le paramètre de l’interface :: Method n’est pas facultatif. Un pointeur NULL a été passé. Cela entraîne le blocage de Direct2D.'
keywords:
- D1114 pointeur facultatif non-valeur NULL
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fa5213eabfb4b22b9a37927495f5058cbfeb0b86b0f1f8b8f3a4ba1a2a2bdbb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666208"
---
# <a name="d1114-non-optional-pointer-null"></a>D1114 : pointeur NULL non facultatif

Le \[ *paramètre* \] de paramètre pour *interface*::*Method* n’est pas facultatif. Un pointeur **null** a été passé. Cela entraîne le blocage de Direct2D.

### <a name="placeholders"></a>Espaces réservés

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*paramètre*
</dt> <dd>

Nom du paramètre qui contient le pointeur **null** .

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

Nom de l’interface à laquelle la *méthode* appartient.

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*méthode*
</dt> <dd>

Nom de la méthode qui a reçu le paramètre non valide.

</dd> </dl> 




 

### <a name="examples"></a>Exemples

L’exemple suivant montre que la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) reçoit un pointeur null pour le paramètre *Geometry* non facultatif.


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



Cet exemple génère le message de débogage suivant :

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a>Causes possibles

Un pointeur NULL a été passé pour un paramètre non facultatif.

## <a name="fixes"></a>Correctifs

Assurez-vous qu’un paramètre non facultatif n’a pas de pointeur NULL.

 

 
