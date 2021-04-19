---
description: Chaque fois que vous apportez des modifications au package, les auteurs des packages de mise à niveau doivent toujours exécuter la validation sur leurs packages avant de tenter d’installer le package pour la première fois et de réexécuter la validation.
ms.assetid: c578c020-18be-47ea-8f59-c1bbd45f1260
title: Validation de la mise à niveau d’une installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cab7f45d3d5c19a71dac8c7a2d0150409b3a45f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538225"
---
# <a name="validating-an-installation-upgrade"></a>Validation de la mise à niveau d’une installation

Chaque fois que vous apportez des modifications au package, les auteurs des packages de mise à niveau doivent toujours exécuter la validation sur leurs packages avant de tenter d’installer le package pour la première fois et de réexécuter la validation. Exécutez la validation sur un package de mise à niveau de la même façon que pour un package d’installation. Pour plus d’informations, consultez [validation d’une base de données d’installation](validating-an-installation-database.md).

Cela termine l’exemple de package de mise à niveau. Pour installer la mise à niveau, installez d’abord MNP2000.msi puis installez MNP2001.msi. Lorsque vous désinstallez MNP2001, les produits d’origine et de mise à niveau sont supprimés de votre ordinateur.

## <a name="next-example"></a>Exemple suivant

[Exemple de transformation de personnalisation](a-customization-transform-example.md)

 

 



