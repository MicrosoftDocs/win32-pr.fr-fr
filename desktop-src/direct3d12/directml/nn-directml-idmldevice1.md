---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Représente un appareil DirectML, utilisé pour créer des opérateurs, des tables de liaison, des enregistreurs de commande et d’autres objets.
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: 7a10cf2c9fe683775d163c7b5cb0e30fe07de08f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417177"
---
# <a name="idmldevice1-interface-directmlh"></a>Interface IDMLDevice1 (directml. h)

Représente un appareil DirectML, utilisé pour créer des opérateurs, des tables de liaison, des enregistreurs de commande et d’autres objets. L’interface **IDMLDevice1** hérite de [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).

Un appareil DirectML est toujours associé à un seul appareil Direct3D 12 sous-jacent. Tous les objets créés par l’appareil DirectML conservent une référence forte à leur périphérique parent. Contrairement à l’appareil Direct3D 12, l’appareil DML n’est pas un singleton. Par conséquent, il est possible de créer plusieurs appareils DirectML sur le même appareil Direct3D 12. Toutefois, cela n’est pas recommandé, car l’appareil DirectML n’a pas d’État mutable, donc il n’y a pas d’avantage à créer plusieurs appareils DML sur le même appareil Direct3D 12.

Cet objet est thread-safe.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="availability"></a>Disponibilité
Cette API a été introduite dans la version DirectML `1.1.0` .

## <a name="tensor-constraints"></a>Contraintes tenseur
**Plateforme cible**: Windows


## <a name="inheritance"></a>Héritage


L’interface IDMLDevice1 hérite de l’interface IDMLDevice.



## <a name="methods"></a>Méthodes

<p>L’interface <b>IDMLDevice1</b> possède ces méthodes.</p>

| Méthode | Description |
| ---- |:---- |
| [IDMLDevice1::CompileGraph](../directml/nf-directml-idmldevice1-compilegraph.md) | Compile un graphique d’opérateurs DirectML dans un objet qui peut être distribué au GPU. |


## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plateforme cible** | Windows |
| **En-tête** | directml. h |

## <a name="see-also"></a>Voir aussi

[Interface IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)