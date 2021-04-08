---
title: Chargement d’un caractère
description: Chargement d’un caractère
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673118"
---
# <a name="loading-a-character"></a>Chargement d’un caractère

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Pour animer un caractère, vous devez d’abord charger le caractère. Utilisez la méthode [**Load**](load-method.md) pour charger les données du caractère. Microsoft agent prend en charge deux formats de données de caractères et d’animation : un seul fichier structuré et des fichiers distincts. En général, vous utilisez le format de fichier unique (. ACS) lorsque les données sont stockées localement. Le format de fichier multiple (. ACF,. CCN) fonctionne mieux lorsque vous souhaitez télécharger des animations individuellement, par exemple lors de l’accès à des animations à partir d’un serveur HTTP.

Une application cliente ne peut charger qu’une seule instance du même caractère. Toute tentative de chargement du même caractère plusieurs fois échoue. Toutefois, une application peut avoir plusieurs instances du même caractère chargées en fournissant des connexions distinctes à Microsoft Agent. Par exemple, une application peut charger le même caractère à partir de deux copies du contrôle Microsoft Agent.

Vous pouvez également définir vos propres caractères en vue de les utiliser avec Microsoft Agent. Vous pouvez utiliser n’importe quel outil de rendu que vous préférez créer les images, à condition de vous retrouver avec les fichiers de format bitmap Windows. Pour assembler et compiler les images d’un caractère dans des animations en vue de les utiliser avec Microsoft Agent, utilisez l’éditeur de caractères Microsoft Agent. Cet outil vous permet de définir les propriétés par défaut d’un caractère et de définir des animations pour ce caractère. L’éditeur de caractères Microsoft agent vous permet également de sélectionner le format de fichier approprié lorsque vous créez un caractère.

 

 




