---
title: sh_mutex, mot clé
description: Le \_ mot clé \ SH mutex \ spécifie que l’objet système est un handle d’un mutex.
keywords:
- sh_mutex mot clé MIDL
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a355eb0121875e186a485ee6f7f96519a4fa0cfb1c75c806e1baea895691c914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641364"
---
# <a name="sh_mutex-keyword"></a>SH \_ (mot clé)

Le mot clé de **\_ mutex SH** spécifie qu’un `system_handle` contient un handle vers un mutex.

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
```

## <a name="parameters"></a>Paramètres

Ce mot clé est un paramètre pour [**system_handle**](system-handle.md).

La documentation [**system_handle**](system-handle.md) contient également des informations sur l’utilisation facultative du paramètre *Access-Rights* . Le comportement par défaut est défini `DUPLICATE_SAME_ACCESS` par les spécifications de [fonction **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

## <a name="remarks"></a>Remarques

Pour pouvoir utiliser ce mot clé avec l' `system_handle` attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.

## <a name="examples"></a>Exemples

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
}
```

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
|-|-|
| Client minimal pris en charge | Windows 10 Mise à jour anniversaire (version 1607, Build 14393) |
| Serveur minimal pris en charge | Windows Server 2016 (build 14393) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Objets mutex](../sync/mutex-objects.md)
</dt> <dt>

[Sécurité de l’objet de synchronisation et droits d’accès](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateMutex** , fonction](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[**CreateMutexEx** fonction)](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>