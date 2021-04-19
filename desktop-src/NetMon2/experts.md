---
description: Un expert est une bibliothèque de liens dynamiques (DLL) Microsoft Win32 qui analyse le trafic réseau collecté par un fournisseur de paquets réseau (NPP) et placé dans un fichier de capture.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf5fc0096b15d590bf70859443667f2d9969f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538841"
---
# <a name="expert"></a>Expert

Un expert est une bibliothèque de liens dynamiques (DLL) Microsoft Win32 qui analyse le trafic réseau collecté par un [*fournisseur de paquets réseau*](n.md) (NPP) et placé dans un fichier de capture. Une fois les données capturées et stockées dans un fichier de capture, l’expert travaille avec un analyseur, également appelé analyseur de protocole, pour analyser les données contenues dans le fichier. Par exemple, vous pouvez examiner les frames du fichier de capture et utiliser un [*analyseur*](p.md) pour reconnaître des protocoles tels que le protocole SMB (Server Message Block) ou le protocole TCP/IP (Transmission Control Protocol/Internet Protocol).

Vous pouvez concevoir un expert pour travailler avec tous les analyseurs de Moniteur réseau et tous les analyseurs que vous créez vous-même.

Une fois que la correspondance de protocoles demandée identifie un frame spécifique, l’expert extrait des données du frame. Vous pouvez programmer l’expert pour manipuler des informations dans des données utilisables que l’Moniteur réseau observateur d’événements affiche.

Vous pouvez configurer un expert au moment de l’exécution, puis utiliser Moniteur réseau pour enregistrer les données de configuration utilisateur en vue de les réutiliser avec différents fichiers de capture. Vous pouvez utiliser un expert pour fournir des données de corrélation et des résolutions personnalisées pour les utilisateurs finaux. Pour plus d’informations sur la création d’informations de configuration HTML, consultez la [page de référence des événements](event-reference-page.md).

Pendant l’installation de Moniteur réseau, les dll d’experts suivantes sont installées dans le sous-répertoire experts :

-   Coalesce.dll
-   Propdist.dll
-   Protdist.dll
-   Resptime.dll
-   Tcpipe.dll
-   Topuser.dll

Lorsque vous démarrez Moniteur réseau, la fonction [**DllMain**](dllmain-expert.md) crée tous les experts dans le sous-répertoire experts. Lorsque l’utilisateur sélectionne **experts** dans le menu **Outils** de l’interface utilisateur Moniteur réseau, moniteur réseau charge les dll d’experts. L’expert est appelé via le point d’entrée de l' [expert Register](register-expert.md) pour fournir des informations de base sur l’expert.

![boîte de dialogue experts du moniteur réseau](images/expick.png)

Moniteur réseau appelle les fonctions suivantes pour gérer l’expert :

-   [**DllMain**](dllmain-expert.md)
-   [**Inscrire un expert**](register-expert.md)
-   [**Utilisez**](run.md)
-   [**Configurer**](configure.md)

L’expert doit implémenter chacune des fonctions précédentes.

 

 



