---
description: 'Permet à l’objet de rappel de spécifier un fichier d’aide HTML et une rubrique qu’il contient. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_GETHELPTOPIC (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c60749b69df30e89c3ffda7a8664b901ee57f9ff0cb586f13d61abd9ca66997e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968708"
---
# <a name="sfvm_gethelptopic-message"></a>\_Message SFVM GETHELPTOPIC

Permet à l’objet de rappel de spécifier un fichier d’aide HTML et une rubrique qu’il contient. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phtd* \[ à\]
</dt> <dd>

Adresse d’une structure [**de \_ \_ données SFVM HELPTOPIC**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) qui spécifie le fichier d’aide HTML et la rubrique.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
