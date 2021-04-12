---
description: Le mode d’erreur indique au système Comment l’application va répondre aux erreurs graves.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Mode d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75238e7ee64f40950c3df3aba36d28d95c953267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109978"
---
# <a name="error-mode"></a>Mode d’erreur

Le mode d’erreur indique au système Comment l’application va répondre aux erreurs graves. Les erreurs graves incluent les défaillances de disque, les erreurs de lecteur non prêt, le mauvais alignement des données et les exceptions non gérées. Ce mode d’erreur peut être géré par thread ou par processus. Une application peut permettre au système d’afficher une boîte de message informant l’utilisateur qu’une erreur s’est produite, ou peut gérer les erreurs.

Pour gérer ces erreurs sans intervention de l’utilisateur, utilisez [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) ou le [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)spécifique au thread. Après l’appel de l’une de ces fonctions et la spécification des indicateurs appropriés, le système n’affichera pas les boîtes de message d’erreur correspondantes.

Un processus peut récupérer son mode d’erreur à l’aide de [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) ou [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).

La meilleure pratique est que toutes les applications appellent la fonction [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) à l’ensemble du processus avec un paramètre de **SEM \_ FAILCRITICALERRORS** au démarrage. Cela permet d’empêcher les boîtes de dialogue du mode d’erreur de suspendre l’application.

À part cela, les appelants doivent privilégier les versions spécifiques aux threads de ces fonctions, car elles sont moins perturbatrices pour le comportement normal du système.

 

 
