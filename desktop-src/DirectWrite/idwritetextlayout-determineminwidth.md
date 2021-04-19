---
title: Méthode IDWriteTextLayout DetermineMinWidth
description: Détermine la largeur minimale possible pour laquelle la disposition peut être définie sans rupture d’urgence entre les caractères de mots entiers se produisant.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Écriture directe de la méthode DetermineMinWidth
- Méthode DetermineMinWidth Write directe, interface IDWriteTextLayout
- Écriture directe de l’interface IDWriteTextLayout, méthode DetermineMinWidth
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534783"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a>IDWriteTextLayout ::D méthode etermineMinWidth

Détermine la largeur minimale possible pour laquelle la disposition peut être définie sans rupture d’urgence entre les caractères de mots entiers se produisant.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*minWidth* \[ à\]
</dt> <dd>

Type : **float \***

Largeur minimale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

