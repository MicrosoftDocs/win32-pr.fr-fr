---
description: Copie le contenu d’un bloc de mémoire source vers un bloc de mémoire de destination et prend en charge les blocs de mémoire source et de destination qui se chevauchent.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Fonction RtlMoveMemory (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517186"
---
# <a name="rtlmovememory-function"></a>RtlMoveMemory fonction)

Copie le contenu d’un bloc de mémoire source vers un bloc de mémoire de destination et prend en charge les blocs de mémoire source et de destination qui se chevauchent.

## <a name="syntax"></a>Syntaxe


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Destination* \[ à\]
</dt> <dd>

Pointeur vers le bloc de mémoire de destination dans lequel copier les octets.

</dd> <dt>

*Source* \[ dans\]
</dt> <dd>

Pointeur vers le bloc de mémoire source à partir duquel copier les octets.

</dd> <dt>

*Longueur* \[ dans\]
</dt> <dd>

Nombre d’octets à copier de la source vers la destination.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Aucune

## <a name="remarks"></a>Notes

Le bloc de mémoire source, qui est défini par la *source* et la *longueur*, peut chevaucher le bloc de mémoire de destination, qui est défini par la *destination* et la *longueur*.

La routine [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) s’exécute plus rapidement que **RtlMoveMemory**, mais **RtlCopyMemory** requiert que les blocs de mémoire source et de destination ne se chevauchent pas.

Les appelants de **RtlMoveMemory** peuvent s’exécuter à n’importe quel niveau IRQL si les blocs de mémoire source et de destination se trouvent dans la mémoire système non paginée. Dans le cas contraire, l’appelant doit s’exécuter au niveau IRQL <= APC \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                    |
| Plateforme cible<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| En-tête<br/>                   | <dl> <dt>WDM. h (inclure WDM. h, Ntddk. h ou Ntifs. h)</dt> </dl>                   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
