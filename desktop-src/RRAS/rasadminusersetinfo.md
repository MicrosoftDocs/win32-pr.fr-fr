---
title: RasAdminUserSetInfo, fonction (rassapi. h)
description: La fonction RasAdminUserSetInfo définit les autorisations RAS et le numéro de téléphone de rappel pour un utilisateur spécifié.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RasAdminUserSetInfo fonction RAS
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51bc4b56b9aa606892002fbef0eda8036c45442c06ce06b8561afba57620b7a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028429"
---
# <a name="rasadminusersetinfo-function"></a>RasAdminUserSetInfo fonction)

\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0. elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003. Les applications doivent utiliser la fonction [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) .\]

La fonction **RasAdminUserSetInfo** définit les autorisations RAS et le numéro de téléphone de rappel pour un utilisateur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszUserAccountServer* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du contrôleur de domaine principal ou secondaire qui possède la base de données de comptes d’utilisateur. Utilisez la fonction [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) pour récupérer ce nom de serveur.

</dd> <dt>

*lpszUser* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom de l’utilisateur pour lequel les informations RAS doivent être définies.

</dd> <dt>

*pRasUser0* \[ dans\]
</dt> <dd>

Pointeur vers la structure d' [**\_ utilisateur RAS \_ 0**](ras-user-0-str.md) qui spécifie les nouvelles données RAS pour l’utilisateur spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour peut être l’un des codes d’erreur suivants.



| Valeur                                                                                                           | Description                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERREUR de \_ données non valides \_**</dt> </dl>             | La mémoire tampon *pRasUser0* contient des données non valides.<br/>                                        |
| <dl> <dt>**ERREUR \_ \_ numéro de rappel non valide \_**</dt> </dl> | Le numéro de rappel spécifié dans la mémoire tampon *pRasUser0* contient des caractères non valides.<br/> |
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl>               | Mémoire insuffisante pour exécuter cette fonction.<br/>                                        |



 

Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Lors de la définition des autorisations RAS pour un utilisateur, le membre **bfPrivilege** de la structure de l' [**\_ utilisateur RAS \_ 0**](ras-user-0-str.md) doit spécifier au moins l’un des indicateurs de rappel. Par exemple, pour définir les privilèges d’un utilisateur afin d’autoriser les droits d’accès à distance, mais aucun privilège de rappel, définissez **bfPrivilege** sur RASPRIV \_ DialinPrivilege \| RASPRIV \_ nocallback.

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

[**\_Utilisateur RAS \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> </dl>

 

