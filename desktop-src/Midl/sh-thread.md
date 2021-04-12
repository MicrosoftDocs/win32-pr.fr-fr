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
ms.openlocfilehash: 2c82dc41d2b1c7cba740c897ef6cea9094979cc3
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104211171"
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

## <a name="remarks"></a>Notes

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
| Client minimal pris en charge | Mise à jour anniversaire Windows 10 (version 1607, Build 14393) |
| Serveur minimal pris en charge | Windows Server 2016 (Build 14393) |

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