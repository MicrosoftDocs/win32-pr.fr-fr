---
title: sh_thread, mot clé
description: Le \_ mot clé \ SH thread \ spécifie que l’objet système est un handle d’un thread.
keywords:
- sh_thread mot clé MIDL
topic_type:
- apiref
api_name:
- sh_thread keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5cd3f5458e54ccd266f5ef0920b1cc79e1c0b42e35fac51f7ac353d22409aaa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641329"
---
# <a name="sh_thread-keyword"></a>SH \_ (mot clé)

Le mot clé de **\_ thread SH** spécifie qu’un `system_handle` contient un descripteur d’un thread.

``` syntax
[system_handle(sh_thread)]

[system_handle(sh_thread, access-rights)]
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
    HRESULT SetThread([in, system_handle(sh_process)] HANDLE threadHandle);
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

[À propos des processus et des threads](../procthread/about-processes-and-threads.md)
</dt> <dt>

[Sécurité des threads et droits d’accès](../procthread/thread-security-and-access-rights.md)
</dt> <dt>

[**CreateThread** , fonction](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
</dt> <dt>

[**OpenThread** fonction)](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)
</dt> </dl>