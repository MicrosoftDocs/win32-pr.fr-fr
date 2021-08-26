---
title: RasAdminPortDisconnect, fonction (rassapi. h)
description: La fonction RasAdminPortDisconnect déconnecte un port en cours d’utilisation.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- RasAdminPortDisconnect fonction RAS
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a0f3abf4cee54f92c9bfd846557623de5e23fffd4724a701ca7c04aa818af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028519"
---
# <a name="rasadminportdisconnect-function"></a>RasAdminPortDisconnect fonction)

\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0. elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003. Les applications doivent utiliser la fonction [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) .\]

La fonction **RasAdminPortDisconnect** déconnecte un port en cours d’utilisation.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszServer* \[ dans\]
</dt> <dd>

pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du serveur RAS Windows NT/Windows 2000. Spécifiez le nom avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *NomServeur*.

</dd> <dt>

*lpszPort* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du port sur le serveur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour peut être l’un des codes d’erreur suivants.



| Valeur                                                                                               | Signification                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**PORT d’erreur \_ non valide \_**</dt> </dl> | Le port spécifié n’est pas valide.<br/>    |
| <dl> <dt>**NERR \_ UserNotFound**</dt> </dl>   | Le port n’est pas en cours d’utilisation.<br/> |



 

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
</dt> </dl>

 

