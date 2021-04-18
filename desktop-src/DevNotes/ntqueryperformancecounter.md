---
description: Retourne la valeur actuelle d’un compteur de performance et, éventuellement, la fréquence du compteur de performance.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: NtQueryPerformanceCounter fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532797"
---
# <a name="ntqueryperformancecounter-function"></a>NtQueryPerformanceCounter fonction)

\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée. Utilisez les fonctions **QueryPerformanceCounter** et **QueryPerformanceFrequency** à la place.\]

Retourne la valeur actuelle d’un compteur de performance et, éventuellement, la fréquence du compteur de performance.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PerformanceCounter* \[ à\]
</dt> <dd>

Adresse d’une variable devant recevoir la valeur actuelle du compteur de performance.

</dd> <dt>

*Performancefrequency n'* \[ out, facultatif\]
</dt> <dd>

Adresse d’une variable qui doit recevoir la fréquence du compteur de performance.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, elle retourne la **\_ réussite** de l’état du code **NTSTATUS** ; sinon, elle retourne un code d’erreur tel que **violation d' \_ accès \_ d’État**.

## <a name="remarks"></a>Notes

Aucun fichier d’en-tête n’est disponible pour **NtQueryPerformanceCounter**. Vous devez utiliser les autres fonctions nommées ci-dessus, bien que vous puissiez également utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.

La fréquence des performances correspond à la fréquence du compteur de performances en Hertz, en particulier en nombre par seconde. Cette valeur dépend de l’implémentation. Si l’implémentation n’a pas de matériel pour prendre en charge la synchronisation des performances, la valeur retournée est 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
