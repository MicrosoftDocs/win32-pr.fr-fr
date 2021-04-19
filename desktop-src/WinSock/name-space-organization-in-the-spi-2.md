---
description: Organisation de l’espace de noms dans le SPI Windows Sockets (Winsock).
ms.assetid: c369a476-23e4-48a1-912b-2d876deb0b88
title: Organisation de l’espace de noms dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a572ad86299f0bf5ba3e7f95662e1616da520608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515022"
---
# <a name="namespace-organization-in-the-spi"></a>Organisation de l’espace de noms dans le SPI

De nombreux espaces de noms sont organisés hiérarchiquement. Certains, tels que X. 500 et NDS, permettent une imbrication illimitée. D’autres autorisent la combinaison de services dans un seul niveau de hiérarchie ou de groupe. Il s’agit généralement d’un groupe de travail. Lors de la construction d’une requête, il est souvent nécessaire d’établir un point de contexte dans une hiérarchie d’espaces de noms à partir de laquelle la recherche commence.

 

 



