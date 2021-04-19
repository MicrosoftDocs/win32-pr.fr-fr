---
description: Une fois que vous avez créé une extension de composant logiciel enfichable d’attachement, vous devez l’inscrire pour que la console MMC et les composants logiciels enfichables de configuration de la sécurité la localisent et l’utilisent.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Inscription d’une extension de composant logiciel enfichable pièce jointe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514597"
---
# <a name="registering-an-attachment-snap-in-extension"></a>Inscription d’une extension de composant logiciel enfichable pièce jointe

Une fois que vous avez créé une extension de composant logiciel enfichable d’attachement, vous devez l’inscrire pour que la console MMC et les composants logiciels enfichables de configuration de la sécurité la localisent et l’utilisent.

Le composant logiciel enfichable de votre pièce jointe doit étendre l’espace de noms des composants logiciels enfichables de configuration de sécurité en ajoutant son propre nœud, comme décrit dans la procédure suivante.

**Pour installer et inscrire l’extension du composant logiciel enfichable pièce jointe**

1.  Enregistrez l’extension du composant logiciel enfichable sous la clé de Registre suivante. Ne créez pas de clé autonome sous le composant logiciel enfichable. les extensions des composants logiciels enfichables d’attachement doivent uniquement être des extensions.

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  Enregistrez l’extension du composant logiciel enfichable d’attachement sous les sous-clés suivantes. Cela peut être fait dans le cadre de vos implémentations de fonction **DllRegisterServer** et **DllUnregisterServer** .

    Espace de noms [modèles de sécurité](security-templates.md) :

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    Espace de noms d' [analyse et de configuration de la sécurité](security-configuration-and-analysis.md) :

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



