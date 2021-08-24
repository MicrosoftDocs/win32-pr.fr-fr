---
description: Sélectionne une carte réseau de registre.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: GetNPPBlobFromUI, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d3b88c369145d53d32d23773072f878d9834110e705cd8ff623a3726cbb98b88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743879"
---
# <a name="getnppblobfromui-function"></a>GetNPPBlobFromUI fonction)

La fonction **GetNPPBlobFromUI** sélectionne une carte réseau de registre.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle d’une fenêtre qui affiche la boîte de dialogue **Sélectionner un réseau** .

</dd> <dt>

*hFilterBlob* \[ dans\]
</dt> <dd>

Handle d’un [*objet blob de filtre*](f.md) utilisé pour limiter les cartes réseau affichées.

</dd> <dt>

*phBlob* \[ à\]
</dt> <dd>

Pointeur vers le handle de l’objet BLOB qui représente la carte réseau sélectionnée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit (l’utilisateur sélectionne une carte réseau), la valeur de retour est NMERR \_ Success et l’objet BLOB vers lequel pointe *phBlob* est renseigné.

Si l’utilisateur ne sélectionne pas une carte réseau, la valeur de retour est **NMERR \_ aucun \_ NPP \_** n’est sélectionné.

Si la fonction échoue, la valeur de retour est une autre valeur NMERR.

## <a name="remarks"></a>Remarques

Quand elle est appelée, Moniteur réseau affiche la boîte de dialogue **Sélectionner un réseau** , que vous pouvez utiliser pour sélectionner une carte réseau. L’objet BLOB NPP qui représente la carte réseau est renvoyé à l’application appelante.

Si l’objet BLOB nommé par *hFilterBlob* est un [*objet BLOB spécial*](s.md), le Finder tente de le traiter. Par exemple, un appel qui avait précédemment retourné un objet BLOB spécial à partir du NPP distant. L’application a inséré la balise requise, le nom de l’ordinateur \_ . Dans ce cas, le Finder transmet cet objet BLOB au NPP distant, qui retourne ensuite une table d’objets BLOB NPP représentant l’ordinateur demandé. Ces objets BLOB NPP distants s’affichent dans la boîte de dialogue.

L’appelant doit appeler la fonction [DestroyBlob](destroyblob.md) , qui détruit l’objet BLOB retourné lorsqu’il n’est plus nécessaire.



| Pour plus d’informations sur l’un des sujets suivants : | Consultez                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| Trois façons de sélectionner des cartes réseau  | [Sélection d’une carte d’interface réseau](selecting-a-network-interface-card.md) |
| Spécification d’un objet BLOB de filtre   | [Spécification d’un objet BLOB de filtre](specifying-a-filter-blob.md)                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[SelectNPPBlobFromTable](selectnppblobfromtable.md)
</dt> </dl>

 

 




