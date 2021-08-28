---
title: ODJ_BLOB
description: Définition du ODJ_BLOB IDL
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: aa1c2b593e0e9f63a52672eb3b29ee83fbf86ea91d7f4860f2351a8e4538f05d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779569"
---
# <a name="odj_blob-structure"></a>Structure ODJ_BLOB

Spécifie une structure contenant soit une structure de ODJ_WIN7BLOB sérialisée, soit une structure de OP_PACKAGE sérialisée.

## <a name="syntax"></a>Syntaxe

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a>Membres

### <a name="ulodjformat"></a>ulODJFormat

Spécifie la version logique de la structure et doit être défini sur l’une des valeurs suivantes :

|Valeur|Signification|
| --- | --- |
|ODJ_WIN7_FORMAT (0x00000001)|Les octets contenus dans pBlob doivent contenir une structure ODJ_WIN7_BLOB sérialisée.|
|ODJ_WIN8_FORMAT (0x00000002)|Les octets contenus dans pBlob doivent contenir une structure OP_PACKAGE sérialisée.|

### <a name="cbblob"></a>cbBlob

Doit être défini sur le nombre d’octets dans le tableau pBlob.

### <a name="pblob"></a>pBlob

Pointe vers une mémoire tampon d’octets qui contient une structure sérialisée telle que spécifiée par ulODJFormat ci-dessus.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

