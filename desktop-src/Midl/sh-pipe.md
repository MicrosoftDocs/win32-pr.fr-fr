---
title: sh_pipe, mot clé
description: Le \_ mot clé \ SH pipe \ spécifie que l’objet système est un handle vers un canal.
keywords:
- sh_pipe mot clé MIDL
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 9f9deab2bf5a751d3b2d5956d4d33a1d5b347e18
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "106531440"
---
# <a name="sh_pipe-keyword"></a>\_mot clé de canal SH

Le mot clé de **\_ canal SH** spécifie qu’un `system_handle` contient un handle vers un canal.

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
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
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
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

[À propos des canaux](../ipc/about-pipes.md)
</dt> <dt>

[Sécurité des fichiers et droits d’accès](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[**CreatePipe** fonction)](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[**CreateNamedPipe** fonction)](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
