---
title: Communication entre processus
description: Les techniques suivantes peuvent être utilisées pour la communication entre les applications 32 bits et 64 bits.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- communication entre processus, programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2398174f011127973dfd0b1773e6eb040cdde898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382342"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a>Communication entre processus entre les applications 32 bits et 64 bits

Les techniques suivantes peuvent être utilisées pour la communication entre les applications 32 bits et 64 bits :

-   les versions 64 bits de Windows utilisent des handles 32 bits pour l’interopérabilité. Lors du partage d’un handle entre des applications 32 bits et 64 bits, seuls les 32 bits inférieurs sont significatifs. il est donc plus sûr de tronquer le descripteur (lors de son passage d’un 64-bit à un bit 32) ou d’étendre le descripteur (lors de son passage de 32-bit à 64-bit). Les handles qui peuvent être partagés incluent des handles d’objets utilisateur tels que Windows (**HWND**), des handles vers des objets GDI tels que des stylets et des pinceaux (**HBRUSH** et **HPEN**), ainsi que des handles vers des objets nommés tels que les mutex, les sémaphores et les descripteurs de fichiers.
-   Les appels de procédure distante (RPC) peuvent être utilisés.
-   COM LocalServers peut être utilisé si les dll proxy/stub 32 bits et 64 bits sont inscrites pour toutes les interfaces utilisées.
-   La mémoire partagée peut être utilisée si les types dépendants du pointeur sont convertis correctement (ou évités).
-   Les fonctions [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) et [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) peuvent lancer des processus 32 bits et 64 bits à partir de processus 32 bits ou 64 bits, avec certaines limitations.

Un fichier exécutable 64 bits situé sous% windir% \\ system32 ne peut pas être lancé à partir d’un processus 32 bits, car le redirecteur du système de fichiers redirige le chemin d’accès. Ne désactivez pas la redirection pour effectuer cette opération. Utilisez à la place% windir% \\ SysNative. Pour plus d’informations, consultez [redirecteur de système de fichiers](file-system-redirector.md).

 

 