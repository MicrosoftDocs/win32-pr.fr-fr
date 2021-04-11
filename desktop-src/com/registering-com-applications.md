---
title: Inscription des applications COM
description: Inscription des applications COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310945"
---
# <a name="registering-com-applications"></a>Inscription des applications COM

Le Registre est une base de données système qui contient des informations sur la configuration du matériel et des logiciels du système, ainsi que sur les utilisateurs du système. N’importe quel programme Windows peut ajouter des informations au registre et lire des informations à partir du Registre. Les clients recherchent dans le registre des composants intéressants à utiliser.

Le registre contient des informations sur tous les objets COM installés dans le système. Chaque fois qu’une application crée une instance d’un composant COM, le Registre est consulté pour résoudre le CLSID ou le ProgID du composant dans le chemin d’accès de la DLL du serveur ou de l’EXE qui le contient. Une fois le serveur du composant déterminé, Windows charge le serveur dans l’espace de processus de l’application cliente (composants in-process) ou démarre le serveur dans son propre espace de processus (serveurs locaux et distants). Le serveur crée une instance du composant et retourne au client une référence à l’une des interfaces du composant.

Pour plus d’informations sur le Registre Windows, consultez les rubriques suivantes :

-   [Hiérarchie du Registre](registry-hierarchy.md)
-   [Classes et serveurs](classes-and-servers.md)
-   [Classification des composants](classifying-components.md)
-   [Utilisation d’OleView](using-oleview.md)
-   [Inscription des composants](registering-components.md)
-   [Vérification de l’inscription](checking-registration.md)
-   [Types d’utilisateurs inconnus](unknown-user-types.md)
-   [Clés de registre COM](com-registry-keys.md)

 

 




