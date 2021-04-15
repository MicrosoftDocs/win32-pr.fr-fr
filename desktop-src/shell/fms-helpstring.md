---
description: Contient des informations utilisées par le gestionnaire de fichiers pour ajouter une chaîne d’aide pour un élément de commande de menu ou de barre d’outils.
title: Structure FMS_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: c934409712ae740797eb3b5af0b55c50ff125342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991593"
---
# <a name="fms_helpstring-structure"></a>Structure de FMS \_ HELPSTRING

Contient des informations utilisées par le gestionnaire de fichiers pour ajouter une chaîne d’aide pour un élément de commande de menu ou de barre d’outils.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a>Membres

<dl> <dt>

**idCommand**
</dt> <dd>

Type : **int**

</dd> <dd>

Identificateur de l’élément de commande.

</dd> <dt>

**hMenu**
</dt> <dd>

Type : **HMENU**

</dd> <dd>

Identificateur de la barre de menus.

</dd> <dt>

**szHelp**
</dt> <dd>

Type : **\_ \_ WCHAR \_ t \[ 128 \]**

</dd> <dd>

Chaîne terminée par le caractère null qui reçoit le texte d’aide.

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
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




