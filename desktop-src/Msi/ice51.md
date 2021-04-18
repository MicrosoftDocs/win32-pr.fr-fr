---
description: ICE51 vérifie qu’un titre a été fourni pour les fichiers de ressources de police.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204191"
---
# <a name="ice51"></a>ICE51

ICE51 vérifie qu’un titre a été fourni pour les fichiers de ressources de police.

Vous devez fournir un titre pour une ressource de police qui n’a pas de nom incorporé. Seuls les fichiers de ressources de polices. TTC,. ttf et. otf ne nécessitent pas de titre, car ces fichiers contiennent un nom incorporé. Ne fournissez pas de titre pour une ressource de police qui contient un nom incorporé, car le système enregistre ensuite la police à deux reprises.

**[Windows Installer 4,5 et versions antérieures](not-supported-in-windows-installer-4-5.md):** ICE51 ne vérifie pas les fichiers de ressources de police. otf.

## <a name="result"></a>Résultats

ICE51 publie une erreur s’il existe des fichiers de ressources de police. TTC,. ttf et. OTF avec des titres. ICE51 publie un avertissement s’il existe d’autres fichiers de ressources de police sans titre.

## <a name="example"></a>Exemple

ICE51 signale l’avertissement suivant pour l’exemple indiqué.

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

ICE51 signale le message d’erreur suivant pour l’exemple indiqué.

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

[Table de fichiers](file-table.md) (partielle)



| Fichier  | FileName  |
|-------|-----------|
| Font1 | font1. ttf |
| Font2 | Font2. fon |



 

[Tableau des polices](font-table.md)



| fichier\_ | FontTitle          |
|--------|--------------------|
| Font1  | Police vraiment cool |
| Font2  |                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



