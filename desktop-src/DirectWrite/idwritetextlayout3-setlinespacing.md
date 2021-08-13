---
title: Méthode IDWriteTextLayout3 SetLineSpacing
description: Définissez l’interligne. | Méthode IDWriteTextLayout3 SetLineSpacing
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Écriture directe de la méthode SetLineSpacing
- Méthode SetLineSpacing Write directe, interface IDWriteTextLayout3
- Écriture directe de l’interface IDWriteTextLayout3, méthode SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1c054fd63beb85303a7d163a16b55f07613b687085be53e22d814b0003c63c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649377"
---
# <a name="idwritetextlayout3setlinespacing-method"></a>IDWriteTextLayout3 :: SetLineSpacing, méthode

Définissez l’interligne.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lineSpacingOptions* \[ dans\]
</dt> <dd>

Comment gérer l’espace entre les lignes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                 |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





