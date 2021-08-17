---
title: Mixer SOA
description: Mixer SOA
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- audio multimédia, architecture de mixage
- audio, architecture de mixage
- mixages audio, architecture
- mixages audio, lignes audio
- lignes audio
- mixages audio, contrôles
- audio multimédia, contrôles de mixage
- audio, contrôles de mixage
- mixages, lignes audio
- mixages, architecture
- mélangeurs, contrôles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f435396dd2a8d5983f596628711dfd01afe7111e75af1dc2060f5c6c4ef0a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065609"
---
# <a name="mixer-architecture"></a>Mixer SOA

L’élément de base de l’architecture du mélangeur est une *ligne audio*. Une ligne audio se compose d’un ou de plusieurs canaux de données provenant d’une source unique ou d’une ressource système. Par exemple, une ligne audio stéréo a deux canaux de données, mais elle est considérée comme une seule ligne audio, car elle provient d’une source unique.

L’architecture du mélangeur fournit des services de routage pour gérer les lignes audio sur un ordinateur. Vous pouvez utiliser les services de routage si vous avez installé les périphériques matériels et les pilotes de logiciels appropriés. L’architecture du mélangeur permet de mapper plusieurs lignes de sources audio sur une seule ligne audio de destination.

Chaque ligne audio peut être associée à des contrôles de mixage. Un contrôle de mixage peut exécuter un nombre quelconque de fonctions (telles que le volume de contrôle), en fonction des caractéristiques de la ligne audio associée.

 

 




