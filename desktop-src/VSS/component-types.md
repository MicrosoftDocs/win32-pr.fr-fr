---
description: Les composants indiquent le type de données qu’ils représentent par le biais d’un type.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Types de composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413390"
---
# <a name="component-types"></a>Types de composants

Les composants indiquent le type de données qu’ils représentent par le biais d’un type.

Actuellement, les types de composant (consultez [**\_ \_ type de composant VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) sont limités à ce qui suit :

-   Composants de base de données
-   Groupes de fichiers

Pour plus d’informations sur la définition des types de composants, consultez [définition des composants par les Writers](definition-of-components-by-writers.md).

Les enregistreurs ont une saisie de données qui indique leur utilisation (consultez [**\_ \_ type de source VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), qui peut être la suivante :

-   une base de données transactionnelle (par exemple, un serveur SQL)
-   Une base de données non transactionnelle (comme un client de feuille de calcul)
-   Groupe de fichiers (autre)

La spécification d’un type de composant en tant que base de données permet d’identifier plus facilement son contenu, permet de gérer séparément les fichiers journaux et de données (consultez [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) et [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) pour plus d’informations) et applique une plus grande rigueur dans la sélection de fichiers en n’autorisant pas la sélection de fichier récursive ou en utilisant un [*autre chemin d’accès*](vssgloss-a.md) (voir [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) et [**IVssCreateWriterMetadata :**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

Avec un composant de groupe de fichiers, en revanche, au prix de ne pas connaître les données qu’il contient, vous avez une plus grande liberté quant à la façon dont les fichiers sont insérés, car vous pouvez utiliser la spécification récursive et d’autres chemins d’accès.

D’autres types de composants peuvent être ajoutés à l’avenir.

 

 



