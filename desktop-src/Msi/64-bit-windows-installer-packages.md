---
description: Un package 64 bits se compose partiellement ou entièrement de composants Windows Installer de 64 bits.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: Packages de Windows Installer 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864541"
---
# <a name="64-bit-windows-installer-packages"></a>Packages de Windows Installer 64 bits

Un package 64 bits se compose partiellement ou entièrement de composants [Windows Installer](windows-installer-components.md) de 64 bits. La liste suivante répertorie les conditions requises pour chaque package Windows Installer 64 bits :

-   La valeur « Intel64 » doit être entrée dans le champ plateforme de la propriété [**Résumé du modèle**](template-summary.md) si et seulement si le package s’exécute sur un processeur Intel64 (Itanium).
-   La valeur « x64 » doit être entrée dans le champ plateforme de la propriété [**Résumé du modèle**](template-summary.md) si et uniquement si le package s’exécute sur un processeur x64.
-   La valeur « Arm64 » doit être entrée dans le champ Platform de la propriété [**Résumé du modèle**](template-summary.md) si et seulement si le package s’exécute sur un processeur Arm64.
-   La propriété de [**Résumé du nombre de pages**](page-count-summary.md) doit être définie sur l’entier 200 ou supérieur, car Windows Installer 2,0 est la version minimale qui est capable d’installer les composants 64 bits. Les packages pour la plateforme Arm64 nécessitent une valeur supérieure ou égale à 500.
-   Chaque composant de Windows Installer 64 bits dans le package doit inclure le bit **msidbComponentAttributes64bit** dans la colonne attributs de la [table des composants](component-table.md).

Pour plus d’informations, consultez [Windows Installer sur les systèmes d’exploitation 64 bits](windows-installer-on-64-bit-operating-systems.md) et les [packages Windows Installer 32 bits](32-bit-windows-installer-packages.md).

 

 



