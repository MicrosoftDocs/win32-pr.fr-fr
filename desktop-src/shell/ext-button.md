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
ms.openlocfilehash: f902c7f812ecd02716c6981f21f3c1e2171fcba46979b518eb566cdf54775754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050429"
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

## <a name="requirements"></a>Configuration requise



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

 

 




