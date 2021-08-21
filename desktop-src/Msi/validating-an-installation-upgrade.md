---
description: Chaque fois que vous apportez des modifications au package, les auteurs des packages de mise à niveau doivent toujours exécuter la validation sur leurs packages avant de tenter d’installer le package pour la première fois et de réexécuter la validation.
ms.assetid: c578c020-18be-47ea-8f59-c1bbd45f1260
title: Validation de la mise à niveau d’une installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549b53ae8d3337b8527cebb13ef819fb65d3345728b34ba632db560bcc438a2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499169"
---
# <a name="validating-an-installation-upgrade"></a>Validation de la mise à niveau d’une installation

Chaque fois que vous apportez des modifications au package, les auteurs des packages de mise à niveau doivent toujours exécuter la validation sur leurs packages avant de tenter d’installer le package pour la première fois et de réexécuter la validation. Exécutez la validation sur un package de mise à niveau de la même façon que pour un package d’installation. Pour plus d’informations, consultez [validation d’une base de données d’installation](validating-an-installation-database.md).

Cela termine l’exemple de package de mise à niveau. Pour installer la mise à niveau, installez d’abord MNP2000.msi puis installez MNP2001.msi. Lorsque vous désinstallez MNP2001, les produits d’origine et de mise à niveau sont supprimés de votre ordinateur.

## <a name="next-example"></a>Exemple suivant

[Exemple de transformation de personnalisation](a-customization-transform-example.md)

 

 



