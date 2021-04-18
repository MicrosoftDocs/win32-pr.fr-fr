---
title: Interopérabilité des processus
description: Vous pouvez exécuter des applications Win32 sur Windows 64 bits à l’aide d’une couche d’émulation. Windows 10 sur ARM comprend une couche d’émulation x86-on-ARM64. Pour plus d’informations, consultez exécution d’applications 32 bits.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- interopérabilité des processus 64-programmation Windows bits
- interopérabilité de la programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023be0dafabfa8b17cf460542ae06467db517c11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512256"
---
# <a name="process-interoperability"></a>Interopérabilité des processus

Vous pouvez exécuter des applications Win32 sur Windows 64 bits à l’aide d’une couche d’émulation. Windows 10 sur ARM comprend une couche d’émulation x86-on-ARM64. Pour plus d’informations, consultez [exécution d’Applications 32 bits](running-32-bit-applications.md).

Sur Windows 64 bits, un processus 64 bits ne peut pas charger une bibliothèque de liens dynamiques (DLL) 32 bits. En outre, un processus 32 bits ne peut pas charger une DLL 64 bits. Toutefois, Windows 64 bits prend en charge les appels de procédure distante (RPC) entre les processus 64 bits et 32 bits (sur le même ordinateur et sur plusieurs ordinateurs). Sur Windows 64 bits, un serveur COM hors processus de 32 bits peut communiquer avec un client 64 bits, et un serveur COM hors processus de 64 bits peut communiquer avec un client 32-bit Server. Par conséquent, si vous avez une DLL 32 bits qui ne prend pas en charge COM, vous pouvez la placer dans un wrapper dans un serveur COM hors processus et utiliser COM pour marshaler les appels vers et à partir d’un processus 64 bits.

Les serveurs in-process sont actuellement inscrits à l’aide de l’entrée de Registre **InprocServer** . Sur les serveurs Windows 64 bits, les serveurs in-process 64 et 32 bits doivent utiliser l’entrée **InprocServer32** .

Pour les descripteurs de port qui, par leur nature, sont locaux sur l’ordinateur et ne seraient jamais utilisés sur la limite 32 bits à 64 bits, utilisez le type de pointeur de **handle \_** à la place du type PTR **int \_** ou **DWORD \_** . Cela comprend le portage des interfaces RPC qui passent des handles comme valeurs **DWORD** . Le pointeur de **HANDLE 64 \_** bits est 64 bits sur le câble (non tronqué) et n’a donc pas besoin d’être mappé. (Le pointeur de **HANDLE 32 \_** bits est 32 bits sur le câble.)

Pour plus d’informations, consultez [conception d’interfaces compatibles avec 64 bits](designing-64-bit-compatible-interfaces.md).

 

 




