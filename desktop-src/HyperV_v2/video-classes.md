---
description: Toutes les machines virtuelles reflètent la présence d’un contrôleur vidéo S3 émulé et d’un contrôleur vidéo synthétique accéléré.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Classes vidéo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485696"
---
# <a name="video-classes"></a>Classes vidéo

Toutes les machines virtuelles reflètent la présence d’un contrôleur vidéo S3 émulé et d’un contrôleur vidéo synthétique accéléré.

Un objet tête vidéo est associé à chaque contrôleur d’affichage. Un seul contrôleur d’affichage peut être actif sur une machine virtuelle à tout moment.

Une connexion de terminal est présente pour chaque session à distance active connectée à une machine virtuelle.

Voici les classes WMI de virtualisation associées à Video.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                  | Description                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ S3DisplayController**](msvm-s3displaycontroller.md)<br/>               | Représente l’état du contrôleur S3 émulé qui est présent dans chaque configuration d’ordinateur virtuel.<br/>       |
| [**MSVM \_ SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)<br/> | Représente l’état du contrôleur d’affichage synthétique qui est présent dans chaque configuration d’ordinateur virtuel.<br/> |
| [**MSVM \_ SystemTerminalConnection**](msvm-systemterminalconnection.md)<br/>     | Associe un ordinateur virtuel à une connexion de terminal.<br/>                                                        |
| [**MSVM \_ TerminalConnection**](msvm-terminalconnection.md)<br/>                 | Indique l’état d’une session à distance active qui interagit avec un ordinateur virtuel.<br/>                             |
| [**MSVM \_ VideoHead**](msvm-videohead.md)<br/>                                   | Décrit la surface de dessin principale sur un contrôleur d’affichage.<br/>                                                  |
| [**MSVM \_ VideoHeadOnController**](msvm-videoheadoncontroller.md)<br/>           | Associe une tête vidéo au contrôleur vidéo qui l’intègre.<br/>                                             |



 

 

 




