---
title: DCOMSCMRemoteCallFlags
description: Contrôle le comportement des appels du gestionnaire de contrôle des services DCOM local (DCOMSCM) à un DCOMSCM distant.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- Valeur de Registre DCOMSCMRemoteCallFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d658b80d347e684aa42aebad936a863b9bca2138b3118508849a730e11878d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678828"
---
# <a name="dcomscmremotecallflags"></a>DCOMSCMRemoteCallFlags

Contrôle le comportement des appels du gestionnaire de contrôle des services DCOM local (DCOMSCM) à un DCOMSCM distant.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur | Description                                       |
|-------|---------------------------------------------------|
| 0x1   | **DCOMSCM \_ Activation \_ utiliser \_ tous les \_ AUTHNSERVICES**  |
| 0x2   | **DCOMSCM \_ Activation \_ interdire un \_ appel non sécurisé \_** |
| 0x4   | **DCOMSCM \_ résoudre \_ utiliser \_ tous les \_ AUTHNSERVICES**     |
| 0x8   | **DCOMSCM \_ résoudre \_ interdire un \_ appel non sécurisé \_**    |
| 0x10  | **DCOMSCM \_ ping \_ utiliser \_ Mid \_ AUTHNSERVICE**         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a>DCOMSCM \_ Activation \_ utiliser \_ toutes les \_ AUTHNSERVICES Description

Lorsque le client émet une demande d’activation qui utilise les paramètres de sécurité par défaut, le DCOMSCM local utilise le service d’authentification Negotiate lors de l’appel RPC d’activation au DCOMSCM distant. Si l’appel échoue, le DCOMSCM local effectue l’appel RPC d’activation en l’absence de sécurité.

**Windows Server 2003 et Windows XP/2000 :** Si l’appel RPC d’activation qui utilise le service Negotiate Authentication échoue, le DCOMSCM local effectue l’appel RPC d’activation à l’aide de Kerberos, NTLM ou d’autres fournisseurs de sécurité configurés. Si aucun fournisseur de sécurité ne fonctionne, le DCOMSCM local effectue l’appel RPC d’activation en l’absence de sécurité.

en définissant cet indicateur, les DCOMSCM locaux sur Windows Vista ou version ultérieure peuvent être configurés pour se comporter comme des systèmes antérieurs à vista. Il n’est pas recommandé de définir cet indicateur, sauf s’il est requis pour des raisons de compatibilité.

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a>DCOMSCM \_ Activation \_ interdire la description de l' \_ appel non sécurisé \_

Si la valeur de l’indicateur d' **\_ \_ \_ \_ appel non sécurisé** de l’activation de DCOMSCM est définie, le DCOMSCM local n’effectue pas d’appel RPC d’activation non sécurisé. Pour permettre aux clients d’effectuer des demandes d’activation avec des paramètres de sécurité autres que ceux par défaut, spécifiez la structure [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) lors de la demande d’activation. Dans ce cas, l' **activation de DCOMSCM \_ \_ utilise \_ tous les \_** indicateurs d' **\_ Activation \_ \_ non sécurisés \_** AUTHNSERVICES et DCOMSCM sont ignorés.

Il n’est pas recommandé de définir cet indicateur, sauf si tous les clients et serveurs du réseau sont entièrement authentifiés.

## <a name="dcomscm_resolve_use_all_authnservices-description"></a>DCOMSCM \_ résoudre \_ utiliser \_ toutes les \_ AUTHNSERVICES Description

Lorsque le client démarshale une référence d’objet, le DCOMSCM local utilise le service d’authentification Negotiate lors de l’appel RPC de résolution OXID au DCOMSCM distant. Si l’appel échoue, le DCOMSCM local effectue l’appel RPC de résolution OXID à l’aide d’aucune sécurité.

**Windows Server 2003 et Windows XP/2000 :** Si l’appel RPC de résolution OXID à l’aide du service d’authentification Negotiate échoue, le DCOMSCM local effectue l’appel RPC de résolution OXID à l’aide de Kerberos, NTLM ou d’autres fournisseurs de sécurité configurés. Si aucun fournisseur de sécurité ne fonctionne, le DCOMSCM local effectue l’appel RPC de résolution OXID à l’aide d’aucune sécurité.

en définissant cet indicateur, les DCOMSCM locaux sur Windows Vista ou version ultérieure peuvent être configurés pour se comporter comme des systèmes antérieurs à vista. Il n’est pas recommandé de définir cet indicateur, sauf s’il est requis pour des raisons de compatibilité.

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a>DCOMSCM \_ résoudre \_ interdire la description de l' \_ appel non sécurisé \_

Si l’indicateur **DCOMSCM \_ résoudre l’interdiction d' \_ \_ \_ appel non sécurisé** est défini, le DCOMSCM local n’effectue pas d’appel RPC de résolution de Oxid non sécurisé. En outre, le DCOMSCM local n’effectue pas un appel RPC garbage collection ping non sécurisé. Il n’est pas recommandé de définir cet indicateur, sauf si tous les clients et serveurs du réseau sont entièrement authentifiés.

## <a name="dcomscm_ping_use_mid_authnservice-description"></a>DCOMSCM \_ ping \_ use \_ Mid \_ AUTHNSERVICE Description

Le DCOMSCM local utilise le service d’authentification Negotiate lors du test ping de l’appel RPC de garbage collection vers le DCOMSCM distant. En cas d’échec de l’appel, le DCOMSCM local effectue l’appel RPC ping de garbage collection sans sécurité.

**Windows Server 2003 et Windows XP/2000 :** En cas d’échec de l’appel RPC ping de garbage collection à l’aide du service Negotiate Authentication, le DCOMSCM local effectue l’appel RPC ping garbage collection à l’aide de Kerberos, NTLM et d’autres fournisseurs de sécurité configurés. Si aucun fournisseur de sécurité ne fonctionne, le DCOMSCM local effectue l’appel RPC ping garbage collection à l’aide d’aucune sécurité.

en définissant cet indicateur, le DCOMSCM local sur Windows Vista ou version ultérieure peut être configuré pour se comporter comme des systèmes antérieurs à vista. Il n’est pas recommandé de définir l’indicateur **\_ ping DCOMSCM \_ use \_ Mid \_ AUTHNSERVICE** , sauf s’il est requis pour des raisons de compatibilité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification des connexions à distance](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[EnableDCOM](enabledcom.md)
</dt> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 