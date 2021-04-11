---
title: État (kit de développement logiciel Windows Media Player)
description: Statut
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Apparences mobiles du lecteur Windows Media, affichage de l’État
- apparences, affichage de l’État
- référence pour les apparences, affichage de l’État
- affichage de l’État dans les apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032181"
---
# <a name="status-windows-media-player-sdk"></a>État (kit de développement logiciel Windows Media Player)

Vous souhaiterez peut-être utiliser un affichage d’État dans votre apparence. Si c’est le cas, l’élément Status doit être défini dans le fichier de définition d’apparence. Vous pouvez également afficher ces informations à l’aide de l’attribut Status dans l’élément de texte.

La section d’État du fichier de définition d’apparence commence par cette ligne :


```C++
[ Status ]

```



Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur l’affichage de l’État dans votre apparence.


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



Vous pouvez utiliser le modèle suivant pour la section État de votre fichier de définition d’apparence :


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



Vous devez utiliser l’ordre indiqué dans le modèle précédent pour obtenir des informations sur l’affichage de l’état de chaque ligne de la section État. Chaque partie de la ligne est requise. Les sections suivantes décrivent chaque élément :

-   [Élément d'état](status-item.md)
-   [Emplacement de l’État](status-location.md)
-   [Alignement de l’État](status-alignment.md)
-   [Police d’État](status-font.md)
-   [Couleur d’État](status-color.md)

Pour obtenir un exemple de code d’État, consultez la [section exemple d’État](sample-status-section.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence d’apparence**](skin-reference.md)
</dt> </dl>

 

 




