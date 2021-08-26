---
title: RasAdminServerGetInfo, fonction (rassapi. h)
description: La fonction RasAdminServerGetInfo obtient la configuration du serveur d’un serveur RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RasAdminServerGetInfo fonction RAS
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f6f83f7310700e774692d876bda979343da80aa45ea8012bf187e50f0af67bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028449"
---
# <a name="rasadminservergetinfo-function"></a>RasAdminServerGetInfo fonction)

\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0. elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003. Les applications doivent utiliser la fonction [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) .\]

La fonction **RasAdminServerGetInfo** obtient la configuration du serveur d’un serveur RAS.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszServer* \[ dans\]
</dt> <dd>

pointeur vers une chaîne Unicode terminée par le caractère **null** qui spécifie le nom du serveur RAS Windows NT/Windows 2000. Si ce paramètre a la **valeur null**, la fonction retourne des informations sur l’ordinateur local. Spécifiez le nom avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *NomServeur*.

</dd> <dt>

*pRasServer0* \[ à\]
</dt> <dd>

Pointeur vers la structure du [**\_ serveur RAS \_ 0**](ras-server-0-str.md) qui reçoit le nombre de ports configurés sur le serveur, le nombre de ports en cours d’utilisation et le numéro de version du serveur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur. Les codes d’erreur possibles incluent ceux retournés par [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour la fonction [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) . Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler **GetLastError**.

## <a name="remarks"></a>Remarques

Pour énumérer tous les serveurs RAS dans un domaine, appelez la fonction [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) et spécifiez la \_ \_ numérotation de type SV pour le paramètre *ServerType* .

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

[**NetServerEnum**](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[**\_Serveur RAS \_ 0**](ras-server-0-str.md)
</dt> </dl>

 

