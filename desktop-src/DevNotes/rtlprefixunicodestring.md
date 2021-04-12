---
description: Compare deux chaînes Unicode pour déterminer si une chaîne est un préfixe de l’autre.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: RtlPrefixUnicodeString, fonction (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483136"
---
# <a name="rtlprefixunicodestring-function"></a>RtlPrefixUnicodeString fonction)

Compare deux chaînes Unicode pour déterminer si une chaîne est un préfixe de l’autre.

## <a name="syntax"></a>Syntaxe


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chaîne1* \[ dans\]
</dt> <dd>

Pointeur vers la première chaîne, qui peut être un préfixe de la chaîne Unicode mise en mémoire tampon à *Chaîne2*.

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

**True** si *Chaîne1* est un préfixe de *Chaîne2*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                    |
| Plateforme cible<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| En-tête<br/>                   | <dl> <dt>Ntddk. h (inclure Ntddk. h)</dt> </dl>                                    |
| Bibliothèque<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RtlCompareUnicodeString**](rtlcompareunicodestring.md)
</dt> </dl>

 

 




