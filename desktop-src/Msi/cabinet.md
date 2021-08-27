---
description: Le type de données Cabinet doit être utilisé dans la colonne Cabinet de la table Media.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16acfd031a6580f898d4cb464a15c895644995a2499a62ac79c9adeced8ccec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105359"
---
# <a name="cabinet"></a>CAB

Le type de données Cabinet doit être utilisé dans la colonne Cabinet de la [table Media](media-table.md).

Si le nom du fichier cab est précédé du signe dièse, le fichier cab est stocké en tant que flux de données à l’intérieur du package. La chaîne de caractères qui suit \# est un [identificateur](identifier.md) pour ce flux de données. Notez que si le fichier cab est stocké en tant que flux de données, le nom d’un fichier cab est sensible à la casse.

Si le nom du fichier CAB n’est pas précédé du signe dièse \# , le fichier cab est stocké dans un fichier séparé situé à la racine de l’arborescence source spécifiée par la [table Directory](directory-table.md). Le fichier cab doit utiliser la syntaxe de nom de fichier abrégé composée d’un nom de huit caractères, d’un point et d’une extension de trois caractères. Le type de données cabinet ne peut pas utiliser la \| syntaxe de Short longname pour les noms de fichiers. Si le fichier cab est stocké sous la forme d’un fichier distinct, le nom du fichier CAB ne respecte pas la casse.

Pour économiser de l’espace disque, le programme d’installation supprime toutes les armoires incorporées dans le fichier .msi avant la mise en cache du package d’installation sur l’ordinateur de l’utilisateur.

Voir [inclusion d’un fichier cab dans une installation](including-a-cabinet-file-in-an-installation.md).

 

 



