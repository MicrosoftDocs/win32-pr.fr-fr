---
title: Méthode IDWriteLocalFontFileLoader GetLastWriteTimeFromKey
description: Obtient l’heure de la dernière écriture du fichier à partir de la clé de référence du fichier de police.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Écriture directe de la méthode GetLastWriteTimeFromKey
- Méthode GetLastWriteTimeFromKey Write directe, interface IDWriteLocalFontFileLoader
- Écriture directe de l’interface IDWriteLocalFontFileLoader, méthode GetLastWriteTimeFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2fb3d79475a943c3a635b347cfd6dbe41e8b3a8903022bae9089e1d6a9847c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816313"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a>IDWriteLocalFontFileLoader :: GetLastWriteTimeFromKey, méthode

Obtient l’heure de la dernière écriture du fichier à partir de la clé de référence du fichier de police.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fontFileReferenceKey* \[ dans\]
</dt> <dd>

Type : **const void \***

Clé de référence du fichier de police qui identifie de façon unique le fichier de police local dans l’étendue du chargeur de polices utilisé.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Type : **UInt32**

Taille de la clé de référence du fichier de police, en octets.

</dd> <dt>

*LastWriteTime* \[ à\]
</dt> <dd>

Type : **fileTime \***

Heure de la dernière modification du fichier de police.

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

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





