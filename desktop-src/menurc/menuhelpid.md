---
title: MENUHELPID, structure
description: Contient les données finales écrites dans la \_ ressource de menu RT pour un menu ou un sous-menu si le membre resInfo de la structure POPUPMENUITEM est défini sur MFR \_ Popup.
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Menus de la structure MENUHELPID et autres ressources
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511594"
---
# <a name="menuhelpid-structure"></a>MENUHELPID, structure

Contient les données finales écrites dans la ressource de [**\_ menu RT**](/windows/desktop/menurc/resource-types) pour un menu ou un sous-menu si le membre **ResInfo** de la structure [**POPUPMENUITEM**](popupmenuitem.md) est défini sur **MFR \_ Popup**. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a>Membres

<dl> <dt>

**helpID**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Identificateur utilisé pour identifier le menu lors du traitement [**de \_ l’aide WM**](/windows/desktop/shell/wm-help) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Ressources](resources.md)
</dt> </dl>

 

