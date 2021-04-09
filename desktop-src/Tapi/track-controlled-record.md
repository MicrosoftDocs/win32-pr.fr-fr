---
description: Cette rubrique fournit une procédure pour effectuer l’enregistrement contrôlé par suivi des flux audio.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Enregistrement Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865689"
---
# <a name="track-controlled-record"></a>Enregistrement Track-Controlled

Cette rubrique fournit une procédure pour effectuer l’enregistrement contrôlé par suivi des flux audio.

**Pour effectuer un enregistrement contrôlé des flux audio**

1.  Sélectionnez fichier suivre les terminaux dans les flux.
2.  Créez le terminal d’enregistrement de fichier.
3.  Définissez le nom du fichier.
4.  Énumérer les flux sur l’appel TAPI. Pour ces étapes, consultez la procédure suivante.
5.  Appelez la méthode [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) sur le terminal d’enregistrement de fichier pour démarrer l’enregistrement de flux.

**Pour énumérer des flux sur l’appel TAPI**

1.  Créer une piste du même type et de la même direction audio que le flux.
2.  Définissez les propriétés de suivi pour le format audio. Si la valeur n’est pas définie, le format sera le même que celui du flux.
3.  Sélectionnez la piste dans le flux.

Si une piste est sélectionnée sur plusieurs flux, cela implique la combinaison de flux.

 

 



