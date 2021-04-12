---
title: ODJ_WIN7BLOB
description: Définition du ODJ_WIN7BLOB IDL
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104316704"
---
# <a name="odj_win7blob-structure"></a>Structure ODJ_WIN7BLOB

Contient les informations de base requises pour joindre un client à un domaine.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a>Membres

### <a name="lpdomain"></a>lpDomain

Doit être défini sur le nom de domaine.

### <a name="lpmachinename"></a>lpMachineName

Doit être défini sur le nom de l’ordinateur.

### <a name="lpmachinepassword"></a>lpMachinePassword

Doit être défini sur un mot de passe en texte clair pour le compte d’ordinateur identifié par lpMachineName

### <a name="dnsdomaininfo"></a>DnsDomainInfo

Contient des informations sur le domaine qui est joint.

### <a name="dcinfo"></a>DcInfo

Contient les informations d’attribution de noms et d’adressage relatives au contrôleur de domaine qui a été utilisé pour créer le compte d’ordinateur Active Directory.

### <a name="options"></a>Options

Doit être défini à zéro.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

[**\_ \_ \_ informations sur le domaine \_ DNS de la stratégie ODJ**](odj-odj_policy_dns_domain_info.md)

[**DOMAIN_CONTROLLER_INFOW**](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



