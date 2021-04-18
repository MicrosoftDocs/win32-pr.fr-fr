---
description: Allocateur de mémoire
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Allocateur de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522204"
---
# <a name="memory-allocator"></a>Allocateur de mémoire

L’objet allocateur de mémoire alloue des tampons pour les exemples de supports. Les filtres peuvent utiliser cet objet pour allouer des mémoires tampons de mémoire partagées ; Toutefois, un filtre avec des exigences spéciales peut également implémenter son propre objet allocateur de mémoire. Créez cet objet en appelant **CoCreateInstance**.



|                  |                                        |
|------------------|----------------------------------------|
| Identificateur de classe | CLSID \_ MemoryAllocator                 |
| Interfaces       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets DirectShow](directshow-objects.md)
</dt> </dl>

 

 



