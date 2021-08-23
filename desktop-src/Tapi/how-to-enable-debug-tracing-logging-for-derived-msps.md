---
description: La procédure suivante décrit comment activer le suivi et la journalisation du débogage.
ms.assetid: 52381397-df75-4d81-a048-f0ed408ac6b8
title: Comment activer le suivi et la journalisation du débogage pour les MSP dérivés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565b66055a43edbe7556e640f8e368aab84fab206bced431c22578a7e21a94ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140522"
---
# <a name="how-to-enable-debug-tracinglogging-for-derived-msps"></a>Comment activer le suivi et la journalisation du débogage pour les MSP dérivés

Tout d’abord, assurez-vous que l’implémentation du MSP dérivé a suivi les instructions de la section précédente en ce qui concerne le suivi du débogage (définition du symbole de préprocesseur MSPLOG, l’inscription pour le suivi pendant DllMain et l’utilisation de la macro LOG pour le suivi). Déterminez le nom que le MSP utilise lors de l’inscription pour le suivi (il s’agit généralement du nom de la DLL ; il est appelé « nom de la dll » ci-dessous &lt; &gt; ). Pour activer le suivi, utilisez un éditeur du Registre (« Regedit.exe » ou « Regedt32.exe ») pour rechercher la clé « HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Tracing » et procédez comme suit. Notez que toutes les valeurs mentionnées ci-dessous, à l’exception de la valeur EnableDebuggerTracing, doivent être créées automatiquement après l’exécution de votre MSP pour la première fois.

-   Pour activer le traçage vers les débogueurs en mode utilisateur et en mode noyau, affectez la valeur 1 à la valeur **DWORD** <dll name> \\ EnableDebuggerTracing. Si vous le souhaitez, utilisez la valeur **DWORD** <dll name> \\ ConsoleTracing mask pour activer ou désactiver divers niveaux de sortie de trace (la valeur par défaut est 0xFFFF0000, qui active tous les niveaux de suivi).
-   Pour activer le suivi d’un fichier, affectez la valeur 1 à la valeur **DWORD** <dll name> \\ EnableFileTracing. Si vous le souhaitez, utilisez la valeur <dll name> \\ de chaîne répertoirefichiers pour ajuster l’emplacement du fichier journal. Si vous le souhaitez, utilisez la valeur **DWORD** <dll name> \\ FileTracingMask pour activer ou désactiver divers niveaux de sortie de trace (la valeur par défaut est 0xFFFF0000, qui active tous les niveaux de suivi).
-   Pour activer le traçage vers une fenêtre de console distincte, en les séparant par une DLL, définissez la valeur **DWORD** EnableConsoleTracing sur 1, et définissez également la valeur **DWORD** <dll name> \\ EnableConsoleTracing sur 1. Si vous le souhaitez, utilisez la valeur **DWORD** <dll name> \\ ConsoleTracing mask pour activer ou désactiver divers niveaux de sortie de trace (la valeur par défaut est 0xFFFF0000, qui active tous les niveaux de suivi).

 

 



