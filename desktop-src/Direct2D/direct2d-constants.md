---
title: Constantes Direct2D
description: Direct2D définit la liste suivante de constantes.
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: cd8adfa3d6fa3c59a05331c82ea12100918a4697d9478097a890eedff039d5e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768729"
---
# <a name="direct2d-constants"></a>Constantes Direct2D

Les constantes suivantes sont déclarées dans `d2d1effectauthor.h` les `d2d1.h` `d2d1_1.h` fichiers d' `d2d1effects_2.h` en-tête,, et.

## <a name="d2d1_append_aligned_element--1"></a>D2D1_APPEND_ALIGNED_ELEMENT (-1)
Utilisé lors de la compression d’éléments de disposition d’entrée. Elle indique que les éléments doivent être empaquetés de façon contiguë.

## <a name="d2d1_default_flattening_tolerance-025f"></a>D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25 f)
Tolérance par défaut pour les opérations de mise à plat géométrique.

## <a name="d2d1_invalid_property_index-uint_max"></a>D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)
Définit un index de propriété non valide.

Cette constante est retournée à partir de [**ID2D1Properties :: GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) pour indiquer que la propriété nommée que vous avez fournie n’a pas d’index dans l’interface de propriété.

Si vous transmettez cette constante à [**ID2D1Properties :: GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) ou [**ID2D1Properties :: GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), l’appel échoue et la mémoire tampon de sortie est remplie de zéros.

## <a name="d2d1_invalid_tag-ulonglong_max"></a>D2D1_INVALID_TAG (ULONGLONG_MAX)
Réservé n’utilisez pas.

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a>D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80,0 f)
Nombre de nits utilisés par l’espace de couleurs sRVB ou ScRVB pour les valeurs de virgule flottante ou de virgule flottante de 1,0 f. Cette valeur est constante uniquement lorsque l’espace colorimétrique utilise la luminance référencée par scène, ce qui est vrai pour le contenu HDR (High dynamique Range). Si l’espace colorimétrique utilise à la place la luminance référencée, le niveau de blanc SDR doit être interrogé à partir de l’affichage.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge | Windows 7, Windows vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ desktop apps \|\] |
| Serveur minimal pris en charge | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[ desktop apps \|\] |
| Téléphone minimal pris en charge | Windows Phone 8,1 \[ Windows Phone silverlight 8,1 et les applications Windows Runtime \] , Windows Phone 8,1 \[ Windows Phone silverlight 8,1 et Windows Runtime apps\] |
| En-tête | d2d1effectauthor. h, d2d1. h, d2d1_1. h, d2d1effects_2. h |
