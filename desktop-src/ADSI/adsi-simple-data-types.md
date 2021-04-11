---
title: Types de données simples ADSI (IADs. h)
description: Les interfaces ADSI (Active Directory Service Interfaces) définissent et utilisent les types de données simples suivants.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032498"
---
# <a name="adsi-simple-data-types"></a>Types de données simples ADSI

Les interfaces ADSI (Active Directory Service Interfaces) définissent et utilisent les types de données simples suivants.


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

**\_BOOLÉENNE ads**
</dt> <dd>

DWORD

</dd> <dt>

**\_ \_ chaîne exacte de cas ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_chaîne d' \_ ignorer le cas ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_chaîne DN \_ ads**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_entier ads**
</dt> <dd>

DWORD

</dd> <dt>

**\_grand \_ entier ads**
</dt> <dd>

[**\_entier long**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

**\_chaîne numérique \_ ads**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_classe d’objet ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_chaînes imprimables \_ ads**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_handle de recherche ADS \_**
</dt> <dd>

HANDLE

</dd> <dt>

**\_heure UTC \_ ads**
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque ADSI lit un attribut qui a été défini en tant qu' **entier** dans le schéma LDAP, il gère toujours l’entier comme une valeur de 32 bits et peut tronquer les données. Cela ne concerne que les serveurs LDAP qui autorisent des valeurs entières de taille arbitraire. Si l’attribut est un attribut personnalisé défini en étendant le schéma, vous pouvez éviter ce problème en définissant l’attribut personnalisé en tant que chaîne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl> |



 

