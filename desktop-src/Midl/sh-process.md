---
title: sh_process, mot clé
description: Le \_ mot clé \ SH process \ spécifie que l’objet système est un handle d’un processus.
keywords:
- sh_process mot clé MIDL
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3dc11f2980e5124bbc76d0b57fce21d8007b0c09905ca47707d5be6fbb112d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146272"
---
# <a name="sh_process-keyword"></a>SH \_ Process (mot clé)

Le mot clé de **\_ processus SH** spécifie qu’un `system_handle` contient un descripteur d’un processus.

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
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
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
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

[Sécurité des processus et droits d’accès](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[Fonction **CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[**OpenProcess** , fonction](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>