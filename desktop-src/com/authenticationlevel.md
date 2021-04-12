---
title: AuthenticationLevel
description: Définit le niveau d’authentification pour les applications qui n’appellent pas CoInitializeSecurity ou pour les applications qui appellent CoInitializeSecurity et spécifient un AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- Valeur de Registre AuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311506"
---
# <a name="authenticationlevel"></a>AuthenticationLevel

Définit le niveau d’authentification pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou pour les applications qui appellent **CoInitializeSecurity** et spécifient un AppID.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur **reg \_ DWORD** qui est équivalente \_ aux \_ constantes de niveau d’authentification RPC C \_ .



| Valeur | Constante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ Authn \_ niveau \_ aucun           |
| 2     | \_ \_ \_ connexion au niveau AUTHn C RPC \_        |
| 3     | \_ \_ \_ appel au niveau d’authentification RPC C \_           |
| 4     | protocole d’authentification de l' \_ authentification RPC C \_ \_ \_            |
| 5     | \_ \_ \_ intégrité PKT du niveau d’authentification RPC \_ C \_ |
| 6     | \_confidentialité du \_ niveau d’authentification RPC C \_ \_ \_   |



 

La valeur **AuthenticationLevel** est similaire à la valeur [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) . Si la valeur **AuthenticationLevel** est présente, elle est utilisée à la place de la valeur **LegacyAuthenticationLevel** pour cet AppID.

Si la valeur de **AuthenticationLevel** est de type incorrect ou hors limites, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) échoue, provoquant l’échec du marshaling de l’interface. Cela empêche l’application d’effectuer des appels (Cross-Apartment, Cross-thread, Cross-process ou Cross-Computer).

Les valeurs **AuthenticationLevel** et [**AccessPermission**](accesspermission.md) sont indépendantes. Si aucun n’est présent, la valeur par défaut est utilisée. Les règles suivantes répertorient l’interaction entre la valeur **AuthenticationLevel** et la valeur **AccessPermission** :

-   Si **AuthenticationLevel** a la valeur None, les valeurs [**AccessPermission**](accesspermission.md) et [**DefaultAccessPermission**](defaultaccesspermission.md) sont ignorées (pour cette application).
-   Si **AuthenticationLevel** n’est pas présent et que [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) a la valeur None, les valeurs [**AccessPermission**](accesspermission.md) et [**DefaultAccessPermission**](defaultaccesspermission.md) sont ignorées (pour cette application).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes de niveau d’authentification](com-authentication-level-constants.md)
</dt> <dt>

[**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)
</dt> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 




