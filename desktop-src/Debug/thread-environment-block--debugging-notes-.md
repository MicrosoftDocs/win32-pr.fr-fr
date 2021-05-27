---
description: Bloc d’environnement de thread (remarques sur le débogage)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloc d’environnement de thread (remarques sur le débogage)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9397c2d442b09b308c4886c2672e3be58b661c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550584"
---
# <a name="thread-environment-block-debugging-notes"></a>Bloc d’environnement de thread (remarques sur le débogage)

Le bloc d’environnement de thread ([**structure TEB**](/windows/win32/api/winternl/ns-winternl-teb)) contient des informations de contexte pour un thread.

Dans les versions suivantes de Windows, le décalage de l’adresse TEB bits 32 dans le TEB 64 bits est 0. Cela peut être utilisé pour accéder directement au TEB bits 32 d’un thread WOW64. Cela peut changer dans les versions ultérieures de Windows



|  Plate-forme     | Version                |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | Windows Server 2012 R2 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Structures de débogage](debugging-structures.md)
</dt> <dt>

[**\_Contexte WOW64**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
