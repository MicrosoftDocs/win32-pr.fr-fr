---
title: commutateur/Win64
description: Le commutateur/Win64 indique au compilateur MIDL de générer des fichiers stub, ou un fichier bibliothèque de types, pour un environnement 64 bits. Notez que ce commutateur est obsolète.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- MIDL du commutateur/Win64
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 963510db9f170a890797ebd3fffee4af9c270616b5d92b2a2333a47850311c30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913629"
---
# <a name="win64-switch"></a>commutateur/Win64

Le commutateur **/Win64** indique au compilateur MIDL de générer des fichiers stub, ou un fichier bibliothèque de types, pour un environnement 64 bits.

> [!Note]  
> Ce commutateur est obsolète. Utilisez le commutateur [**/ia64**](-ia64.md) ou [**/amd64**](-amd64.md) à la place. Le commutateur **/Win64** est équivalent au commutateur **/ia64** .

 

``` syntax
midl /win64
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Le commutateur **/Win64** revient à définir le commutateur [**/env**](-env.md) sur Win64.

> [!Note]  
> il n’est pas possible d’utiliser MIDL.exe pour produire un tlb 64 bits sur Windows 2000.

 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/env**](-env.md)
</dt> <dt>

[**/ia64**](-ia64.md)
</dt> <dt>

[**/amd64**](-amd64.md)
</dt> </dl>

 

 




