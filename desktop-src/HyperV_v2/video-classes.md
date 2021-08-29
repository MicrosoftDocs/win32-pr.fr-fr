---
description: Toutes les machines virtuelles reflètent la présence d’un contrôleur vidéo S3 émulé et d’un contrôleur vidéo synthétique accéléré.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Classes vidéo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a1880a37b6d71ef561cf702cce27a4b86f091701fcadbec59797343440238d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075249"
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



 

 

 




