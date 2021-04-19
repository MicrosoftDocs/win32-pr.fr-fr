---
description: Obtient l’objet ISearchItem si l’URL représente une source de données Shell réelle (également appelée extension d’espace de noms Shell).
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: 'ISearchItem :: GetParentFolder, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4209b319e066d5481c669bcca021684f87532a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517240"
---
# <a name="isearchitemgetparentfolder-method"></a>ISearchItem :: GetParentFolder, méthode

Obtient l’objet [**ISearchItem**](-search-isearchitem.md) si l’URL représente une source de données Shell réelle (également appelée extension d’espace de noms Shell).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IShellFolder* \[ à\]
</dt> <dd>

Type : **ppShellFolder \* \***

Au retour, contient l’adresse d’un pointeur vers le dossier qui contient l’URL actuelle. L' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) est exposée par tous les objets de dossier de l’espace de noms Shell, et ses méthodes sont utilisées pour gérer les dossiers.

</dd> <dt>

*LPITEMIDLIST* \[ à\]
</dt> <dd>

Tapez : **ppidl \** _

Au retour, contient l’adresse d’un pointeur vers une liste d’identificateurs d’éléments (PIDL) qui identifie le dossier parent. Le paramètre _LPITEMIDLIST * peut faire référence à un objet à n’importe quel niveau sous le dossier parent dans la hiérarchie d’espaces de noms, et peut donc être un pointeur à plusieurs niveaux vers un **PIDL** relatif au dossier parent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

La méthode **ISearchItem :: GetParentFolder** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.

Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**ISearchItem**](-search-isearchitem.md) et les API suivantes : les interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)et [**ISearchProtocolUI**](-search-isearchprotocolui.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISearchItem**](-search-isearchitem.md)
</dt> </dl>

 

 
