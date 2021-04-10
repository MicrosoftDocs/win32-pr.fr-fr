---
title: Publication des services COM+
description: Les services COM fournissent un proxy d’application sous la forme d’un package Windows Installer (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Publication des services COM+
- Active Directory, utilisation de, publication d’un service, services COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028596"
---
# <a name="publishing-com-services"></a>Publication des services COM+

Les services COM fournissent un proxy d’application sous la forme d’un package Windows Installer (MSI). Ce fichier. msi contient le nom du serveur à utiliser et d’autres éléments requis, tels que les proxy/stubs et les bibliothèques de types requis pour le marshaling. Le composant logiciel enfichable Services de composants génère automatiquement ces proxys d’application pour les applications serveur COM+.

Les proxys d’application sont publiés dans des objets de stratégie dans Active Directory à l’aide de l’éditeur de stratégie de groupe. Aucune intervention spéciale n’est nécessaire dans l’application cliente. Le compte d’ordinateur/utilisateur sur l’ordinateur client doit se trouver dans une unité d’organisation configurée pour utiliser l’objet de stratégie dans lequel les proxys d’application sont publiés. Le Binder COM localise automatiquement le serveur au moyen du répertoire lorsque le client établit une instance des objets concernés.

 

 




