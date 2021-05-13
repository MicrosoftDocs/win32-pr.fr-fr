---
description: Convertit ce pointeur vers une liste d’identificateurs d’élément (PIDL) en une partie non valide du dossier shell.
title: 'IShellFolderSearchable :: InvalidateSearch, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 43d76c6a27b301a61474b8028af16e5e540cf2ce
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841690"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a>IShellFolderSearchable :: InvalidateSearch, méthode

Convertit ce pointeur vers une liste d’identificateurs d’élément (PIDL) en une partie non valide du dossier shell.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pidlSearch* \[ dans\]
</dt> <dd>

Type : **LPCITEMIDLIST**

Pointeur vers la structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) pour le dossier de recherche.

</dd> <dt>

*pdwFlags* \[ dans\]
</dt> <dd>

Type : **DWORD \***

Aucun indicateur n’est actuellement défini. Affectez la valeur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Lorsqu’un dossier de recherche est invalidé, il peut effectuer le nettoyage des ressources qu’il a utilisées. La méthode **IShellFolderSearchable :: InvalidateSearch** peut provoquer l’annulation d’une recherche asynchrone et provoquera la libération finale de l’objet d’interface [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




