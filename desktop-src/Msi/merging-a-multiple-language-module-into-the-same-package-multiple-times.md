---
description: Lorsqu’un module prend en charge plusieurs langues, vous pouvez le fusionner dans la même Windows Installer base de données plusieurs fois, tout en veillant à ce que chaque fusion utilise une langue différente.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Fusion multiple d’un module multiple Language dans le même package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520677"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a>Fusion multiple d’un module multiple Language dans le même package

Lorsqu’un module prend en charge plusieurs langues, vous pouvez le fusionner dans la même Windows Installer base de données plusieurs fois, tout en veillant à ce que chaque fusion utilise une langue différente. Avant chaque fusion, demandez une autre langue à partir du module. La base de données. msi qui en résulte possède ensuite un enregistrement dans la [table ModuleSignature](modulesignature-table.md) pour chaque fusion du module. Les composants qui sont partagés entre les langages existent une seule fois dans la [table des composants](component-table.md), mais sont associés à chaque langue dans la [table ModuleComponents](modulecomponents-table.md).

Lors de la fusion de plusieurs langues d’un module dans le même package, chaque fusion doit respecter les mêmes restrictions sur les pages de code que les modules à une seule langue. Les modules ne peuvent pas contenir de chaînes dans différentes pages de codes.

Lors de la fusion d’un module plusieurs fois dans un seul fichier. msi, vous devrez peut-être modifier l’ordre des fichiers dans la [table de fichiers](file-table.md) pour utiliser le fichier. cab existant à partir du module directement dans votre installation. L’ordre des fichiers dans la table de fichiers doit correspondre à l’ordre des fichiers dans le fichier. cab. Lors de la fusion d’un module plusieurs fois dans une base de données d’installation, la séquence peut être modifiée, car les fichiers partagés entre les langues peuvent déjà exister dans le module à partir d’une fusion antérieure, et ils ont un numéro de séquence relatif différent.

 

 



