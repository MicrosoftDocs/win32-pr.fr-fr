---
description: 'Permet à l’objet de rappel de spécifier qu’une animation doit être affichée pendant que les éléments sont énumérés sur un thread d’arrière-plan. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: Message SFVM_GETANIMATION (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115834"
---
# <a name="sfvm_getanimation-message"></a>\_Message SFVM GETANIMATION

Permet à l’objet de rappel de spécifier qu’une animation doit être affichée pendant que les éléments sont énumérés sur un thread d’arrière-plan. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phinst* \[ à\]
</dt> <dd>

Handle d’instance du module à partir duquel la ressource doit être chargée.

</dd> <dt>

*pwszName* \[ à\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le chemin d’accès du fichier. avi ou le nom d’une ressource AVI. Ce paramètre peut également être constitué de l’identificateur de ressource dans le mot de poids faible et de 0 dans le mot de poids fort. Pour créer cette valeur, utilisez la macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) . Le contrôle charge la ressource à partir du module spécifié par hinst. Une ressource AVI doit avoir le type « AVI ».

</dd> </dl>

## <a name="remarks"></a>Notes

Par défaut, l’objet de vue du dossier système affiche l’animation « torche » pendant une énumération en arrière-plan.

*phinst* et *pwszName* sont passés au contrôle d' [animation](../controls/animation-control-overview.md) avec un message [**ACM \_ ouvert**](../controls/acm-open.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
