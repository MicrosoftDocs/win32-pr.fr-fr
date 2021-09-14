---
title: Méthode IDWriteLocalFontFileLoader GetFilePathFromKey
description: Obtient le chemin d’accès absolu au fichier de polices à partir de la clé de référence du fichier de police.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Écriture directe de la méthode GetFilePathFromKey
- Méthode GetFilePathFromKey Write directe, interface IDWriteLocalFontFileLoader
- Écriture directe de l’interface IDWriteLocalFontFileLoader, méthode GetFilePathFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119818"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a>IDWriteLocalFontFileLoader :: GetFilePathFromKey, méthode

Obtient le chemin d’accès absolu au fichier de polices à partir de la clé de référence du fichier de police.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
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

*filePath* \[ à\]
</dt> <dd>

Type : **WCHAR \***

Tableau de caractères qui reçoit le chemin d’accès au fichier local.

</dd> <dt>

*filePathSize* 
</dt> <dd>

Type : **UInt32**

Longueur du tableau de caractères de chemin d’accès de fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





