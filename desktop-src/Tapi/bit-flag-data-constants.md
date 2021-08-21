---
description: Pour les constantes de données de l’indicateur de bit extensible, un fournisseur de fournisseurs de services peut définir de nouvelles valeurs pour les bits spécifiés.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Bit-Flag les constantes de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7842c7054fb973e4159b281486e4f4326debf3178b340770c0be280c7d1620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871501"
---
# <a name="bit-flag-data-constants"></a>Bit-Flag les constantes de données

Pour les constantes de données de l’indicateur de bit extensible, un fournisseur de fournisseurs de services peut définir de nouvelles valeurs pour les bits spécifiés. Étant donné que la plupart des constantes d’indicateur de bits sont des **DWORD** s, un nombre spécifique de bits inférieurs est généralement réservé pour les extensions communes, tandis que les bits supérieurs restants sont disponibles pour les extensions spécifiques au fournisseur. Les indicateurs binaires communs sont assignés de bit zéro vers le haut, et les extensions spécifiques au fournisseur doivent être assignées de bit 31. Ce schéma offre une flexibilité maximale pour l’affectation de positions de bits aux extensions courantes, par opposition aux extensions spécifiques au fournisseur. Un fournisseur est censé définir de nouvelles valeurs qui sont des extensions naturelles des indicateurs binaires définis par l’API.

Les structures de données extensibles ont un champ de taille variable qui est réservé à une utilisation spécifique à l’appareil. Étant donné que le champ est de taille variable, le fournisseur de services choisit la quantité d’informations et l’interprétation du champ. Un fournisseur qui définit un champ spécifique à l’appareil est supposé créer ces extensions naturelles de la structure de données d’origine définies par l’API.

 

 



