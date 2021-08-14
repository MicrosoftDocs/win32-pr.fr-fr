---
description: la méthode Connecter de l’objet Merge peut être utilisée pour connecter un module à une fonctionnalité supplémentaire qui a été fusionnée dans la base de données ou qui sera fusionnée dans la base de données. La fonctionnalité doit exister avant d’appeler cette méthode.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Connexion d’un module de fusion à plusieurs fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12044ff293d825c160533907d625a2d12bb9ea217233c54dd9d5a0099990ee3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948420"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a>Connexion d’un module de fusion à plusieurs fonctionnalités

la méthode [**Connecter**](merge-connect.md) de l' [objet Merge](merge-object.md) peut être utilisée pour connecter un module à une fonctionnalité supplémentaire qui a été fusionnée dans la base de données ou qui sera fusionnée dans la base de données. La fonctionnalité doit exister avant d’appeler cette méthode.

Un module de fusion ne doit jamais remettre un composant contenant des fichiers système à la fonctionnalité principale d’une application, car cela peut entraîner la validation et la réparation de l’application par le programme d’installation chaque fois que le fichier système est utilisé. Un fichier de .msi destiné à accepter des composants d’un module de fusion doit être créé afin que tous les composants qui contiennent des fichiers système appartiennent uniquement à des fonctionnalités qui sont séparées de la fonctionnalité principale de l’application.

Si votre package utilise un module de fusion contenant des fichiers système qui lient tous les composants du module de fusion à la fonctionnalité principale de l’application, une tentative d’utilisation du fichier système peut déclencher le programme d’installation pour essayer de réparer la fonctionnalité principale de l’application. Si la fonctionnalité principale ne peut pas être réparée, l’installation peut échouer.

 

 



