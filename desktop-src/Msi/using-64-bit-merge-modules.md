---
description: Suivez ces instructions lors de la création d’un module de fusion 64 bits.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Utilisation des modules de fusion 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757804"
---
# <a name="using-64-bit-merge-modules"></a>Utilisation des modules de fusion 64 bits

Un module de fusion 64 bits présente l’une des caractéristiques identifiées dans cette rubrique.

-   Le module de fusion contient au moins un composant qui a été compilé pour les systèmes d’exploitation 64 bits.
-   Le module de fusion ne contient aucun composant 64 bits, mais il est destiné à être utilisé uniquement avec les packages de [Windows Installer 64 bits](64-bit-windows-installer-packages.md) .

Les modules de fusion peuvent être utilisés comme suit :

-   Un module de fusion 64 bits peut être fusionné dans un package [Windows Installer 64 bits](64-bit-windows-installer-packages.md) . Les propriétés [**Résumé du modèle**](template-summary.md) dans le module de fusion et dans le package Windows Installer doivent être définies sur le même type de processeur 64 bits. Un module de fusion x64 ne peut être fusionné que dans des packages x64 et un module de fusion Intel64 ne peut être fusionné que dans des packages Intel64.
-   Un module de fusion 32 bits peut être fusionné dans des packages de Windows Installer 32 bits ou [64](64-bit-windows-installer-packages.md) bits.
-   Un module de fusion 64 bits peut être fusionné dans un package 64 bits sur un système d’exploitation 32 bits.

Respectez les points suivants lors de la création d’un module de fusion 64 bits :

-   Utilisez la même procédure générale que lors de la création de modules de fusion bits 32. Pour plus d’informations, consultez [à propos des modules de fusion](about-merge-modules.md) et [création de modules de fusion](authoring-merge-modules.md).
-   Si vous exécutez un système Intel64, vous devez définir la propriété [**Résumé du modèle**](template-summary.md) avec la valeur Intel64. Vous devez définir la propriété **Résumé du modèle** avec la valeur x64 si vous exécutez un système x64. Pour plus d’informations, consultez [Référence du flux des informations résumées du module de fusion](merge-module-summary-information-stream-reference.md).
-   Lorsque les deux modules de fusion 32 bits et 64 bits existent pour le même composant, il est recommandé que les modules aient des signatures différentes. Cela permet à un package de contenir les deux versions du composant.

Pour plus d’informations, consultez [Windows Installer sur les systèmes d’exploitation 64 bits](windows-installer-on-64-bit-operating-systems.md).

 

 



