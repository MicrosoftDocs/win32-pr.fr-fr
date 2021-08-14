---
title: Structure MENUEX_TEMPLATE_ITEM
description: Définit un élément de menu dans un modèle de menu étendu. Cette définition de structure est destinée uniquement à des fins d’explication. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM des menus de structure et d’autres ressources
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6352c7ce596a59d69b21f1ba424ac50b471e13cd97320f0df184bce2e1abd295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733904"
---
# <a name="menuex_template_item-structure"></a>Structure d’élément de \_ modèle menuex \_

Définit un élément de menu dans un modèle de menu étendu. Cette définition de structure est destinée uniquement à des fins d’explication. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a>Membres

<dl> <dt>

**dwType**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Type d’élément de menu. Ce membre peut être une combinaison des valeurs de type (commençant par MFT) listées avec la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

</dd> <dt>

**dwState**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

État de l’élément de menu. Ce membre peut être une combinaison de l’État (à partir de MFS) et de la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

</dd> <dt>

**Codé**
</dt> <dd>

Type : **uint**

</dd> <dd>

Identificateur de l’élément de menu. Il s’agit d’une valeur définie par l’application qui identifie l’élément de menu. Dans une ressource de menu étendue, les éléments qui ouvrent des menus déroulants ou des sous-menus et des éléments de commande peuvent avoir des identificateurs.

</dd> <dt>

**wFlags**
</dt> <dd>

Type : **Word**

</dd> <dd>

Spécifie si l’élément de menu est le dernier élément dans la barre de menus, le menu déroulant, le sous-menu ou le menu contextuel et s’il s’agit d’un élément qui ouvre un menu déroulant ou un sous-menu. Ce membre peut être égal à zéro ou plusieurs de ces valeurs. Pour les applications 32 bits, ce membre est un mot ; pour les applications 16 bits, il s’agit d’un octet.

<dt>

0x80
</dt> <dd>

La structure définit le dernier élément de menu dans la barre de menus, le menu déroulant, le sous-menu ou le menu contextuel.

</dd> <dt>

0x01
</dt> <dd>

La structure définit un élément qui ouvre un menu déroulant ou un sous-menu. Les structures suivantes définissent les éléments de menu dans le menu déroulant ou le sous-menu correspondant.

</dd> </dl> </dd> <dt>

**szText**
</dt> <dd>

Type : **WCHAR**

</dd> <dd>

Texte de l’élément de menu. Ce membre est une chaîne Unicode terminée par le caractère null, alignée sur une limite de mot. La taille de la définition d’élément de menu varie en fonction de la longueur de cette chaîne.

</dd> </dl>

## <a name="remarks"></a>Remarques

Un modèle de menu étendu se compose d’une structure d' [**\_ \_ en-tête de modèle menuex**](menuex-template-header.md) suivie d’une ou de plusieurs structures d' **\_ \_ élément de modèle menuex** contiguës. Les structures d' **\_ \_ élément de modèle menuex** , qui sont de longueur variable, sont alignées sur les limites **DWORD** . Pour créer un menu à partir d’un modèle de menu étendu en mémoire, utilisez la fonction [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .

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

[**\_ \_ en-tête de modèle menuex**](menuex-template-header.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

 





