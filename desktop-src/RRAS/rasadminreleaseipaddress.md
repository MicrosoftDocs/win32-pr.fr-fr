---
title: RasAdminReleaseIpAddress fonction de rappel
description: La fonction RasAdminReleaseIpAddress est une fonction définie par l’application qui est exportée par une DLL d’administration de serveur RAS tierce.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- Fonction de rappel RasAdminReleaseIpAddress RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d58c162ebc6d340b9bd913407bc00aac87e208e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229247"
---
# <a name="rasadminreleaseipaddress-callback-function"></a>RasAdminReleaseIpAddress fonction de rappel

\[La fonction **RasAdminReleaseIpAddress** peut être utilisée dans Windows NT 4,0 et n’est pas disponible dans les versions ultérieures. Utilisez plutôt [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]

La fonction **RasAdminReleaseIpAddress** est une fonction définie par l’application qui est exportée par une DLL d’administration de serveur RAS tierce. RAS appelle cette fonction pour notifier à la DLL que le client distant a été déconnecté et que l’adresse IP doit être libérée.

## <a name="syntax"></a>Syntaxe


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszUserName* \[ dans\]
</dt> <dd>

Spécifie le pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom d’un utilisateur distant pour lequel une adresse IP a été obtenue précédemment à l’aide de la fonction [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) .

</dd> <dt>

*lpszPortName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du port sur lequel l’utilisateur spécifié par *lpszUserName* est connecté.

</dd> <dt>

*pipAddress* \[ dans\]
</dt> <dd>

Pointeur vers une variable **ipaddr** qui spécifie l’adresse IP renvoyée pour cet utilisateur lors d’un appel précédent à [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Notes

Le serveur RAS appelle la fonction **RasAdminReleaseIpAddress** uniquement si l’application a retourné la **valeur true** dans le paramètre *bNotifyRelease* au cours de l’appel précédent à [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) pour l’utilisateur spécifié par le paramètre *lpszUserName* .

Le programme d’installation d’une DLL d’administration RAS tierce doit inscrire la DLL auprès de RAS en fournissant les informations sous la clé suivante dans le registre :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Pour inscrire la DLL, définissez les valeurs suivantes sous cette clé.



| Nom de la valeur    | Données de valeur                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Chaîne **\_ SZ reg** qui contient le nom complet convivial de la dll. |
| *DLLPath*     | Chaîne **\_ SZ reg** contenant le chemin d’accès complet de la dll.                  |



 

Par exemple, l’entrée de Registre pour une DLL d’administration RAS d’une société fictive nommée ProElectron, Inc. peut être :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **reg \_ SZ** : dll d’administration du service d’accès distant diselectron *DllPath*: **reg \_ SZ** : C : \\ NT \\ system32 \\ntwkadm.dll

Le programme d’installation d’une DLL d’administration RAS doit également fournir des fonctionnalités de suppression/désinstallation. Si un utilisateur supprime la DLL, le programme d’installation doit supprimer les entrées de registre de la DLL.

 

 