---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Lecteur Windows Media, migration de DVD
- Windows Media Player Object Model, DVD
- modèle objet, DVD
- Contrôle ActiveX du lecteur Windows Media, DVD
- Contrôle ActiveX, DVD
- Windows Media Player Mobile contrôle ActiveX, DVD
- Windows Media Player Mobile, migration de DVD
- Guide de migration, DVD
- Migration de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673950"
---
# <a name="dvd"></a>DVD

Le contrôle ActiveX du lecteur Windows Media 6,4 contient un objet **DVD** qui expose une variété de méthodes et de propriétés, et un événement pour traiter spécifiquement le contenu du DVD. Par exemple, pour déterminer le nombre de titres de DVD disponibles, vous utilisez **Player6**. propriété **titlesAvailable** :


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



Le modèle objet Windows Media Player 7 ou version ultérieure implémente une approche plus intégrée du DVD. Les propriétés, méthodes et événements spécifiques aux DVD sont implémentés uniquement lorsque cela est nécessaire. Dans le cas contraire, la fonctionnalité de modèle objet existante fonctionne avec les supports DVD, comme vous pouvez vous y attendre. Par exemple, pour déterminer le nombre de titres de DVD disponibles lors de l’utilisation du lecteur Windows Media 7 ou version ultérieure, vous récupérez un objet de **sélection** à partir de l’objet **cdrom** :


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



L’exemple précédent récupère un objet **playlist** avec une première entrée représentant le support DVD dans le premier lecteur. Les entrées supplémentaires représentent des titres de DVD individuels. Par conséquent, le nombre de titres disponibles peut être calculé comme suit :


```C++
var numTitles = dvdTitles.count - 1;

```



Voici les principales différences à prendre en compte lors de la migration à partir de la version 6,4 :

-   La lecture de DVD est prise en charge uniquement lors de l’utilisation du lecteur Windows Media pour Windows XP ou version ultérieure et du système d’exploitation Windows XP ou version ultérieure.
-   Les lecteurs de DVD-ROM sont énumérés exactement comme des lecteurs de CD-ROM à l’aide de l’objet **CdromCollection** .
-   Les lecteurs de DVD-ROM individuels sont gérés à l’aide de l’objet **cdrom** .
-   L’objet **DVD** étend le modèle objet avec les méthodes et une propriété spécifiquement pour l’utilisation de DVD.
-   Il existe deux nouveaux événements, **OpenPlaylistSwitch** et **DomainChange**, en particulier pour l’utilisation de DVD.
-   Le contenu DVD est organisé à l’aide d’objets de **sélection** et d’objets **multimédias** .
-   Les langues des DVD sont gérées à l’aide des fonctionnalités de langage disponibles à partir de l’objet **contrôles** (Windows Media Player 9 Series ou version ultérieure).
-   Les contrôles de transport et les informations de position pour le DVD fonctionnent de la même façon que pour les autres types de médias numériques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de migration du modèle objet**](object-model-migration-guide.md)
</dt> <dt>

[**Utilisation du contrôle du lecteur Windows Media avec Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




