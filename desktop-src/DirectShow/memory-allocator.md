---
description: Allocateur de mémoire
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Allocateur de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9346cf35e9383ff79e3dc5dafe54c0857a3f6f8818d9d137ae92bd1e6f98977d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584149"
---
# <a name="memory-allocator"></a>Allocateur de mémoire

L’objet allocateur de mémoire alloue des tampons pour les exemples de supports. Les filtres peuvent utiliser cet objet pour allouer des mémoires tampons de mémoire partagées ; Toutefois, un filtre avec des exigences spéciales peut également implémenter son propre objet allocateur de mémoire. Créez cet objet en appelant **CoCreateInstance**.



| Étiquette | Valeur |
|------------------|----------------------------------------|
| Identificateur de classe | CLSID \_ MemoryAllocator                 |
| Interfaces       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Objets](directshow-objects.md)
</dt> </dl>

 

 



