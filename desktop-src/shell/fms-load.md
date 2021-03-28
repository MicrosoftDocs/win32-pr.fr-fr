---
description: Contient des informations utilisées par le gestionnaire de fichiers pour ajouter un menu personnalisé fourni par une DLL d’extension du gestionnaire de fichiers. La structure fournit également une valeur delta que la DLL d’extension peut utiliser pour manipuler le menu personnalisé après le chargement du menu par le gestionnaire de fichiers.
title: Structure FMS_LOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: 1745c4e34ac124e9990602350db6479ce287be8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971915"
---
# <a name="fms_load-structure"></a>\_Structure de charge FMS

Contient des informations utilisées par le gestionnaire de fichiers pour ajouter un menu personnalisé fourni par une DLL d’extension du gestionnaire de fichiers. La structure fournit également une valeur delta que la DLL d’extension peut utiliser pour manipuler le menu personnalisé après le chargement du menu par le gestionnaire de fichiers.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwSize nul**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Longueur, en octets, de la structure.

</dd> <dt>

**szMenuName**
</dt> <dd>

Type : **\[ \_ \_ longueur \] du texte du menu TCHAR**

</dd> <dd>

Nom se terminant par un caractère NULL d’un élément de menu qui s’affiche dans la barre de menus du gestionnaire de fichiers.

</dd> <dt>

**hMenu**
</dt> <dd>

Type : **HMENU**

</dd> <dd>

Identificateur du menu contextuel ajouté à la barre de menus dans le gestionnaire de fichiers.

</dd> <dt>

**wMenuDelta**
</dt> <dd>

Type : **uint**

</dd> <dd>

Valeur delta de l’élément de menu. Pour éviter les conflits avec ses propres éléments de menu, le gestionnaire de fichiers renumérote les identificateurs d’élément de menu dans le menu contextuel identifié par le membre **HMENU** en ajoutant cette valeur Delta à chaque identificateur. Une DLL d’extension qui doit modifier un élément de menu doit identifier l’élément en ajoutant la valeur Delta à l’identificateur de l’élément de menu. La valeur de ce membre peut varier de la session à la session.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




