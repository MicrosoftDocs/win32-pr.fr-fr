---
title: sh_reg_key, mot clé
description: Le \_ mot clé \ SH reg \_ key \ spécifie que l’objet système est un handle de clé de registre.
keywords:
- sh_reg_key mot clé MIDL
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: cec526bed766534f82d5a1bc24c55050dea814ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "106540912"
---
# <a name="sh_reg_key-keyword"></a>SH \_ reg \_ Key (mot clé)

Le mot clé **SH \_ \_ reg** spécifie qu’un `system_handle` contient un handle vers une clé de registre.

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
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
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
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

[Registre](../sysinfo/registry.md)
</dt> <dt>

[Sécurité de la clé de Registre et droits d’accès](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[Fonction **RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
