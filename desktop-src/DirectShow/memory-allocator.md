---
description: Allocateur de mémoire
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Allocateur de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012167"
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

 

 



