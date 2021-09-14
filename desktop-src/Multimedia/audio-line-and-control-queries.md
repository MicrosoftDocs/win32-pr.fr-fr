---
title: Requêtes audio et de contrôle
description: Requêtes audio et de contrôle
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- audio multimédia, contrôles de mixage
- audio, contrôles de mixage
- mixages audio, lignes audio
- lignes audio
- mixages audio, contrôles
- mélangeurs, contrôles
- mixages, lignes audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007268"
---
# <a name="audio-line-and-control-queries"></a>Requêtes audio et de contrôle

Les services de mixage fournissent des fonctions permettant de déterminer les informations sur les lignes audio, les contrôles de ligne audio et les détails de contrôle. Les services fournissent également des fonctions permettant de définir les détails du contrôle.

Vous pouvez utiliser la fonction [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) pour récupérer des informations sur une ligne audio spécifiée. Cette fonction remplit la structure [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) pour une ligne audio source, une ligne audio de destination ou un identificateur de ligne spécifiés. La structure comprend le numéro de ligne de destination, le nombre de canaux dans la ligne audio, ainsi qu’un nom abrégé et un nom long pour la ligne audio.

La fonction [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) récupère des informations générales sur un ou plusieurs contrôles associés à une ligne audio. Cette fonction remplit la structure [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) avec des informations sur le ou les contrôles spécifiés. Vous pouvez utiliser **mixerGetLineControls** pour récupérer des propriétés de contrôle pour l’un des éléments suivants :

-   Tous les contrôles pour une ligne source spécifiée
-   Contrôle spécifié pour une ligne source spécifiée
-   Premier contrôle d’une classe spécifique pour une ligne source spécifiée

La fonction [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) récupère les propriétés d’un contrôle unique associé à une ligne audio. Cette fonction remplit la structure [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) avec les valeurs actuelles d’un contrôle.

La fonction [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) utilise le contenu de la structure **MIXERCONTROLDETAILS** pour définir les propriétés du contrôle spécifié. Vous devez vous assurer que tous les membres de cette structure sont remplis avant d’appeler **mixerSetControlDetails**.

 

 