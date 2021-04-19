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
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106527270"
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

## <a name="remarks"></a>Notes

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
| Client minimal pris en charge | Mise à jour anniversaire Windows 10 (version 1607, Build 14393) |
| Serveur minimal pris en charge | Windows Server 2016 (Build 14393) |

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