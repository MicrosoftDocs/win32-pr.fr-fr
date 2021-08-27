---
description: Les assemblys privés côte à côte peuvent être utilisés pour créer des composants qui peuvent être facilement mis à jour sans mettre à jour également l’application d’hébergement.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Mise à jour des composants d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02948355143bc6f08c759ec6c2fe6009399cc6d8ca4b2bbd687e3d206c0e771f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101589"
---
# <a name="updating-application-components"></a>Mise à jour des composants d’application

Les assemblys privés côte à côte peuvent être utilisés pour créer des composants qui peuvent être facilement mis à jour sans mettre à jour également l’application d’hébergement. Cela permet à un service de mise à jour d’installer les composants mis à jour de l’application, de redémarrer l’application et de faire en sorte que l’application utilise les modifications. Lors de l’utilisation de manifestes d’application, les fonctionnalités des composants hébergés par une application peuvent être mises à jour sans avoir à modifier le code de l’application d’hébergement.

Cette méthode peut être utilisée pour mettre à jour la version des ressources d’une application. Par exemple, si une application contient un assembly, le manifeste de l’application peut spécifier une dépendance sur cet assembly. L’application peut obtenir l’assembly en appelant [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) pour rechercher et charger les fichiers dont il a besoin. Un programme de mise à jour doit simplement mettre en avant les derniers bits de l’assembly, qui peuvent exister côte à côte avec une version antérieure de l’assembly.

 

 
