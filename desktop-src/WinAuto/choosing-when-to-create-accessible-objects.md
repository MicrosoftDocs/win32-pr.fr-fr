---
title: Choix du moment où créer des objets accessibles
description: Les développeurs de serveurs peuvent créer tous les objets accessibles au sein d’un conteneur lorsque le conteneur est créé, ou ils peuvent créer les objets accessibles dynamiquement.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a53ee02cb7de574242b3ba9986cdf0ce6068e8495e1ebaf638eed08e9c04b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325978"
---
# <a name="choosing-when-to-create-accessible-objects"></a>Choix du moment où créer des objets accessibles

Les développeurs de serveurs peuvent créer tous les objets accessibles au sein d’un conteneur lorsque le conteneur est créé, ou ils peuvent créer les objets accessibles dynamiquement.

Par exemple, Imaginez une boîte de dialogue avec plusieurs contrôles personnalisés. Un serveur crée des objets accessibles pour tous les contrôles personnalisés lorsque la boîte de dialogue s’affiche. Toutefois, si l’un des contrôles est une zone de liste déroulante personnalisée, le serveur attend qu’un utilisateur le sélectionne pour créer des objets accessibles pour les éléments contenus dans la zone de liste déroulante.

En faisant en sorte que le parent crée dynamiquement des objets accessibles, les applications utilisent moins de mémoire que si tous les objets accessibles possibles ont été créés à l’avance.

 

 




