---
title: OP_PACKAGE
description: Définition du OP_PACKAGE IDL
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81fdc237b731489f7ac501a4e053e62d744b0fdef77c5b630cd478dede5aeda5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911489"
---
# <a name="op_package-structure"></a>Structure OP_PACKAGE

Contient une structure qui contient un OP_PACKAGE_COLLECTION sérialisé.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a>Membres

### <a name="encryptiontype"></a>EncryptionType

Réservé pour une utilisation ultérieure et doit être défini sur GUID_NULL.

### <a name="encryptioncontext"></a>EncryptionContext

Réservé pour une utilisation ultérieure et doit être défini sur tous les zéros.

### <a name="wrappedpartcollection"></a>WrappedPartCollection

Structure OP_BLOB qui contient une structure OP_PACKAGE_COLLECTION sérialisée.

### <a name="cbdecryptedpartcollection"></a>cbDecryptedPartCollection

Réservé pour une utilisation ultérieure et doit être défini à zéro.

### <a name="extension"></a>Extension

Réservé pour une utilisation ultérieure et doit être défini sur tous les zéros.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

[**\_objet BLOB op**](odj-op_blob.md)

[**\_collection de packages op \_**](odj-op_package_collection.md)
