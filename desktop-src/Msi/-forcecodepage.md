---
description: La \_ table ForceCodepage est une table spéciale utilisée pour modifier la page de codes d’un package d’installation. Vous pouvez déterminer ou définir la page de codes en exportant ou en important un fichier d’archive de texte nommé \_ ForceCodepage. IDT.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519663"
---
# <a name="_forcecodepage"></a>\_ForceCodepage

La \_ table ForceCodepage est une table spéciale utilisée pour modifier la page de codes d’un package d’installation. Vous pouvez déterminer ou définir la page de codes en exportant ou en important un [fichier d’archive de texte](text-archive-files.md) nommé \_ ForceCodepage. IDT.

Le format de la \_ table ForceCodepage est 2 lignes vides suivies d’une troisième ligne indiquant la page de codes numérique. Par exemple, un \_ fichier ForceCodepage table. IDT pour une base de données japonaise se présenterait comme suit. Dans ce cas, la page de codes numérique est 932.

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

Pour plus d’informations sur l’utilisation de \_ ForceCodepage pour obtenir ou définir la page de codes d’une base de données, consultez les rubriques suivantes.

-   [Gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md)
-   [Détermination de la page de codes d’une base de données d’installation](determining-an-installation-database-s-code-page.md)
-   [Définition de la page de codes d’une base de données](setting-the-code-page-of-a-database.md)

La \_ table ForceCodepage est une pseudo-table spéciale utilisée pour modifier la page de codes d’un package d’installation. L’utilisation de la \_ table ForceCodepage définit de manière inconditionnelle la base de données sur la page de codes sans effectuer de validation pour déterminer si les données présentes dans la base de données peuvent être traduites dans la nouvelle page de codes. Il est toujours recommandé de modifier la page de codes d’une base de données à partir d’une base de données indépendante de la langue.

 

 



