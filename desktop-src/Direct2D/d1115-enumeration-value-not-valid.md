---
title: Valeur d’énumération D1115 non valide
description: Valeur d’énumération D1115 non valide
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- Valeur d’énumération D1115 non valide Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "106533525"
---
# <a name="d1115-enumeration-value-not-valid"></a>D1115 : valeur d’énumération non valide

Le paramètre de paramètre avec la valeur \[  \] \[  \] de valeur pour *interface*::*Method* n’est pas une valeur d’énumération valide.

## <a name="placeholders"></a>Espaces réservés

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*paramètre*
</dt> <dd>

Nom du paramètre qui a reçu le type inattendu.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*ajoutée*
</dt> <dd>

Valeur d’énumération non valide.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

Nom de l’interface à laquelle la *méthode* appartient.

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*méthode*
</dt> <dd>

Nom de la méthode qui a reçu la valeur d’énumération non valide.

</dd> </dl> 




 

## <a name="examples"></a>Exemples

L’exemple suivant spécifie une valeur d’énumération de [**\_ \_ \_ type cible de rendu d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) de 30, qui est en dehors de la plage attendue.


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



Cet exemple génère le message de débogage suivant :

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a>Causes possibles

Un paramètre A utilisé une valeur d’énumération non valide.

## <a name="fixes"></a>Correctifs

Utilisez une valeur d’énumération valide.

> [!Note]  
> La couche de débogage vérifie actuellement uniquement les valeurs d’énumération individuelles ; elle ne vérifie pas si une combinaison au niveau du bit est valide.

 

 

 
