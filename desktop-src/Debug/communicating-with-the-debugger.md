---
description: La fonction OutputDebugString envoie une chaîne à partir du processus en cours de débogage vers le débogueur en générant un \_ \_ événement de débogage d’événement de chaîne de débogage de sortie \_ . Un processus peut déterminer s’il est en cours de débogage en appelant la fonction IsDebuggerPresent.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Communication avec le débogueur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846949"
---
# <a name="communicating-with-the-debugger"></a>Communication avec le débogueur

La fonction [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) envoie une chaîne à partir du processus en cours de débogage vers le débogueur en générant un \_ événement de \_ débogage d’événement de chaîne de débogage de sortie \_ . Un processus peut déterminer s’il est en cours de débogage en appelant la fonction [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .

La fonction [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) provoque une exception de point d’arrêt dans le processus en cours. Un point d’arrêt est un emplacement dans un programme où l’exécution est arrêtée pour permettre au développeur d’examiner le code, les variables et les valeurs de Registre du programme et, si nécessaire, d’effectuer des modifications, de poursuivre l’exécution ou de terminer l’exécution.

La fonction [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) met fin au processus en cours et donne le contrôle d’exécution au débogueur, mais contrairement à [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), il ne génère pas d’exception. Cette fonction ne doit être utilisée qu’en dernier recours, car elle ne libère pas toujours la mémoire du processus et ne ferme pas ses fichiers.

 

 
