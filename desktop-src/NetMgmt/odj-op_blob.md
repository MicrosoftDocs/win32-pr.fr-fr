---
title: OP_BLOB
description: Définition du OP_BLOB IDL
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 757df1549d1bdb0a9a87ee22373a1903a034a1e267d087d51dac46bb6bc5a762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796889"
---
# <a name="op_blob-structure"></a>Structure OP_BLOB

Contient une mémoire tampon d’octets opaque.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a>Membres

### <a name="cbblob"></a>cbBlob

Spécifie la taille de pBlob en octets.

### <a name="pblob"></a>pBlob

Pointe vers une mémoire tampon d’octets.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)
