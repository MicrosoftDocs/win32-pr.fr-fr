---
title: Débogage des allocations de mémoire
description: Débogage des allocations de mémoire
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b3376b2ffee17ce747197eb57fecbdae18e086d5252dd5f4721975181885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993449"
---
# <a name="debugging-memory-allocations"></a>Débogage des allocations de mémoire

COM fournit l’interface [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) que les développeurs peuvent utiliser pour déboguer leurs allocations de mémoire. Pour chaque méthode dans [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), il existe deux méthodes dans **IMallocSpy**, une méthode « pre » et une méthode « poster ». Une fois qu’un développeur l’a implémenté et le publie sur le système, le système appelle la méthode « pre » **IMallocSpy** juste avant la méthode **IMalloc** correspondante, ce qui permet au code de débogage d’être « Spy » sur l’opération d’allocation et appelle la méthode « poster » pour libérer l’espion.

Par exemple, lorsque COM détecte que l’appel suivant est un appel à [**IMalloc :: Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), il appelle [**IMallocSpy ::P realloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), en exécutant les opérations de débogage que le développeur souhaite au cours de l’exécution de l' **allocation** , puis, lorsque l’appel **alloc** est retourné, appelle [**IMallocSpy ::P ostalloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) pour libérer l’espion et retourner le contrôle au code.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de l’allocation de mémoire](managing-memory-allocation.md)
</dt> </dl>

 

 