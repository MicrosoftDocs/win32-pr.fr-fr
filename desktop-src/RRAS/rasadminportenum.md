---
title: RasAdminPortEnum, fonction (rassapi. h)
description: La fonction RasAdminPortEnum énumère tous les ports sur le serveur RAS spécifié. Pour chaque port sur le serveur, la fonction retourne la \_ structure du port RAS \_ 0 qui contient des informations sur le port.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RasAdminPortEnum fonction RAS
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e4841627ce5df3feee3f885b399a070388ed55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533058"
---
# <a name="rasadminportenum-function"></a>RasAdminPortEnum fonction)

\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0. Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003. Les applications doivent utiliser la fonction [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) .\]

La fonction **RasAdminPortEnum** énumère tous les ports sur le serveur RAS spécifié. Pour chaque port sur le serveur, la fonction retourne la structure du [**\_ port RAS \_ 0**](ras-port-0-str.md) qui contient des informations sur le port.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszServer* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du serveur RAS. Spécifiez le nom avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *NomServeur*.

</dd> <dt>

*ppRasPort0* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit un pointeur vers une mémoire tampon qui contient un tableau de structures du [**\_ port RAS \_ 0**](ras-port-0-str.md) . Lorsque l’application a terminé la mémoire, libérez-la en appelant la fonction [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .

</dd> <dt>

*pcEntriesRead* \[ à\]
</dt> <dd>

Pointeur vers une variable de 16 bits qui reçoit le nombre total de structures [**RAS \_ port \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) retournées dans le tableau *ppRasPort0* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour peut être le code d’erreur suivant.



| Valeur                                                                                             | Signification                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NERR \_ ItemNotFound**</dt> </dl> | Aucun port ne peut être énuméré. Cela peut être dû au fait que tous les ports configurés sur le serveur sont actuellement utilisés pour la numérotation.<br/> |



 

Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

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

[**\_Port RAS \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

