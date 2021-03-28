---
description: 'Permet à l’objet de rappel de demander l’énumération sur un thread d’arrière-plan. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_BACKGROUNDENUM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991684"
---
# <a name="sfvm_backgroundenum-message"></a>\_Message SFVM BACKGROUNDENUM

Permet à l’objet de rappel de demander l’énumération sur un thread d’arrière-plan. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a>Paramètres

Ce message n’a pas de paramètres.

## <a name="remarks"></a>Notes

En réponse à cette notification, retournez \_ OK pour activer l’énumération d’arrière-plan. Par défaut, l’objet dossier système affiche l’animation « torche » pendant que l’énumération a lieu. Pour spécifier une animation personnalisée, gérez [**SFVM \_ GETANIMATION**](sfvm-getanimation.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
