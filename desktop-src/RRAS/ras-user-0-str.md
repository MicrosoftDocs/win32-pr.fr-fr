---
title: Structure RAS_USER_0 (rassapi. h)
description: La structure de l' \_ utilisateur RAS \_ 0 est utilisée dans les fonctions RasAdminUserSetInfo et RasAdminUserGetInfo pour spécifier des informations sur un utilisateur.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS_USER_0 de la structure RAS
- Point d’accès RAS du pointeur de structure PRAS_USER_0
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb4b04ddf3b81d330825b3333899e149d2f7b0d1f30c19106c6977e5291846f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789140"
---
# <a name="ras_user_0-structure"></a>Structure de l' \_ utilisateur RAS \_ 0

\[cette version de la structure de l' **\_ utilisateur RAS \_ 0** n’est pas prise en charge à partir de Windows Vista. Utilisez à la place l' [**\_ utilisateur RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) plus récent défini dans mprapi. h.\]

La structure de l' **\_ utilisateur RAS \_ 0** est utilisée dans les fonctions [**RasAdminUserSetInfo**](rasadminusersetinfo.md) et [**RasAdminUserGetInfo**](rasadminusergetinfo.md) pour spécifier des informations sur un utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a>Membres

<dl> <dt>

**bfPrivilege**
</dt> <dd>

Jeu d’indicateurs binaires qui spécifient les privilèges d’accès distant de l’utilisateur. Ce membre peut être une combinaison de l' \_ indicateur RASPRIV DialinPrivilege et de l’un des indicateurs de rappel. Utilisez le \_ masque RASPRIV CallbackType pour identifier le type de privilège de rappel fourni à l’utilisateur. Les indicateurs suivants sont définis.



| Valeur                                                                                                                                                                                                                                         | Signification                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <dt>**RASPRIV \_ Nocallback**</dt> </dl>                             | L’utilisateur n’a pas de privilège de rappel.<br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <dt>**RASPRIV \_ AdminSetCallback**</dt> </dl>     | Le compte d’utilisateur est configuré pour demander à l’administrateur de définir le numéro de rappel.<br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <dt>**RASPRIV \_ CallerSetCallback**</dt> </dl> | L’utilisateur distant peut spécifier un numéro de téléphone de rappel lors de la numérotation.<br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <dt>**RASPRIV \_ DialinPrivilege**</dt> </dl>         | L’utilisateur a l’autorisation de se connecter à ce serveur.<br/>                                 |



 

Spécifiez l’un des indicateurs de rappel dans l’appel à la fonction [**RasAdminUserSetInfo**](rasadminusersetinfo.md) .

</dd> <dt>

**szPhoneNumber**
</dt> <dd>

Chaîne Unicode se terminant par un caractère null qui spécifie le numéro de téléphone de rappel de l’utilisateur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du service d’accès à distance (RAS)](about-remote-access-service.md)
</dt> <dt>

[Structures d’administration de serveur RAS](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

 





