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
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462570"
---
# <a name="notlb-switch"></a>commutateur/notlb

Le commutateur **/notlb** empêche le compilateur MIDL de générer un fichier de bibliothèque de types (TLB).

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Par défaut, le compilateur MIDL génère un fichier TLB chaque fois qu’il rencontre une instruction [**Library**](library.md) . Ce commutateur remplace le comportement par défaut.

Quand l’option **/notlb** est spécifiée, tous les autres stubs, en-têtes, etc. sont générés comme d’habitude.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/TLB**](-tlb.md)
</dt> </dl>

 

 




