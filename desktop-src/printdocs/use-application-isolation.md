---
description: Les applications peuvent déclarer l’isolement du pilote d’imprimante dans leur manifeste d’application pour isoler l’application du pilote d’imprimante et améliorer la fiabilité des applications.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 'Comment : utiliser l’isolation d’application'
ms.date: 05/31/2018
ms.openlocfilehash: 28c2a143406e9501662e0ddf7294abfb25e362b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202803"
---
# <a name="how-to-use-application-isolation"></a>Comment : utiliser l’isolation d’application

Les applications peuvent déclarer l’isolement du pilote d’imprimante dans leur manifeste d’application pour isoler l’application du pilote d’imprimante et améliorer la fiabilité de l’application. Le service d’impression Windows permet aux pilotes d’imprimante de s’exécuter dans des processus distincts du processus dans lequel le spouleur d’impression s’exécute. À l’aide de cette fonctionnalité, votre application l’empêche de se bloquer en cas d’erreur du pilote d’imprimante.

L’isolation du pilote d’imprimante est implémentée dans Windows 7 et Windows Server 2008 R2.

### <a name="prerequisites"></a>Prérequis

-   Application de code managé ou Windows Store qui utilise l’impression Windows.

## <a name="instructions"></a>Instructions

### <a name="update-the-app-manifest"></a>Mettre à jour le manifeste d’application

Pour activer l’isolation des pilotes d’imprimantes, vous devez ajouter l’élément **printerDriverIsolation** au manifeste de l’application. Voici comment faire :

1.  Modifiez le manifeste de l’application, en ajoutant l’élément **printerDriverIsolation** avec la valeur **true** à l’élément **windowsSettings** de l’élément **application** , comme indiqué dans cet exemple.
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  Régénérez votre application.

 

 



