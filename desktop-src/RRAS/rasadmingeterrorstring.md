---
title: RasAdminGetErrorString, fonction (rassapi. h)
description: La fonction RasAdminGetErrorString récupère une chaîne de message qui correspond à un code d’erreur RAS renvoyé par l’une des fonctions d’administration de serveur RAS (RasAdmin).
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RasAdminGetErrorString fonction RAS
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524005"
---
# <a name="rasadmingeterrorstring-function"></a>RasAdminGetErrorString fonction)

\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0. Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003. Les applications doivent utiliser la fonction [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) .\]

La fonction **RasAdminGetErrorString** récupère une chaîne de message qui correspond à un code d’erreur RAS renvoyé par l’une des fonctions d’administration de serveur RAS (RasAdmin). Ces chaînes de message sont extraites de la Rasmsg.dll installée dans le cadre du service RAS.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ResourceId* \[ dans\]
</dt> <dd>

Spécifie un code d’erreur retourné par l’une des fonctions RasAdmin. Cette valeur doit être comprise dans la plage de codes d’erreur de RASBASE à RASBASEEND. Celles-ci sont définies dans Raserror. h.

</dd> <dt>

*lpszString* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit le message d’erreur qui correspond au code d’erreur spécifié.

</dd> <dt>

*InBufSize* \[ dans\]
</dt> <dd>

Spécifie la taille, en caractères, de la mémoire tampon *lpszString* . Les messages d’erreur sont généralement de 80 caractères au maximum ; une taille de mémoire tampon de 512 caractères est toujours appropriée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur. Cette valeur peut être une dernière valeur d’erreur définie par les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)ou [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) . Il peut s’agir de l’un des codes d’erreur suivants :



| Valeur                                                                                                      | Signification                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>   | Les paramètres *ResourceId* ou *lpszString* ne sont pas valides.<br/>      |
| <dl> <dt>**ERREUR \_ de \_ mémoire tampon insuffisante**</dt> </dl> | La taille spécifiée par le paramètre *InBufSize* est trop petite.<br/> |



 

Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Notes

Les fonctions RasAdmin peuvent retourner des codes d’erreur qui ne sont pas dans la plage prise en charge par la fonction **RasAdminGetErrorString** . Par exemple, les fonctions RasAdmin peuvent retourner des codes d’erreur définis dans Lmerr. h et winerror. h. Avant d’appeler **RasAdminGetErrorString**, vérifiez que le code d’erreur se trouve dans la plage RASBASE à RASBASEEND, comme défini dans Raserror. h.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows 2000 Professionnel<br/>                                                   |
| Fin de la prise en charge des serveurs<br/> | Windows 2000 Server<br/>                                                         |
| En-tête<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Bibliothèque<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du service d’accès à distance (RAS)](about-remote-access-service.md)
</dt> <dt>

[Fonctions d’administration du serveur RAS](ras-server-administration-functions.md)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

