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
ms.openlocfilehash: a5e5aded87ca197af8774a7b5506e21c958dc564eb0af67396e100877ac53e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094909"
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

Type : **ppidl \***

Au retour, contient l’adresse d’un pointeur vers une liste d’identificateurs d’éléments (PIDL) qui identifie le dossier parent. Le paramètre *LPITEMIDLIST* peut faire référence à un objet à n’importe quel niveau sous le dossier parent dans la hiérarchie d’espaces de noms et peut donc être un pointeur à plusieurs niveaux vers un **PIDL** relatif au dossier parent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

la méthode **ISearchItem :: GetParentFolder** est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.

pour prévisualiser les pièces jointes avec un gestionnaire de protocole tiers sur des ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**ISearchItem**](-search-isearchitem.md) et les api suivantes : les interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)et [**ISearchProtocolUI**](-search-isearchprotocolui.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISearchItem**](-search-isearchitem.md)
</dt> </dl>

 

 
