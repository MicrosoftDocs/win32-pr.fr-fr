---
title: Méthode MoveNext IDWriteColorGlyphRunEnumerator
description: Passe au glyphe suivant exécuté dans l’énumérateur.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- Écriture directe de la méthode MoveNext
- Méthode MoveNext Write directe, interface IDWriteColorGlyphRunEnumerator
- Écriture directe de l’interface IDWriteColorGlyphRunEnumerator, méthode MoveNext
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416943"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a>IDWriteColorGlyphRunEnumerator :: MoveNext, méthode

Passe au glyphe suivant exécuté dans l’énumérateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*haveRun* \[ à\]
</dt> <dd>

Type : **bool \***

Retourne la **valeur true** s’il y a une exécution de glyphe suivante.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





