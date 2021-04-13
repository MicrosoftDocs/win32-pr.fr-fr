---
description: Ajoute un objet de données en tant qu’enfant du nœud de données du fichier ID3DXFileSaveData.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'ID3DXFileSaveData :: AddDataObject, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b097e63792b32bc1688ce93c8ce32ffaedeae6ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323065"
---
# <a name="id3dxfilesavedataadddataobject-method"></a>ID3DXFileSaveData :: AddDataObject, méthode

Ajoute un objet de données en tant qu’enfant du nœud de données du fichier [**ID3DXFileSaveData**](id3dxfilesavedata.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rguidTemplate* \[ dans\]
</dt> <dd>

Type : **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

GUID représentant le modèle de l’objet de données.

</dd> <dt>

*szName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers le nom de l’objet de données à ajouter. Spécifiez **null** si l’objet n’a pas de nom.

</dd> <dt>

*PID* \[ dans\]
</dt> <dd>

Type : **const [**GUID**](guid.md) \***

Pointeur vers un GUID représentant l’objet de données. L’objet de données doit avoir été enregistré avec [**ID3DXFile :: RegisterTemplates**](id3dxfile--registertemplates.md) ou [**ID3DXFile :: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md). Spécifiez **null** si l’objet n’a pas de GUID.

</dd> <dt>

*cbSize* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**

Taille de l’objet de données, en octets.

</dd> <dt>

*pvData* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers une mémoire tampon contenant toutes les données requises dans l’objet de données.

</dd> <dt>

*ppObj* \[ dans, retval\]
</dt> <dd>

Type : **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***

Adresse d’un pointeur vers une interface [**ID3DXFileSaveData**](id3dxfilesavedata.md) , représentant le nœud de données de fichier auquel l’objet de données sera ajouté.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
