---
description: Le Service VSS (VSS) fournit l’infrastructure système permettant d’exécuter des applications VSS sur des systèmes Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: Service VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751604"
---
# <a name="the-volume-shadow-copy-service"></a><span data-ttu-id="6a6a0-103">Service VSS</span><span class="sxs-lookup"><span data-stu-id="6a6a0-103">The Volume Shadow Copy Service</span></span>

<span data-ttu-id="6a6a0-104">Le Service VSS (VSS) fournit l’infrastructure système permettant d’exécuter des applications VSS sur des systèmes Windows.</span><span class="sxs-lookup"><span data-stu-id="6a6a0-104">The Volume Shadow Copy Service (VSS) provides the system infrastructure for running VSS applications on Windows-based systems.</span></span>

<span data-ttu-id="6a6a0-105">Bien qu’il soit largement transparent pour l’utilisateur et le développeur, VSS effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a6a0-105">Though largely transparent to user and developer, VSS does the following:</span></span>

-   <span data-ttu-id="6a6a0-106">Coordonne les activités des fournisseurs, des enregistreurs et des demandeurs lors de la création et de l’utilisation des clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="6a6a0-106">Coordinates activities of providers, writers, and requesters in the creation and use of shadow copies</span></span>
-   <span data-ttu-id="6a6a0-107">Fournit le fournisseur système par défaut</span><span class="sxs-lookup"><span data-stu-id="6a6a0-107">Furnishes the default system provider</span></span>
-   <span data-ttu-id="6a6a0-108">Implémente la fonctionnalité de pilote de bas niveau nécessaire pour que tout fournisseur fonctionne</span><span class="sxs-lookup"><span data-stu-id="6a6a0-108">Implements low-level driver functionality necessary for any provider to work</span></span>

<span data-ttu-id="6a6a0-109">Le service VSS démarre à la demande ; il doit donc être activé pour les opérations VSS puissent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="6a6a0-109">The VSS service starts on demand; therefore, for VSS operations to be successful, this service must be enabled.</span></span>

 

 



