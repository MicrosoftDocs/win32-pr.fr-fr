---
title: Interopérabilité des processus
description: vous pouvez exécuter des applications Win32 sur les Windows 64 bits à l’aide d’une couche d’émulation. Windows 10 sur ARM comprend une couche d’émulation x86-on-ARM64. Pour plus d’informations, consultez exécution d’applications 32 bits.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- interopérabilité des processus 64 bits Windows programmation
- interopérabilité 64-programmation de Windows bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74e75af4299e9c249ea46b8eac2cdd47de10eb3f832aa88d6b313d20304afc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561515"
---
# <a name="process-interoperability"></a>Interopérabilité des processus

vous pouvez exécuter des applications Win32 sur les Windows 64 bits à l’aide d’une couche d’émulation. Windows 10 sur ARM comprend une couche d’émulation x86-on-ARM64. Pour plus d’informations, consultez [exécution d’Applications 32 bits](running-32-bit-applications.md).

sur les Windowss 64 bits, un processus 64 bits ne peut pas charger une bibliothèque de liens dynamiques (DLL) 32 bits. En outre, un processus 32 bits ne peut pas charger une DLL 64 bits. toutefois, 64 bits Windows prend en charge les appels de procédure distante (RPC) entre les processus 64 bits et 32 bits (sur le même ordinateur et sur plusieurs ordinateurs). sur les Windowss 64 bits, un serveur com hors processus 32 bits peut communiquer avec un client 64 bits, et un serveur com hors processus de 64 bits peut communiquer avec un client 32-bit. Par conséquent, si vous avez une DLL 32 bits qui ne prend pas en charge COM, vous pouvez la placer dans un wrapper dans un serveur COM hors processus et utiliser COM pour marshaler les appels vers et à partir d’un processus 64 bits.

Les serveurs in-process sont actuellement inscrits à l’aide de l’entrée de Registre **InprocServer** . sur les Windows 64 bits, les serveurs in-process 64 et 32 bits doivent utiliser l’entrée **InprocServer32** .

Pour les descripteurs de port qui, par leur nature, sont locaux sur l’ordinateur et ne seraient jamais utilisés sur la limite 32 bits à 64 bits, utilisez le type de pointeur de **handle \_** à la place du type PTR **int \_** ou **DWORD \_** . Cela comprend le portage des interfaces RPC qui passent des handles comme valeurs **DWORD** . Le pointeur de **HANDLE 64 \_** bits est 64 bits sur le câble (non tronqué) et n’a donc pas besoin d’être mappé. (Le pointeur de **HANDLE 32 \_** bits est 32 bits sur le câble.)

Pour plus d’informations, consultez [conception d’interfaces compatibles avec 64 bits](designing-64-bit-compatible-interfaces.md).

 

 




