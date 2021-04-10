---
title: Choix du moment où créer des objets accessibles
description: Les développeurs de serveurs peuvent créer tous les objets accessibles au sein d’un conteneur lorsque le conteneur est créé, ou ils peuvent créer les objets accessibles dynamiquement.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987b40527c178c40101288b0192c38d9a9b06040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029502"
---
# <a name="choosing-when-to-create-accessible-objects"></a>Choix du moment où créer des objets accessibles

Les développeurs de serveurs peuvent créer tous les objets accessibles au sein d’un conteneur lorsque le conteneur est créé, ou ils peuvent créer les objets accessibles dynamiquement.

Par exemple, Imaginez une boîte de dialogue avec plusieurs contrôles personnalisés. Un serveur crée des objets accessibles pour tous les contrôles personnalisés lorsque la boîte de dialogue s’affiche. Toutefois, si l’un des contrôles est une zone de liste déroulante personnalisée, le serveur attend qu’un utilisateur le sélectionne pour créer des objets accessibles pour les éléments contenus dans la zone de liste déroulante.

En faisant en sorte que le parent crée dynamiquement des objets accessibles, les applications utilisent moins de mémoire que si tous les objets accessibles possibles ont été créés à l’avance.

 

 




