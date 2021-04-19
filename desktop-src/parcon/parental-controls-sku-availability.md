---
description: Disponibilité des références SKU des contrôles parentaux
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Disponibilité des références SKU des contrôles parentaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b858bc62e8f10a3b06313befd99d67e497b8d442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518666"
---
# <a name="parental-controls-sku-availability"></a><span data-ttu-id="590ff-103">Disponibilité des références SKU des contrôles parentaux</span><span class="sxs-lookup"><span data-stu-id="590ff-103">Parental Controls SKU Availability</span></span>

<span data-ttu-id="590ff-104">Les interfaces utilisateur, les fonctionnalités et les API des contrôles parentaux décrits dans cette section sont actuellement planifiées pour être disponibles uniquement sur les références (SKU) axées sur le consommateur, telles que :</span><span class="sxs-lookup"><span data-stu-id="590ff-104">The Parental Controls user interfaces, features, and APIs described in this section are currently planned to be available only on consumer-focused SKUs such as:</span></span>

-   <span data-ttu-id="590ff-105">Windows Vista Starter</span><span class="sxs-lookup"><span data-stu-id="590ff-105">Windows Vista Starter</span></span>
-   <span data-ttu-id="590ff-106">Windows Vista Édition Familiale Basique</span><span class="sxs-lookup"><span data-stu-id="590ff-106">Windows Vista Home Basic</span></span>
-   <span data-ttu-id="590ff-107">Windows Vista Édition Familiale Premium</span><span class="sxs-lookup"><span data-stu-id="590ff-107">Windows Vista Home Premium</span></span>
-   <span data-ttu-id="590ff-108">Windows Vista Édition Intégrale</span><span class="sxs-lookup"><span data-stu-id="590ff-108">Windows Vista Ultimate</span></span>

<span data-ttu-id="590ff-109">Le contrôle parental s’installe uniquement sur ces références (SKU).</span><span class="sxs-lookup"><span data-stu-id="590ff-109">Parental Controls only installs on these SKUs.</span></span> <span data-ttu-id="590ff-110">Les solutions qui doivent être déployées sur les références SKU de l’entreprise devront :</span><span class="sxs-lookup"><span data-stu-id="590ff-110">Solutions having a requirement to deploy onto business SKUs will need to either:</span></span>

-   <span data-ttu-id="590ff-111">Détectez et ne fournissez pas de fonctionnalités de contrôle parental sur les références métier.</span><span class="sxs-lookup"><span data-stu-id="590ff-111">Detect and not provide parental controls functionality on business SKUs.</span></span>
-   <span data-ttu-id="590ff-112">Détectez et fournissez un autre moyen de configuration, de journalisation et de restrictions.</span><span class="sxs-lookup"><span data-stu-id="590ff-112">Detect and provide an alternative means of configuration, logging, and restrictions.</span></span>

<span data-ttu-id="590ff-113">Il est recommandé que les solutions détectent la disponibilité de l’infrastructure de contrôle parental en vérifiant la réussite de COM CoCreateInstance sur l’API de conformité.</span><span class="sxs-lookup"><span data-stu-id="590ff-113">It is recommended that solutions detect availability of the Parental Controls Infrastructure by checking for success of COM CoCreateInstance on the Compliance API.</span></span>

<span data-ttu-id="590ff-114">Les applications qui prennent en charge les contrôles parentaux en fonction de l’infrastructure de Windows Vista peuvent également vouloir supprimer toute leur propre interface utilisateur exposant des paramètres ou d’autres fonctionnalités lorsque l’interface utilisateur des contrôles parentaux est supprimée sur une référence SKU prise en charge.</span><span class="sxs-lookup"><span data-stu-id="590ff-114">Parental Controls-aware applications depending on the Windows Vista infrastructure may also want to suppress any of their own UI exposing settings or other functionality when Parental Controls UI is suppressed on a supported SKU.</span></span> <span data-ttu-id="590ff-115">Une fonction est fournie pour une détermination de visibilité qui couvre des cas tels que la suppression jointe à un domaine.</span><span class="sxs-lookup"><span data-stu-id="590ff-115">A function is provided for visibility determination that covers cases such as domain-joined suppression.</span></span>

 

 



