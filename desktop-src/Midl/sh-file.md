---
title: sh_file, mot clé
description: Le fichier \ SH \_ \ Keyword spécifie que l’objet système est un handle de fichier.
keywords:
- sh_file mot clé MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 05b76ad772ca628a28677d9b0da06252d0fec70251a4a197d39b50b9760ef931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013627"
---
# <a name="sh_file-keyword"></a>\_fichier sh (mot clé)

Le mot clé **\_ fichier sh** spécifie qu’un `system_handle` contient un descripteur d’un fichier.

``` syntax
[system_handle(sh_file)]

[system_handle(sh_file, access-rights)]
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
    HRESULT WriteThisFile([in, system_handle(sh_file)] HANDLE file);

    HRESULT GetFileToRead([out, system_handle(sh_file, READ_CONTROL | SYNCHRONIZE | FILE_READ_DATA | FILE_READ_keywordS | FILE_READ_EA)] HANDLE* pReadThisFile);
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

[Sécurité des fichiers et droits d’accès](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[DirectComposition](/windows/win32/api/_directcomp/)
</dt> <dt>

[**DCompositionCreateSurfaceHandle** fonction)](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> <dt>
