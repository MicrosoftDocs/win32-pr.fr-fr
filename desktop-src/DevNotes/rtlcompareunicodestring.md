---
description: Compare deux chaînes Unicode.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Fonction RtlCompareUnicodeString (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861057"
---
# <a name="rtlcompareunicodestring-function"></a>RtlCompareUnicodeString fonction)

Compare deux chaînes Unicode.

## <a name="syntax"></a>Syntaxe


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chaîne1* \[ dans\]
</dt> <dd>

Pointeur vers la première chaîne.

</dd> <dt>

*Chaîne2* \[ dans\]
</dt> <dd>

Pointeur vers la deuxième chaîne.

</dd> <dt>

*CaseInSensitive* \[ dans\]
</dt> <dd>

Si la **valeur est true**, la casse doit être ignorée lors de la comparaison.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur signée qui donne les résultats de la comparaison :



| Code de retour                                                                               | Description                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**Nuls**</dt> </dl>       | *Chaîne1* est égal à *Chaîne2*.<br/>          |
| <dl> <dt>**< zéro**</dt> </dl>  | *Chaîne1* est inférieur à *Chaîne2*.<br/>    |
| <dl> <dt>**> zéro**</dt> </dl> | *Chaîne1* est supérieur à *Chaîne2*.<br/> |



 

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

[**RtlCompareString**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[**RtlEqualString**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
