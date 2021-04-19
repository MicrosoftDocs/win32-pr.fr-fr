---
title: ODJ_PROVISION_DATA
description: Définition du ODJ_PROVISION_DATA IDL
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "106510291"
---
# <a name="odj_provision_data-structure"></a>Structure ODJ_PROVISION_DATA

Spécifie la structure de sérialisation la plus à l’extérieur utilisée par les API de jonction de domaine hors connexion.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a>Membres

### <a name="ulversion"></a>ulVersion

La valeur doit être 1.

### <a name="ulcblobs"></a>ulcBlobs

Doit être défini sur le nombre d’éléments dans le tableau pBlobs.

### <a name="pblobs"></a>pBlobs

Pointe vers un tableau de structures de ODJ_BLOB.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

[**\_objet BLOB ODJ**](odj-odj_blob.md)


