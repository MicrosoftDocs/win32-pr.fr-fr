---
title: sh_socket, mot clé
description: Le \_ mot clé \ SH Socket \ spécifie que l’objet système est un handle d’un Socket.
keywords:
- sh_socket mot clé MIDL
topic_type:
- apiref
api_name:
- sh_socket keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 542610d586af084f4238e70cd0e6c848099e4d2153d0feab8d617475a50476e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822099"
---
# <a name="sh_socket-keyword"></a>\_mot clé de socket SH

Le mot clé de **\_ Socket SH** spécifie qu’un `system_handle` contient un handle vers un Socket.

``` syntax
[system_handle(sh_socket)]

[system_handle(sh_socket, access-rights)]
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
    HRESULT ListenToSocket([in, system_handle(sh_socket)] HANDLE socket);
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

[Windows Sockets 2](../winsock/windows-sockets-start-page-2.md)
</dt> </dl>
