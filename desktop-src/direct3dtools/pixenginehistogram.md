---
description: Représente un histogramme d’une texture.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineHistogram, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FC720568-6C8E-4B14-BCB1-5FA14D32C785
api_name:
- PixEngineHistogram
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: afa9de8ecb598c76daee56367cc9f3ee80a0d0a43f706d11d2eaaa33cd814f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282308"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span id="vspixengine.pixenginehistogram"></span>PixEngineHistogram, structure

Représente un histogramme d’une texture.

## <a name="syntax"></a>Syntaxe


```C++
} PixEngineHistogram;
```

## <a name="members"></a>Membres

**horizontalMin**  
Valeurs minimales pour chacun des composants X, Y, Z et W dans l’axe horizontal (domaine) de l’histogramme.

**horizontalMax**  
Valeurs maximales pour chacun des composants X, Y, Z et W dans l’axe horizontal (domaine) de l’histogramme.

**verticalMin**  
Valeurs minimales pour chacun des composants X, Y, Z et W dans l’axe vertical (plage) de l’histogramme.

**verticalMax**  
Valeurs maximales pour chacun des composants X, Y, Z et W dans l’axe vertical (plage) de l’histogramme.

**dataLength**  
Nombre d’échantillons pris en compte dans l’histogramme.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



