---
title: Méthode IDWriteLocalFontFileLoader GetFilePathLengthFromKey
description: Obtient la longueur du chemin d’accès absolu du fichier à partir de la clé de référence du fichier de police.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Écriture directe de la méthode GetFilePathLengthFromKey
- Méthode GetFilePathLengthFromKey Write directe, interface IDWriteLocalFontFileLoader
- Écriture directe de l’interface IDWriteLocalFontFileLoader, méthode GetFilePathLengthFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119817"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a>IDWriteLocalFontFileLoader :: GetFilePathLengthFromKey, méthode

Obtient la longueur du chemin d’accès absolu du fichier à partir de la clé de référence du fichier de police.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
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

Taille de la clé de référence du fichier de police en octets.

</dd> <dt>

*filePathLength* \[ à\]
</dt> <dd>

Type : **UInt32 \***

Longueur de la chaîne du chemin d’accès du fichier, sans inclure le caractère **null** terminé.

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

 

 





