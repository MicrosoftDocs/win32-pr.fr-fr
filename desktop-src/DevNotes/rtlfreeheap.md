---
description: Libère un bloc de mémoire qui a été alloué à partir d’un segment de mémoire par RtlAllocateHeap.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: RtlFreeHeap, fonction (Ntifs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dd46808c898cd934bbb4ee8804027bcb926e4a5cd07eb1521e2814a2c4b0e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538071"
---
# <a name="rtlfreeheap-function"></a>RtlFreeHeap fonction)

Libère un bloc de mémoire qui a été alloué à partir d’un segment de mémoire par [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).

## <a name="syntax"></a>Syntaxe


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HeapHandle* \[ dans\]
</dt> <dd>

Handle pour le tas dont le bloc de mémoire doit être libéré. Ce paramètre est un handle retourné par [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).

</dd> <dt>

*Indicateurs* \[ dans, facultatif\]
</dt> <dd>

Jeu d’indicateurs qui contrôle les aspects de la libération d’un bloc de mémoire. La spécification de la valeur suivante remplace la valeur correspondante qui a été spécifiée dans le paramètre *Flags* lorsque le segment de mémoire a été créé par [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).



| Indicateur                           | Signification                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| segment de mémoire \_ non \_ sérialisé<br/> | L’exclusion mutuelle n’est pas utilisée quand **RtlFreeHeap** accède au segment de mémoire. <br/> |



 

</dd> <dt>

*HeapBase* \[ dans\]
</dt> <dd>

Pointeur vers le bloc de mémoire à libérer. Ce pointeur est retourné par [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le bloc a été correctement libéré ; **False** dans le cas contraire.

> [!Note]  
> à partir de Windows 8 la valeur de retour est de type **logique**, dont la taille est différente de la valeur **booléenne**.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                    |
| Plateforme cible<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| En-tête<br/>                   | <dl> <dt>Ntifs. h (inclure Ntifs. h)</dt> </dl>                                    |
| Bibliothèque<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[**RtlDestroyHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
