---
description: Vous pouvez lancer une vue enracinée d’un point de jonction par le biais d’un fichier de raccourci vers ce point de jonction.
title: Comment ouvrir une vue enracinée d’un point de jonction à l’aide d’un fichier de raccourci
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52096f0dbbcebadb60e2612f0304ed497199b2ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581607"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a>Comment ouvrir une vue enracinée d’un point de jonction à l’aide d’un fichier de raccourci

Vous pouvez lancer une vue enracinée d’un point de jonction par le biais d’un [fichier de raccourci](./links.md) vers ce point de jonction.

## <a name="instructions"></a>Instructions


Définissez la ligne cible du fichier de raccourci sur Explorer.exe avec un indicateur/root. La forme exacte de la commande dépend de l’emplacement du point de jonction :

-   Si le point de jonction est un sous-dossier du bureau, utilisez :

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   Si le point de jonction est un dossier de système de fichiers, utilisez :

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   Si le point de jonction est un sous-dossier d’un dossier virtuel système, utilisez :

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    Les dossiers virtuels système qui peuvent contenir des points de jonction ont les identificateurs de classe suivants (CLSID) :

    

    | Dossier système     | Identificateur de classe                       |
    |-------------------|----------------------------------------|
    | Poste de travail       | {20D04FE0-3AEA-1069-A2D8-08002B30309D} |
    | Favoris réseau | {208D2C60-3AEA-1069-A2D7-08002B30309D} |
    | Control panel     | {21EC2020-3AEA-1069-A2DD-08002B30309D} |
    | Internet Explorer | {871C5380-42A0-1069-A2EA-08002B30309D} |

    

     

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification de l’emplacement d’une extension d’espace de noms](nse-junction.md)
</dt> <dt>

[Comment ouvrir une vue enracinée d’un point de jonction dans le registre](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
