---
description: les modules de fusion sont essentiellement simplifiés .msi fichiers, qui est l’extension de nom de fichier d’un package d’installation Windows Installer. Un module de fusion standard a une extension de nom de fichier. msm.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: À propos des modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3e6c0ec1d4d7073d85984539ce54b47de92885a64570bc1de709be64748b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640161"
---
# <a name="about-merge-modules"></a>À propos des modules de fusion

les modules de fusion sont essentiellement simplifiés .msi fichiers, qui est l’extension de nom de fichier d’un package d’installation Windows Installer. Un module de fusion standard a une extension de nom de fichier. msm.

Un module de fusion ne peut pas être installé seul, car il n’a pas de tables de base de données vitales présentes dans une base de données d’installation. Les modules de fusion contiennent également des tables supplémentaires qui sont uniques à eux-mêmes. Pour installer les informations fournies par un module de fusion avec une application, le module doit d’abord être fusionné dans le fichier .msi de l’application.

Un module de fusion se compose des éléments suivants :

-   Une [base de données de module de fusion](merge-module-database.md) contenant les propriétés d’installation et la logique d’installation fournies par le module de fusion.
-   [Référence du flux de données de résumé du module de fusion](merge-module-summary-information-stream-reference.md) décrivant le module.
-   Fichier CAB [ inetMergeModule.CAB](mergemodule-cabinet.md) stocké en tant que flux à l’intérieur du module de fusion. Ce fichier cab contient tous les fichiers requis par les composants fournis par le module de fusion.

Les [modules de fusion à plusieurs langues](multiple-language-merge-modules.md) peuvent fournir des composants à un package d’installation dans plusieurs langues. Dans un module de fusion à plusieurs langues, la base de données contient les propriétés d’installation et la logique pour plusieurs langues et l’armoire MergeModule.CABinet inclut tous les fichiers nécessaires pour installer les composants avec toutes les langues prises en charge par le module.

 

 



