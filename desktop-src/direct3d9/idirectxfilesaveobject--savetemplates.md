---
description: Enregistre les modèles dans un fichier DirectX. Action déconseillée.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'IDirectXFileSaveObject :: SaveTemplates, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 87ec95932b26877354c22089a97b249bd542aa841552c3e3f9e4827a20f6d608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292220"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a>IDirectXFileSaveObject :: SaveTemplates, méthode

Enregistre les modèles dans un fichier DirectX. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cTemplates* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre total de modèles à enregistrer.

</dd> <dt>

*ppguidTemplates* \[ dans\]
</dt> <dd>

Type : **const [**GUID**](guid.md) \* \***

Adresse d’un pointeur vers un tableau de GUID pour tous les modèles à enregistrer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Notes

Le fragment de code suivant fournit un exemple d’appel à **IDirectXFileSaveObject :: SaveTemplates** et un exemple de contenu pour le tableau auquel ppguidTemplates pointe.


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



Après avoir utilisé cette méthode pour enregistrer les modèles, utilisez la méthode [**IDirectXFileSaveObject :: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) pour créer un objet de données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
