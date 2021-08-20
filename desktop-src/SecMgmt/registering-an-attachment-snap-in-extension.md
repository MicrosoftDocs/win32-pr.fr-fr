---
description: Une fois que vous avez créé une extension de composant logiciel enfichable d’attachement, vous devez l’inscrire pour que la console MMC et les composants logiciels enfichables de configuration de la sécurité la localisent et l’utilisent.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Inscription d’une extension de composant logiciel enfichable pièce jointe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7af8b586f0071a5718b420612fd552d578bf30bb083cca45a43f38198e1aee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005017"
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

 

 



