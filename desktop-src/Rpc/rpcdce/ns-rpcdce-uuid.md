---
title: UUID
description: Fournit une désignation unique d’un objet tel qu’une interface, un vecteur de point d’entrée de gestionnaire ou un objet client.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 95d2d420502a5d92af64c902ffa82c709639d872
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101061"
---
# <a name="uuid-structure"></a>UUID, structure

La structure **UUID** définit un identificateur unique universel (UUID). Un **UUID** fournit une désignation unique d’un objet tel qu’une interface, un vecteur de point d’entrée de gestionnaire ou un objet client.

La structure **UUID** est un `typedef` synonyme de la structure [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) .

## <a name="syntax"></a>Syntaxe

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>Notes

Les bibliothèques Runtime RPC utilisent des **UUID** pour vérifier la compatibilité entre les clients et les serveurs, et pour effectuer une sélection parmi plusieurs implémentations d’une interface.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | Défini dans rpcdce. h ; inclure RPC. h |

## <a name="see-also"></a>Voir aussi

[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ VECTEUR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)