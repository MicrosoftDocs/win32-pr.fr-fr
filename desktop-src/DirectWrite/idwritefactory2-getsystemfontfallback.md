---
title: Méthode IDWriteFactory2 GetSystemFontFallback
description: Crée un objet de police de secours à partir de la liste des polices système de secours.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Écriture directe de la méthode GetSystemFontFallback
- Méthode GetSystemFontFallback Write directe, interface IDWriteFactory2
- Écriture directe de l’interface IDWriteFactory2, méthode GetSystemFontFallback
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4513c8ee7fb4e7a3796ec442d4d36bb663a0c8803bb6276a584edcfda306d588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329443"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a>IDWriteFactory2 :: GetSystemFontFallback, méthode

Crée un objet de police de secours à partir de la liste des polices système de secours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fontFallback* \[ à\]
</dt> <dd>

Type : **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***

Contient une adresse d’un pointeur vers l’objet de police de secours nouvellement créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

 