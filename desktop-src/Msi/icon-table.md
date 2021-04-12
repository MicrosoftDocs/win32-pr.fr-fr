---
description: Ce tableau contient les fichiers d’icône. Chaque icône de la table est copiée dans un fichier dans le cadre de la publication du produit à utiliser pour les raccourcis publiés et les serveurs OLE. Consultez Limitations OLE sur les flux.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Table d’icônes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202539"
---
# <a name="icon-table"></a>Table d’icônes

Ce tableau contient les fichiers d’icône. Chaque icône de la table est copiée dans un fichier dans le cadre de la publication du produit à utiliser pour les raccourcis publiés et les serveurs OLE. Consultez [limitations OLE sur les flux](ole-limitations-on-streams.md).

La table d’icônes contient les colonnes suivantes.



| Colonne | Type                         | Clé | Nullable |
|--------|------------------------------|-----|----------|
| Nom   | [Identificateur](identifier.md) | O   | N        |
| Données   | [Binaire](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Nom du fichier d’icône.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée
</dt> <dd>

Les données de l’icône binaire dans le format PE (. dll ou. exe) ou icône (. ico).

</dd> </dl>

## <a name="remarks"></a>Notes

Cette table est référencée lorsque l' [action PublishProduct](publishproduct-action.md) est exécutée.

Les icônes pour les raccourcis, les extensions de nom de fichier et les CLSID doivent être stockées dans des fichiers distincts du fichier cible lui-même. Cela est nécessaire, car le programme d’installation ne doit copier que les fichiers d’icône de petite taille sur l’ordinateur de l’utilisateur lors de la publication de la ressource. Le développeur d’un package d’installation doit donc créer des fichiers distincts contenant uniquement les icônes. Ces fichiers icône sont ensuite stockés sous forme de données binaires dans la table icône.

Les fichiers d’icône qui sont associés strictement à des extensions de nom de fichier ou à des CLSID peuvent avoir n’importe quelle extension, telle que. ico. Toutefois, les fichiers icône associés à des raccourcis doivent être au format binaire EXE et doivent être nommés de telle sorte que leur extension corresponde à l’extension de la cible. Le raccourci ne fonctionnera pas si cette règle n’est pas suivie. Par exemple, si un raccourci doit pointer vers une ressource contenant le fichier de clé Red.bar, le fichier d’icône doit également avoir l’extension. bar. Plusieurs icônes peuvent être insérées dans le même fichier d’icône, à condition que tous les fichiers cibles aient la même extension.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE50](ice50.md)  
</dl>

 

 



