---
description: Récupère un énumérateur qui retourne un pointeur vers une liste d’identificateurs d’élément (PIDL) pour chaque vue étendue.
title: 'IShellFolderViewType :: EnumViews, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 4ccaac7baf99608e097b8f8b67c8eac30f60ed3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991136"
---
# <a name="ishellfolderviewtypeenumviews-method"></a>IShellFolderViewType :: EnumViews, méthode

Récupère un énumérateur qui retourne un pointeur vers une liste d’identificateurs d’élément (PIDL) pour chaque vue étendue.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*grfFlags* \[ dans\]
</dt> <dd>

Type : **ULong**

Indicateurs spécifiant les éléments à inclure dans l’énumération. Pour obtenir la liste des valeurs possibles, consultez le type énuméré [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) . Ce paramètre peut être ignoré.

</dd> <dt>

*ppEnum* \[ à\]
</dt> <dd>

Type : **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***

Adresse d’une variable pointeur de type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) qui reçoit l’énumérateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Les vues sont représentées à l’utilisateur en tant que dossiers masqués dans le répertoire racine (représenté par PIDL). Le cas échéant, l’affichage par défaut (à partir du dossier racine) est représenté sous la forme **null**, ou vide, PIDL.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




