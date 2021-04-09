---
description: La méthode Connect de l’objet Merge peut être utilisée pour connecter un module à une fonctionnalité supplémentaire qui a été fusionnée dans la base de données ou qui sera fusionnée dans la base de données. La fonctionnalité doit exister avant d’appeler cette méthode.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Connexion d’un module de fusion à plusieurs fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57b49f1ee27b4c8d3aa5d0b3ac1b0d7b8b8e11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867045"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a>Connexion d’un module de fusion à plusieurs fonctionnalités

La méthode [**Connect**](merge-connect.md) de l' [objet Merge](merge-object.md) peut être utilisée pour connecter un module à une fonctionnalité supplémentaire qui a été fusionnée dans la base de données ou qui sera fusionnée dans la base de données. La fonctionnalité doit exister avant d’appeler cette méthode.

Un module de fusion ne doit jamais remettre un composant contenant des fichiers système à la fonctionnalité principale d’une application, car cela peut entraîner la validation et la réparation de l’application par le programme d’installation chaque fois que le fichier système est utilisé. Un fichier. msi destiné à accepter des composants d’un module de fusion doit être créé afin que tous les composants qui contiennent des fichiers système appartiennent uniquement à des fonctionnalités qui sont séparées de la fonctionnalité principale de l’application.

Si votre package utilise un module de fusion contenant des fichiers système qui lient tous les composants du module de fusion à la fonctionnalité principale de l’application, une tentative d’utilisation du fichier système peut déclencher le programme d’installation pour essayer de réparer la fonctionnalité principale de l’application. Si la fonctionnalité principale ne peut pas être réparée, l’installation peut échouer.

 

 



