---
description: 'Vous pouvez affecter une lettre de lecteur (par exemple, X : \) à un volume local à l’aide de la fonction SetVolumeMountPoint, à condition qu’il n’y ait aucun volume déjà affecté à cette lettre de lecteur.'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Affectation d’une lettre de lecteur à un volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f31b9446cc41ad26f14a34874c59e153e1db8ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534179"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a>Affectation d’une lettre de lecteur à un volume

Vous pouvez affecter une lettre de lecteur (par exemple, X : \) à un volume local à l’aide de la fonction [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , à condition qu’il n’y ait aucun volume déjà affecté à cette lettre de lecteur. Si le volume local a déjà une lettre de lecteur. Ensuite, [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) échoue. Pour gérer cela, commencez par supprimer la lettre de lecteur à l’aide de la fonction [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) . Pour obtenir un exemple de code, consultez [modification des affectations de lettres de lecteur](editing-drive-letter-assignments.md).

Le système prend en charge au plus une lettre de lecteur par volume. Par conséquent, vous ne pouvez pas avoir C : \\ et F : \\ représentent le même volume.

> [!Caution]
>
> La suppression d’une lettre de lecteur existante et l’affectation d’une nouvelle lettre peuvent altérer les chemins existants, tels que ceux des raccourcis sur le bureau. Il peut également rompre le chemin d’accès au programme en modifiant la lettre de lecteur. Avec la gestion de la mémoire virtuelle Windows, cela peut perturber l’application, ce qui laisse le système dans un état instable et peut-être inutilisable. Il incombe au concepteur de programme d’éviter ces catastrophes potentielles.

 

 

 



