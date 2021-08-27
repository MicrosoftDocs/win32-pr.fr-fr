---
description: Le tableau suivant identifie les limites de taille pour les différents éléments du Registre.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Limites de taille des éléments du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76a11abc80f80a13e0643d7745d211168ecba8bcf06446af9ac842f8351567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885232"
---
# <a name="registry-element-size-limits"></a>Limites de taille des éléments du Registre

Le tableau suivant identifie les limites de taille pour les différents éléments du Registre.



| Élément Registry | Taille maximale                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom de clé         | 255 caractères. Le nom de clé comprend le chemin d’accès absolu de la clé dans le registre, en commençant toujours à une clé de base, par exemple, HKEY \_ local \_ machine. |
| Nom de valeur       | 16 383 caractères **Windows 2000 :** 260 caractères ANSI ou 16 383 caractères Unicode.<br/>                                                       |
| Valeur            | Mémoire disponible (format le plus récent) 1 Mo (format standard)<br/>                                                                                     |
| Arborescence             | Une arborescence du Registre peut avoir 512 niveaux de profondeur. Vous pouvez créer jusqu’à 32 niveaux à la fois à l’aide d’un appel d’API de Registre unique.                                  |



 

Les valeurs longues (plus de 2 048 octets) doivent être stockées dans un fichier et l’emplacement du fichier doit être stocké dans le registre. Cela permet au registre de fonctionner efficacement.

L’emplacement du fichier peut être le nom d’une valeur ou les données d’une valeur. Chaque barre oblique inverse dans la chaîne d’emplacement doit être précédée d’une autre barre oblique inverse comme caractère d’échappement. Par exemple, spécifiez « C : \\ \\ mydir \\ \\ MyFile » pour stocker la chaîne « c : \\ mydir \\ MyFile ». Un emplacement de fichier peut également être le nom d’une clé s’il se trouve dans la limite de 255 caractères pour les noms de clé et ne contient pas de barres obliques inverses, qui ne sont pas autorisées dans les noms de clés.

 

 




