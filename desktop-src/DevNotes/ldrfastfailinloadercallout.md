---
description: Cette fonction termine de force le programme appelant s’il est appelé à l’intérieur d’un appel de chargeur. Dans le cas contraire, elle n’a aucun effet.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: LdrFastFailInLoaderCallout fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528619"
---
# <a name="ldrfastfailinloadercallout-function"></a>LdrFastFailInLoaderCallout fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Cette fonction termine de force le programme appelant s’il est appelé à l’intérieur d’un appel de chargeur. Dans le cas contraire, elle n’a aucun effet.

## <a name="syntax"></a>Syntaxe


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette routine n’intercepte pas tous les cas de blocage potentiels ; Il est possible pour un thread à l’intérieur d’une légende de chargeur d’acquérir un verrou tandis qu’un thread en dehors d’un appel de chargeur détient le même verrou et effectue un appel dans le chargeur. En d’autres termes, il peut y avoir une inversion d’ordre de verrou entre le verrou du chargeur et un verrou client.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>NTDll. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>NTDll.dll</dt> </dl> |



 

 




