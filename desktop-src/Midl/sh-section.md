---
title: sh_section, mot clé
description: La section \ SH \_ \ Keyword spécifie que l’objet système est un handle d’une section.
keywords:
- sh_section mot clé MIDL
topic_type:
- apiref
api_name:
- sh_section keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: eab938b414745a24f81c1f61f2320443e7f3e9600eefab5f590598294345d83f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806248"
---
# <a name="sh_section-keyword"></a>SH \_ section (mot clé)

Le mot clé de la **\_ section SH** spécifie qu’un `system_handle` contient un handle vers une section.

``` syntax
[system_handle(sh_section)]

[system_handle(sh_section, access-rights)]
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
    HRESULT GiveSection([in, system_handle(sh_section)] HANDLE section);

    HRESULT GetSectionToWatch([out, system_handle(sh_section, SECTION_MAP_READ)] HANDLE* pSection);
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

[Objets et vues de section](/windows-hardware/drivers/kernel/section-objects-and-views)
</dt> <dt>

[Fonction **ZwCreateSection** (y compris les spécifications d’accès)](/windows-hardware/drivers/ddi/wdm/nf-wdm-zwcreatesection)
</dt> </dl>
