---
description: Contient des informations sur un bouton que la DLL d’extension du gestionnaire de fichiers ajoute à la barre d’outils du gestionnaire de fichiers.
title: Structure EXT_BUTTON (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 5eabb9f5e958b1e0bd15a6412dfbfa276d23f255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751013"
---
# <a name="ext_button-structure"></a>\_Structure du bouton ext

Contient des informations sur un bouton que la DLL d’extension du gestionnaire de fichiers ajoute à la barre d’outils du gestionnaire de fichiers.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a>Membres

<dl> <dt>

**idCommand**
</dt> <dd>

Type : **Word**

</dd> <dd>

Identificateur de commande pour le bouton.

</dd> <dt>

**idsHelp**
</dt> <dd>

Type : **Word**

</dd> <dd>

Identificateur de la chaîne d’aide pour le bouton.

</dd> <dt>

**fsStyle**
</dt> <dd>

Type : **Word**

</dd> <dd>

Style du bouton.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> <dt>

[**\_TOOLBARLOAD FMS**](fms-toolbarload.md)
</dt> </dl>

 

 




