---
title: OP_CERT_PART
description: Définition du OP_CERT_PART IDL
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517773"
---
# <a name="op_cert_part-structure"></a>Structure OP_CERT_PART

Contient des magasins de certificats et PFX sérialisés.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a>Membres

### <a name="cpfxstores"></a>cPfxStores

Contient le nombre d’éléments dans pPfxStores.

### <a name="ppfxstores"></a>pPfxStores

Contient un tableau de structures OP_CERT_PFX_STORE.

### <a name="csststores"></a>cSstStores

Contient le nombre d’éléments dans pSstStores.

### <a name="psststores"></a>pSstStores

Contient un tableau de structures OP_CERT_SST_STORE.

### <a name="extension"></a>Extension

Réservé pour une utilisation ultérieure et doit contenir uniquement des zéros.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

[**\_ \_ magasin pfx du certificat op \_**](odj-op_cert_pfx_store.md)

[**\_ \_ magasin SST du certificat op \_**](odj-op_cert_sst_store.md)

[**\_objet BLOB op**](odj-op_blob.md)

