---
title: Accès aux pointeurs opaques
description: Les clients sont en mesure d’accéder aux informations stockées dans les destinations à l’aide de pointeurs opaques.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507307"
---
# <a name="accessing-opaque-pointers"></a>Accès aux pointeurs opaques

Les clients sont en mesure d’accéder aux informations stockées dans les destinations à l’aide de pointeurs opaques. Pour utiliser le stockage, le client doit d’abord appeler [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) pour obtenir le pointeur. Chaque fois qu’une modification apportée aux informations est nécessaire, le client doit d’abord verrouiller la destination en appelant [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) avec le paramètre *LockDest* défini sur **true**. Une fois que la destination est verrouillée, le client peut apporter les modifications nécessaires. La destination peut être déverrouillée à l’aide d’un autre appel à **RtmLockDestination** avec le paramètre *LockDest* défini sur **false**.

La fonction [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) permet également à un client d’utiliser un verrou de lecture ou un verrou d’écriture, à l’aide du paramètre *exclusive* . Un client doit utiliser le verrou d’écriture uniquement lorsqu’il apporte des modifications aux informations conservées à l’aide du pointeur opaque. Les clients peuvent utiliser le verrou en lecture pour afficher les informations de pointeur opaques stockées dans une destination.

Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [accéder au pointeur opaque dans une destination](access-the-opaque-pointer-in-a-destination.md).

 

 




