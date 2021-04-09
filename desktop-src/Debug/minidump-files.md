---
description: Les applications peuvent produire des fichiers Minidump en mode utilisateur, qui contiennent un sous-ensemble utile des informations contenues dans un fichier de vidage sur incident.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Fichiers minidump
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fcd57611cd0b6e5f4f5abdf8bc535f8222feb7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110207"
---
# <a name="minidump-files"></a>Fichiers minidump

Les applications peuvent produire des fichiers Minidump en mode utilisateur, qui contiennent un sous-ensemble utile des informations contenues dans un fichier de vidage sur incident. Les applications peuvent créer des fichiers Minidump très rapidement et efficacement. Étant donné que les fichiers Minidump sont peu volumineux, ils peuvent être facilement envoyés via Internet au support technique de l’application.

Un fichier Minidump ne contient pas autant d’informations qu’un fichier de vidage sur incident complet, mais il contient suffisamment d’informations pour effectuer des opérations de débogage de base. Pour lire un fichier minidump, les fichiers binaires et les fichiers de symboles doivent être disponibles pour le débogueur.

Les versions actuelles de Microsoft Office et Microsoft Windows créent des fichiers minidump pour l’analyse des défaillances sur les ordinateurs des clients.

Les fonctions DbgHelp suivantes sont utilisées avec les fichiers minidump.

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**Entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



