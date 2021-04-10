---
description: Les assemblys privés côte à côte peuvent être utilisés pour créer des composants qui peuvent être facilement mis à jour sans mettre à jour également l’application d’hébergement.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Mise à jour des composants d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba559323c3272db96f0cd106f0fc61624519b770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951094"
---
# <a name="updating-application-components"></a>Mise à jour des composants d’application

Les assemblys privés côte à côte peuvent être utilisés pour créer des composants qui peuvent être facilement mis à jour sans mettre à jour également l’application d’hébergement. Cela permet à un service de mise à jour d’installer les composants mis à jour de l’application, de redémarrer l’application et de faire en sorte que l’application utilise les modifications. Lors de l’utilisation de manifestes d’application, les fonctionnalités des composants hébergés par une application peuvent être mises à jour sans avoir à modifier le code de l’application d’hébergement.

Cette méthode peut être utilisée pour mettre à jour la version des ressources d’une application. Par exemple, si une application contient un assembly, le manifeste de l’application peut spécifier une dépendance sur cet assembly. L’application peut obtenir l’assembly en appelant [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) pour rechercher et charger les fichiers dont il a besoin. Un programme de mise à jour doit simplement mettre en avant les derniers bits de l’assembly, qui peuvent exister côte à côte avec une version antérieure de l’assembly.

 

 
