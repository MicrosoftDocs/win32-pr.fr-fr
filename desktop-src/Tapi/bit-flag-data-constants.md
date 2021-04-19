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
# <a name="bit-flag-data-constants"></a><span data-ttu-id="5d725-103">Bit-Flag les constantes de données</span><span class="sxs-lookup"><span data-stu-id="5d725-103">Bit-Flag Data Constants</span></span>

<span data-ttu-id="5d725-104">Pour les constantes de données de l’indicateur de bit extensible, un fournisseur de fournisseurs de services peut définir de nouvelles valeurs pour les bits spécifiés.</span><span class="sxs-lookup"><span data-stu-id="5d725-104">For extensible bit-flag data constants, a service-provider vendor can define new values for specified bits.</span></span> <span data-ttu-id="5d725-105">Étant donné que la plupart des constantes d’indicateur de bits sont des **DWORD** s, un nombre spécifique de bits inférieurs est généralement réservé pour les extensions communes, tandis que les bits supérieurs restants sont disponibles pour les extensions spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5d725-105">Because most bit-flag constants are **DWORD** s, a specific number of the lower bits are usually reserved for common extensions, while the remaining upper bits are available for vendor-specific extensions.</span></span> <span data-ttu-id="5d725-106">Les indicateurs binaires communs sont assignés de bit zéro vers le haut, et les extensions spécifiques au fournisseur doivent être assignées de bit 31.</span><span class="sxs-lookup"><span data-stu-id="5d725-106">Common bit flags are assigned from bit zero up, and vendor-specific extensions should be assigned from bit 31 down.</span></span> <span data-ttu-id="5d725-107">Ce schéma offre une flexibilité maximale pour l’affectation de positions de bits aux extensions courantes, par opposition aux extensions spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5d725-107">This scheme provides maximum flexibility in assigning bit positions to common extensions, as opposed to vendor-specific extensions.</span></span> <span data-ttu-id="5d725-108">Un fournisseur est censé définir de nouvelles valeurs qui sont des extensions naturelles des indicateurs binaires définis par l’API.</span><span class="sxs-lookup"><span data-stu-id="5d725-108">A vendor is expected to define new values that are natural extensions of the bit flags defined by the API.</span></span>

<span data-ttu-id="5d725-109">Les structures de données extensibles ont un champ de taille variable qui est réservé à une utilisation spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5d725-109">Extensible data structures have a variably sized field that is reserved for device-specific use.</span></span> <span data-ttu-id="5d725-110">Étant donné que le champ est de taille variable, le fournisseur de services choisit la quantité d’informations et l’interprétation du champ.</span><span class="sxs-lookup"><span data-stu-id="5d725-110">Because the field is variably sized, the service provider decides the field's amount of information and interpretation.</span></span> <span data-ttu-id="5d725-111">Un fournisseur qui définit un champ spécifique à l’appareil est supposé créer ces extensions naturelles de la structure de données d’origine définies par l’API.</span><span class="sxs-lookup"><span data-stu-id="5d725-111">A vendor that defines a device-specific field is expected to make these natural extensions of the original data structure defined by the API.</span></span>

 

 



