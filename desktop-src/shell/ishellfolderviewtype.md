---
description: Expose des méthodes qui permettent à un dossier de Shell de prendre en charge différentes vues sur son contenu (différentes dispositions hiérarchiques de ses données).
title: Interface IShellFolderViewType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9b597f6b-ef27-4fa1-ad00-e131dbd979e7
ms.openlocfilehash: 1440b6d14950ad70d2c76168b28bb1077b19b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034494"
---
# <a name="ishellfolderviewtype-interface"></a>Interface IShellFolderViewType

Expose des méthodes qui permettent à un dossier de Shell de prendre en charge différentes vues sur son contenu (différentes dispositions hiérarchiques de ses données).

## <a name="members"></a>Membres

L’interface **IShellFolderViewType** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IShellFolderViewType** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IShellFolderViewType** possède ces méthodes.



| Méthode                                                                      | Description                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumViews**](ishellfolderviewtype-enumviews.md)                         | Récupère un énumérateur qui retourne un PIDL pour chaque vue étendue.<br/>                                                                                |
| [**GetDefaultViewName**](ishellfolderviewtype-getdefaultviewname.md)       | Obtient le nom de la vue par défaut. Appelez [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) pour récupérer les noms des autres vues.<br/> |
| [**GetViewTypeProperties**](ishellfolderviewtype-getviewtypeproperties.md) | Obtient les propriétés de la vue.<br/>                                                                                                                          |
| [**TranslateViewPidl**](ishellfolderviewtype-translateviewpidl.md)         | Reconstruit un PIDL à partir d’une représentation hiérarchique du dossier Shell dans une représentation différente.<br/>                                             |



 

## <a name="remarks"></a>Notes

Cet énumérateur retourne des PIDL qui sont des dossiers masqués spéciaux au niveau supérieur du dossier shell, qui ne sont pas énumérés autrement. La vue par défaut est celle qui s’affiche normalement dans le dossier de l’interpréteur de commandes.

Cette interface n’est définie dans aucun fichier d’en-tête public. Si vous choisissez d’implémenter cette interface, vous pouvez utiliser le code C/C++ suivant pour déclarer ses méthodes.


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderViewType Methods _*_

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList _*ppenum) PURE;

    // GetDefaultViewName:
    //   Returns the name of the default view.  The names of the other views
    //   can be retrieved by calling GetDisplayNameOf.
    STDMETHOD(GetDefaultViewName)(THIS_ DWORD  uFlags, __out LPWSTR *ppwszName) PURE;
    STDMETHOD(GetViewTypeProperties)(THIS_ PCUITEMID_CHILD pidl, __out DWORD *pdwFlags)  PURE;

    // TranslateViewPidl:
    //   Attempts to take a pidl represented in one hierarchical representation of
    //   the Shell folder, and find it in a different representation.
    //   pidl should be relative to the root folder.
    //   Remember to ILFree ppidlOut
    STDMETHOD(TranslateViewPidl)(THIS_ PCUIDLIST_RELATIVE pidl, PCUIDLIST_RELATIVE pidlView,
              __out PIDLIST_RELATIVE *ppidlOut) PURE;
};

#define SFVTFLAG_NOTIFY_CREATE  0x00000001
#define SFVTFLAG_NOTIFY_RESORT  0x00000002
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
