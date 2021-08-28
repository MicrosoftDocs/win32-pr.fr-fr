---
description: La fonction SelectNPPBlobFromTable sélectionne une carte réseau à partir d’une table d’objets BLOB NPP fournie.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: SelectNPPBlobFromTable, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14d9ca14d027efc1540f5a5d2ae78e948da68dd59247252989b617d07229bb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074409"
---
# <a name="selectnppblobfromtable-function"></a>SelectNPPBlobFromTable fonction)

La fonction **SelectNPPBlobFromTable** sélectionne une carte réseau à partir d’une table d’objets BLOB NPP fournie.

## <a name="syntax"></a>Syntaxe


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle vers la fenêtre qui affiche la boîte de dialogue **Sélectionner un réseau** .

</dd> <dt>

*pBlobTable* \[ dans\]
</dt> <dd>

Pointeur vers la table d’objets BLOB fournie. Moniteur réseau utilise ce tableau pour renseigner la boîte de dialogue **Sélectionner un réseau** .

</dd> <dt>

*hBlob* \[ à\]
</dt> <dd>

Handle vers l’objet BLOB qui représente la carte réseau sélectionnée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit et que l’utilisateur sélectionne une carte réseau, la valeur de retour est NMERR \_ Success ; l’objet BLOB vers lequel pointe *hBlob* est renseigné.

Si l’utilisateur ne sélectionne pas une carte réseau, la valeur de retour est NMERR \_ aucun NPP n’est \_ \_ sélectionné.

Si la fonction échoue, la valeur de retour est une autre valeur NMERR.

## <a name="remarks"></a>Remarques

Quand elle est appelée, Moniteur réseau affiche la boîte de dialogue **Sélectionner un réseau** , que vous pouvez utiliser pour sélectionner une carte réseau. L’objet BLOB NPP qui représente la carte réseau sélectionnée retourne à l’application appelante.

Pour connaître les différentes façons de sélectionner des cartes réseau, consultez [sélection d’une carte d’interface réseau](selecting-a-network-interface-card.md) .

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

[GetNPPBlobFromUI](getnppblobfromui.md)
</dt> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[Entrées d’objets BLOB spéciales](special-blob-entries.md)
</dt> </dl>

 

 




