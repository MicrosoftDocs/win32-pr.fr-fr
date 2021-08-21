---
title: Publication des services COM+
description: les services COM fournissent un proxy d’application sous la forme d’un package Windows installer (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Publication des services COM+
- Active Directory, utilisation de, publication d’un service, services COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91801bbfcbf8efa34ac0b79477dd9d859fc2ed34a8d40bcf0bd829f82cfd571a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025427"
---
# <a name="publishing-com-services"></a>Publication des services COM+

les services COM fournissent un proxy d’application sous la forme d’un package Windows installer (MSI). Ce fichier .msi contient le nom du serveur à utiliser et d’autres éléments requis, tels que les proxy/stubs et les bibliothèques de types requis pour le marshaling. Le composant logiciel enfichable Services de composants génère automatiquement ces proxys d’application pour les applications serveur COM+.

Les proxys d’application sont publiés dans des objets de stratégie dans Active Directory à l’aide de l’éditeur de stratégie de groupe. Aucune intervention spéciale n’est nécessaire dans l’application cliente. Le compte d’ordinateur/utilisateur sur l’ordinateur client doit se trouver dans une unité d’organisation configurée pour utiliser l’objet de stratégie dans lequel les proxys d’application sont publiés. Le Binder COM localise automatiquement le serveur au moyen du répertoire lorsque le client établit une instance des objets concernés.

 

 




