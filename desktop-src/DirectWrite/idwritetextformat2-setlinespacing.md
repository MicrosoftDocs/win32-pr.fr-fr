---
title: Méthode IDWriteTextFormat2 SetLineSpacing
description: Définissez l’interligne. | Méthode IDWriteTextFormat2 SetLineSpacing
ms.assetid: 71d8c6c4-920f-a1b5-5a13-9985a7aca41e
keywords:
- Écriture directe de la méthode SetLineSpacing
- Méthode SetLineSpacing Write directe, interface IDWriteTextFormat2
- Écriture directe de l’interface IDWriteTextFormat2, méthode SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextFormat2.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4298d4671b6f1b9a5a46e4ffdeb450540c2a8eb7f547d1a8dd0f0c0768f54d84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075549"
---
# <a name="idwritetextformat2setlinespacing-method"></a>IDWriteTextFormat2 :: SetLineSpacing, méthode

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

Type : **const [**DWRITE \_ ligne \_ Spacing**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing) \***

Comment gérer l’espace entre les lignes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

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

[**IDWriteTextFormat2**](idwritetextformat2.md)
</dt> </dl>

 

 





