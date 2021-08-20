---
title: SID_IDENTIFIER_AUTHORITY
description: Définition du SID_IDENTIFIER_AUTHORITY IDL
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 8d2ac3b8763026c0aea31214169ff8a0e2c6260086456c8c7c2431f69b13b2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796877"
---
# <a name="sid_identifier_authority-structure"></a>Structure SID_IDENTIFIER_AUTHORITY

Contient une autorité d’identificateur de SID.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a>Membres

### <a name="value"></a>Valeur

Doit être défini sur les six octets de l’autorité d’identificateur SID.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)