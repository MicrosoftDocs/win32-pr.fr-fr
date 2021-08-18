---
description: La propriété DVDDirectory définit ou récupère le répertoire actif du volume DVD actuel.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Propriété DVDDirectory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2431d9255aa743698baeb9c4b8427ffa9bf5220a60182ac08c246e11f20bcec8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749099"
---
# <a name="dvddirectory-property"></a>Propriété DVDDirectory

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDDirectory` propriété définit ou récupère le répertoire actif du volume DVD actuel.

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur de chaîne indiquant le chemin d’accès au répertoire racine du DVD.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture sans valeur par défaut. Utilisez cette méthode pour définir le chemin d’accès racine lorsqu’il y a plus d’un lecteur de DVD sur un système. Lorsqu’il n’y a qu’un seul lecteur sur le système et que sa lettre de lecteur est supérieure à « C », l’objet MSWebDVD le détecte automatiquement. Pour un disque DVD-Video standard, le chemin racine doit inclure le \_ répertoire vidéo TS :


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



Certains volumes de DVD peuvent avoir leur vidéo dans un répertoire nommé autre que « vidéo \_ TS ». L’idée générale est qu’un « volume DVD » supplémentaire (le jeu de. IFO. VOB et. Les fichiers BUP qui seraient normalement stockés dans le répertoire de la vidéo \_ TS) peuvent être placés dans un sous-répertoire du disque. En modifiant la racine pour pointer vers ce répertoire, MSWebDVD fonctionnera sur ce volume de DVD distinct. Un nouvel ensemble de menus, titres, etc. sera disponible, indépendamment des titres dans la racine de la vidéo \_ TS, qui n’est plus accessible. Ces répertoires sont appelés « répertoires cachés ». L’exemple suivant montre comment définir un répertoire masqué comme racine, où « Hidden » est un espace réservé pour le nom que les créateurs de disque ont donné au répertoire.


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



