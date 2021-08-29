---
title: Le type de la ressource D1106 est incorrect
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: La ressource donnée n’est pas d’un type attendu.
keywords:
- Le type de ressource D1106 est incorrect.
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1bbfd6d58eeb155002fbf5e7dbe243bd8d942ddaf4fa7d7715c6211523015476
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911189"
---
# <a name="d1106-resource-is-wrong-type"></a>D1106 : type de ressource incorrect

La \[ *ressource* \] de ressource donnée n’est pas d’un type attendu.

## <a name="placeholders"></a>Espaces réservés

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*ressource*
</dt> <dd>

Adresse de la ressource.

</dd> </dl> 




 

## <a name="possible-causes"></a>Causes possibles

Une interface a été incorrectement castée et utilisée comme paramètre pour une méthode ou une fonction.

## <a name="examples"></a>Exemples

L’exemple suivant passe un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) lorsqu’un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) est attendu.


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



Cet exemple génère le message de débogage suivant :

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a>Correctifs

Utilisez le type requis par la méthode.

 

 
