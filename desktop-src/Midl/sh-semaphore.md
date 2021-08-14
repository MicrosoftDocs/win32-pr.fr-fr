---
title: sh_semaphore, mot clé
description: Le \_ mot clé \ SH Semaphore \ spécifie que l’objet système est un descripteur d’un sémaphore.
keywords:
- sh_semaphore mot clé MIDL
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a48d0b085f3653679c7399ad0f234e7b7a1ecf1b1532480c003923967ac4830a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383219"
---
# <a name="sh_semaphore-keyword"></a>SH \_ (mot clé)

Le mot clé de **\_ sémaphore SH** spécifie qu’un `system_handle` contient un descripteur d’un sémaphore.

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
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
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
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

[Objets Semaphore](../sync/semaphore-objects.md)
</dt> <dt>

[Sécurité de l’objet de synchronisation et droits d’accès](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateSemaphore,** fonction)](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[**CreateSemaphoreEx** fonction)](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
