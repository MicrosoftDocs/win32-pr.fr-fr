---
title: commutateur/notlb
description: Le commutateur/notlb empêche le compilateur MIDL de générer un fichier de bibliothèque de types (TLB).
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- MIDL du commutateur/notlb
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e309ed753d1549c31c9e3dea0a5c7aa87b32217aa12e5ee04934a183927adf87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067519"
---
# <a name="notlb-switch"></a>commutateur/notlb

Le commutateur **/notlb** empêche le compilateur MIDL de générer un fichier de bibliothèque de types (TLB).

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Par défaut, le compilateur MIDL génère un fichier TLB chaque fois qu’il rencontre une instruction [**Library**](library.md) . Ce commutateur remplace le comportement par défaut.

Quand l’option **/notlb** est spécifiée, tous les autres stubs, en-têtes, etc. sont générés comme d’habitude.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/TLB**](-tlb.md)
</dt> </dl>

 

 




