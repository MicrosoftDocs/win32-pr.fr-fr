---
title: Architecture du gestionnaire
description: Architecture du gestionnaire
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0da7846f31c94202d8d50ac0566c87ef5db085a0b9efb3f9250468346512db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141092"
---
# <a name="handler-architecture"></a>Architecture du gestionnaire

La fonction interne d’un fichier ou d’un gestionnaire de flux est définie par le gestionnaire lui-même. Pour une application, un gestionnaire de fichiers apparaît généralement sous la forme d’un module permettant de lire et d’écrire des fichiers AVI. De même, un gestionnaire de flux apparaît en tant que module pour lire et écrire un type spécifique de flux de données. L’interface de flux cohérent rend non importante la source et la destination du flux pour l’application qui utilise le gestionnaire.

Un gestionnaire de fichiers permet d’accéder à une source de données composée d’un ou de plusieurs flux de données. Les gestionnaires de fichiers fournissent généralement un accès aux fichiers de disque contenant un ou plusieurs flux de données, et les fonctions internes du gestionnaire de fichiers lisent et écrivent les données multimédias. Toutefois, les gestionnaires de fichiers peuvent fonctionner avec n’importe quelle source de données, par exemple un canal de transmission numérique contenant plusieurs flux de données mélangés.

En revanche, un gestionnaire de flux traite un type de données et apparaît comme un flux de données pour une application. Un gestionnaire de flux peut fournir des données qu’il fabrique ou peut récupérer des données à partir d’un fichier ou d’une source externe. Il fournit ses données dans un format que votre application peut utiliser.

 

 




