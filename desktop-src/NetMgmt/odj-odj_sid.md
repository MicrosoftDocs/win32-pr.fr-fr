---
title: ODJ_SID
description: Définition du ODJ_SID IDL
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517789"
---
# <a name="odj_sid-structure"></a>Structure ODJ_SID

Contient un identificateur de sécurité (SID).

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a>Membres

### <a name="revision"></a>Révision

Doit être défini sur la révision SID.

### <a name="subauthoritycount"></a>SubAuthorityCount

Doit être défini sur le nombre d’éléments dans la sous-autorité.

### <a name="identifierauthority"></a>IdentifierAuthority

Doit être défini sur l’identificateur de l’autorité de SID.

### <a name="subauthority"></a>Sous-autorité

Doit contenir un tableau de sous-autorités SID.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

[**\_autorité d' \_ identificateur SID \_ ODJ**](odj-sid_identifier_authority.md)
