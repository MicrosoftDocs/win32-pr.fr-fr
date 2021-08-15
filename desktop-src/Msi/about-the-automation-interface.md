---
description: Un objet d’installation doit être créé initialement pour charger la prise en charge d’Automation requise pour accéder aux composants du programme d’installation via COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: À propos de l’interface d’automatisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c51469240ad684d6fd32ffbc5466007e73f4e4ff7a870b6878b18f25f54d32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382066"
---
# <a name="about-the-automation-interface"></a>À propos de l’interface d’automatisation

Un [**objet d’installation**](installer-object.md) doit être créé initialement pour charger la prise en charge d’Automation requise pour accéder aux composants du programme d’installation via com. Cet objet fournit des wrappers pour créer les objets de niveau supérieur et accéder à leurs méthodes. ces wrappers fournissent simplement des traductions de paramètres pour exposer les fonctions du programme d’installation d’une manière cohérente avec Microsoft Visual Basic sans modifier le comportement des méthodes.

dans la mesure du possible, une paire de méthodes C++ d’extraction et de définition sont exposées à Visual Basic en tant que propriété unique. Dans certains cas, les méthodes C++ qui prennent un argument d’index sont exposées en tant que propriété indexée. De nombreuses méthodes C++ retournent le résultat via un paramètre, car la valeur de retour est utilisée pour le retour d’erreur. toutefois, dans Visual Basic, les erreurs sont gérées par un mécanisme distinct, et le résultat est toujours passé dans la valeur de retour.

Pour plus d’informations sur l’utilisation d’Automation et la création de l’objet installer, consultez [utilisation de l’interface Automation](using-the-automation-interface.md).

pour obtenir des documents de référence pour les objets Windows Installer, consultez référence de l' [Interface Automation](automation-interface-reference.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



