---
title: Erreurs d’alignement
description: Erreurs d’alignement
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- erreurs d’alignement 64 bits Windows programmation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d813a47cb3428c57ee6235442491f26f8d126a997dd7fcfa6844d551e7958b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412909"
---
# <a name="alignment-faults"></a>Erreurs d’alignement

Le gestionnaire d’erreurs d’alignement système est désactivé par défaut sur les systèmes basés sur Itanium. Par conséquent, tout accès aux données non alignées génère une exception qui ne sera pas automatiquement corrigée par le système, à moins que l’application n’intercepte l’exception dans un [Gestionnaire d’exceptions basé sur des frames](/windows/desktop/Debug/frame-based-exception-handling). Pour activer le gestionnaire d’erreurs d’alignement du système, appelez la fonction [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) avec **SEM \_ NOALIGNMENTFAULTEXCEPT**. Toutefois, Notez que les processus peuvent subir une dégradation importante des performances si le gestionnaire d’erreurs d’alignement du système est activé et que le processus génère des erreurs d’alignement.

Si le débogueur WinDbg a été installé en tant que débogueur système, WinDbg est lancé automatiquement si un processus sur le système génère une exception non gérée. Si un débogueur n’est pas installé en tant que débogueur système, le système affiche une boîte de dialogue indiquant que votre application a rencontré une erreur et a fourni la possibilité de signaler le problème à Microsoft.

Sur les systèmes x64 et ARM64, les erreurs d’alignement sont gérées par une combinaison de matériel et de logiciels. Pour des performances optimales, tout accès à la mémoire doit être correctement aligné. En outre, [l’accès aux variables bloquées](/windows/desktop/Sync/interlocked-variable-access) non alignées doit être évité sur ARM64, car ces opérations ne sont pas atomiques.

 

 