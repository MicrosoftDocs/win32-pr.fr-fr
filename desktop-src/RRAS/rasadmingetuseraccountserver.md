---
title: RasAdminGetUserAccountServer, fonction (rassapi. h)
description: La fonction RasAdminGetUserAccountServer récupère le nom du serveur qui contient la base de données de comptes d’utilisateur. Utilisez le nom de serveur renvoyé dans les fonctions RasAdminUserGetInfo et RasAdminUserSetInfo pour obtenir ou définir des informations sur un utilisateur spécifié.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RasAdminGetUserAccountServer fonction RAS
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528122"
---
# <a name="rasadmingetuseraccountserver-function"></a>RasAdminGetUserAccountServer fonction)

\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0. Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003. Les applications doivent utiliser la fonction [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) .\]

La fonction **RasAdminGetUserAccountServer** récupère le nom du serveur qui contient la base de données de comptes d’utilisateur. Utilisez le nom de serveur renvoyé dans les fonctions [**RasAdminUserGetInfo**](rasadminusergetinfo.md) et [**RasAdminUserSetInfo**](rasadminusersetinfo.md) pour obtenir ou définir des informations sur un utilisateur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszDomain* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère **null** qui spécifie le nom du domaine auquel le serveur RAS appartient. Ce paramètre a la **valeur null** pour les applications d’administration RAS qui s’exécutent sur des stations de travail ou des serveurs qui ne sont pas membres d’un domaine. Si ce paramètre a la **valeur null**, le paramètre *lpszServer* doit être non **null**.

</dd> <dt>

*lpszServer* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère **null** qui spécifie le nom du serveur RAS. Spécifiez le nom avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *NomServeur*. Ce paramètre peut avoir la **valeur null** si le paramètre *lpszDomain* n’a pas la **valeur null**.

</dd> <dt>

*lpszUserAccountServer* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit une chaîne Unicode terminée par le caractère **null** qui spécifie le nom d’un contrôleur de domaine qui possède la base de données de compte d’utilisateur. La mémoire tampon doit être suffisamment grande pour contenir le nom du serveur (ONCLEn + 1). La fonction préfixe le nom du serveur retourné avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *ServerName*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour peut être le code d’erreur suivant.



| Valeur                                                                                                    | Signification                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl> | *LpszDomain* et *lpszServer* sont tous deux **null**.<br/> |



 

Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Notes

La fonction **RasAdminGetUserAccountServer** obtient le nom du serveur avec la base de données des comptes d’utilisateur. Cette fonction requiert le nom du serveur RAS ou le nom du domaine dans lequel réside le serveur RAS.

Le paramètre *lpszDomain* doit spécifier un nom de domaine valide. Ce paramètre a la **valeur null** pour les applications d’administration RAS s’exécutant sur des serveurs qui ne sont pas membres d’un domaine (par exemple, le serveur est dans son propre groupe de travail). Dans ce cas, le paramètre *lpszServer* doit spécifier le nom du serveur. Pour récupérer le nom du serveur, appelez la fonction [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) . Veillez à faire précéder le nom du serveur de \\ \\ caractères «».

Si le nom du serveur spécifié par *lpszServer* est un serveur autonome (autrement dit, si le serveur ou la station de travail n’est pas membre d’un domaine), le nom du serveur lui-même est retourné dans la mémoire tampon *lpszUserAccountServer* .

Utilisez ensuite le nom du serveur de compte d’utilisateur dans un appel à la fonction [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) pour énumérer les utilisateurs de la base de données des comptes d’utilisateur.

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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

