---
description: organisation de l’espace de noms dans le SPI Windows sockets (Winsock).
ms.assetid: c369a476-23e4-48a1-912b-2d876deb0b88
title: Organisation de l’espace de noms dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d3cd2569f90009ceb4db9ceaca3d5020c6949e7e69842b96030cab4634c534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121379"
---
# <a name="namespace-organization-in-the-spi"></a>Organisation de l’espace de noms dans le SPI

De nombreux espaces de noms sont organisés hiérarchiquement. Certains, tels que X. 500 et NDS, permettent une imbrication illimitée. D’autres autorisent la combinaison de services dans un seul niveau de hiérarchie ou de groupe. Il s’agit généralement d’un groupe de travail. Lors de la construction d’une requête, il est souvent nécessaire d’établir un point de contexte dans une hiérarchie d’espaces de noms à partir de laquelle la recherche commence.

 

 



