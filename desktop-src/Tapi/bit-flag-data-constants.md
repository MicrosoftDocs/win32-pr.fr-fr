---
description: Pour les constantes de données de l’indicateur de bit extensible, un fournisseur de fournisseurs de services peut définir de nouvelles valeurs pour les bits spécifiés.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Bit-Flag les constantes de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519822"
---
# <a name="bit-flag-data-constants"></a>Bit-Flag les constantes de données

Pour les constantes de données de l’indicateur de bit extensible, un fournisseur de fournisseurs de services peut définir de nouvelles valeurs pour les bits spécifiés. Étant donné que la plupart des constantes d’indicateur de bits sont des **DWORD** s, un nombre spécifique de bits inférieurs est généralement réservé pour les extensions communes, tandis que les bits supérieurs restants sont disponibles pour les extensions spécifiques au fournisseur. Les indicateurs binaires communs sont assignés de bit zéro vers le haut, et les extensions spécifiques au fournisseur doivent être assignées de bit 31. Ce schéma offre une flexibilité maximale pour l’affectation de positions de bits aux extensions courantes, par opposition aux extensions spécifiques au fournisseur. Un fournisseur est censé définir de nouvelles valeurs qui sont des extensions naturelles des indicateurs binaires définis par l’API.

Les structures de données extensibles ont un champ de taille variable qui est réservé à une utilisation spécifique à l’appareil. Étant donné que le champ est de taille variable, le fournisseur de services choisit la quantité d’informations et l’interprétation du champ. Un fournisseur qui définit un champ spécifique à l’appareil est supposé créer ces extensions naturelles de la structure de données d’origine définies par l’API.

 

 



