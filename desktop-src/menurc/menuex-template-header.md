---
title: Structure MENUEX_TEMPLATE_HEADER
description: Définit l’en-tête d’un modèle de menu étendu. Cette définition de structure est destinée uniquement à des fins d’explication. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER des menus de structure et d’autres ressources
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31e52661e04a036cf7a49791be96af002b801af0e0ed1c4b6ad3ddebf971c2c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226119"
---
# <a name="menuex_template_header-structure"></a>\_Structure d' \_ en-tête de modèle menuex

Définit l’en-tête d’un modèle de menu étendu. Cette définition de structure est destinée uniquement à des fins d’explication. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**wVersion**
</dt> <dd>

Type : **Word**

</dd> <dd>

Numéro de version du modèle. Ce membre doit avoir la 1 pour les modèles de menu étendus.

</dd> <dt>

**wOffset**
</dt> <dd>

Type : **Word**

</dd> <dd>

Offset de la première structure [**d' \_ \_ élément de modèle menuex**](menuex-template-item.md) , par rapport à la fin de ce membre de structure. Si la première définition d’élément suit immédiatement le membre **dwHelpId** , ce membre doit être 4.

</dd> <dt>

**dwHelpId**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Identificateur d’aide de la barre de menus.

</dd> </dl>

## <a name="remarks"></a>Remarques

Un modèle de menu étendu se compose d’une structure d' **\_ \_ en-tête de modèle menuex** suivie d’une ou de plusieurs structures d' [**\_ \_ élément de modèle menuex**](menuex-template-item.md) contiguës. Les structures d' **\_ \_ élément de modèle menuex** , qui sont de longueur variable, sont alignées sur les limites **DWORD** . Pour créer un menu à partir d’un modèle de menu étendu en mémoire, utilisez la fonction [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**\_élément de modèle menuex \_**](menuex-template-item.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

 





