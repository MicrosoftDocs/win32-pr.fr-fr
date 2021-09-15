---
title: OP_CERT_SST_STORE
description: Définition du OP_CERT_SST_STORE IDL
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 294d21d730e1cce478088cddb43686706217ec5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517761"
---
# <a name="op_cert_sst_store-structure"></a>Structure OP_CERT_SST_STORE

Contient un magasin de certificats sérialisés.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a>Membres

### <a name="storelocation"></a>StoreLocation

Contient un identificateur pour le magasin de certificats à partir d' [**emplacements du magasin système**](../seccrypto/system-store-locations.md).

### <a name="pstorename"></a>pStoreName

Contient le nom du magasin.

### <a name="cbsst"></a>cbSst

Contient la taille de pSst en octets.

### <a name="psst"></a>pSst

Contient un magasin de certificats sérialisés (voir [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)