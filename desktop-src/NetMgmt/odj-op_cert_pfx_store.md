---
title: OP_CERT_PFX_STORE
description: Définition du OP_CERT_PFX_STORE IDL
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 28e8b9e1a6d73f3d93e1700f812b21a0edf21982b7d5b9c927f4e7391b961850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911539"
---
# <a name="op_cert_pfx_store-structure"></a>Structure OP_CERT_PFX_STORE

Contient une structure PFX sérialisée.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a>Membres

### <a name="ptemplatename"></a>pTemplateName

Doit être défini sur le nom du modèle de certificat utilisé pour créer le certificat.

### <a name="ulprivatekeyexportpolicy"></a>ulPrivateKeyExportPolicy

Contient une valeur de l’énumération [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) .

### <a name="ppolicyserverurl"></a>pPolicyServerUrl

Doit être défini sur l’URL du serveur de stratégie.

### <a name="ulpolicyserverurlflags"></a>ulPolicyServerUrlFlags

Contient une valeur de l’énumération [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) .

### <a name="ppolicyserverid"></a>pPolicyServerId

Contient une chaîne qui identifie de façon unique le serveur de stratégie

### <a name="cbpfx"></a>cbPfx

Contient la taille de pPfx en octets.

### <a name="ppfx"></a>pPfx

Contient une structure PFX sérialisée (voir [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)
