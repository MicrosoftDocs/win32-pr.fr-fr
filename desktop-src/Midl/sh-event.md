---
title: sh_event, mot clé
description: Le \_ mot clé \ SH Event \ spécifie que l’objet système est un handle d’événement.
keywords:
- sh_event mot clé MIDL
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1a9b6dc7cc9dc4de4abd5dcc88a53588167db59d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "106543756"
---
# <a name="sh_event-keyword"></a>SH \_ (mot clé)

Le mot clé **\_ Event SH** spécifie qu’un `system_handle` contient un descripteur d’événement.

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
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
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
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

[Objets d’événement](../sync/event-objects.md)
</dt> <dt>

[Sécurité de l’objet de synchronisation et droits d’accès](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateEvent** (fonction)](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**CreateEventEx** fonction)](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
