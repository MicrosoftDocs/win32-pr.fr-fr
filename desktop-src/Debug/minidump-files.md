---
description: Les applications peuvent produire des fichiers Minidump en mode utilisateur, qui contiennent un sous-ensemble utile des informations contenues dans un fichier de vidage sur incident.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Fichiers minidump
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412e719d54f34c9766981667be35990c37ae3511eaecc8836ceac0311a5105e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406089"
---
# <a name="minidump-files"></a>Fichiers minidump

Les applications peuvent produire des fichiers Minidump en mode utilisateur, qui contiennent un sous-ensemble utile des informations contenues dans un fichier de vidage sur incident. Les applications peuvent créer des fichiers Minidump très rapidement et efficacement. Étant donné que les fichiers Minidump sont peu volumineux, ils peuvent être facilement envoyés via Internet au support technique de l’application.

Un fichier Minidump ne contient pas autant d’informations qu’un fichier de vidage sur incident complet, mais il contient suffisamment d’informations pour effectuer des opérations de débogage de base. Pour lire un fichier minidump, les fichiers binaires et les fichiers de symboles doivent être disponibles pour le débogueur.

les versions actuelles de Microsoft Office et Microsoft Windows créer des fichiers minidump pour l’analyse des défaillances sur les ordinateurs des clients.

Les fonctions DbgHelp suivantes sont utilisées avec les fichiers minidump.

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**Entrée**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



