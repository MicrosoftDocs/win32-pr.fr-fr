---
description: Les fournisseurs WMI sont généralement conçus pour fournir des informations sur un objet géré spécifique sur un seul ordinateur.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Liaison de classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534731"
---
# <a name="linking-classes-together"></a><span data-ttu-id="967de-103">Liaison de classes</span><span class="sxs-lookup"><span data-stu-id="967de-103">Linking Classes Together</span></span>

<span data-ttu-id="967de-104">Les fournisseurs WMI sont généralement conçus pour fournir des informations sur un objet géré spécifique sur un seul ordinateur.</span><span class="sxs-lookup"><span data-stu-id="967de-104">WMI providers are usually designed to provide information about a specific managed object on a single computer.</span></span> <span data-ttu-id="967de-105">S’il existe une propriété commune qui peut servir de clé pour identifier de façon unique toutes les différentes instances sources, utilisez le [fournisseur d’affichage](view-provider.md) pour combiner les propriétés de différentes classes, espaces de noms ou ordinateurs en une seule classe.</span><span class="sxs-lookup"><span data-stu-id="967de-105">If there is a common property that can serve as a key to uniquely identify all the different source instances, then use the [View Provider](view-provider.md) to combine properties from different classes, namespaces, or computers into a single class.</span></span>

<span data-ttu-id="967de-106">Vous devez d’abord [inscrire le fournisseur d’affichage](registering-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="967de-106">You must first [register the View Provider](registering-the-view-provider.md).</span></span> <span data-ttu-id="967de-107">Après l’inscription, vous pouvez créer les types de classes d’affichage suivants :</span><span class="sxs-lookup"><span data-stu-id="967de-107">After registration, you can create the following types of view classes:</span></span>

-   [<span data-ttu-id="967de-108">Vue de jointure</span><span class="sxs-lookup"><span data-stu-id="967de-108">Join view</span></span>](creating-a-new-instance-from-old-properties.md)

    <span data-ttu-id="967de-109">Instances de différentes classes connectées par une valeur de propriété commune.</span><span class="sxs-lookup"><span data-stu-id="967de-109">Instances of different classes connected by a common property value.</span></span>

-   [<span data-ttu-id="967de-110">Vue Association</span><span class="sxs-lookup"><span data-stu-id="967de-110">Association view</span></span>](associating-instances-between-namespaces.md)

    <span data-ttu-id="967de-111">Vues des classes d’association existantes à travers la limite de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="967de-111">Views of existing association classes across the namespace boundary.</span></span>

-   [<span data-ttu-id="967de-112">Vue Union</span><span class="sxs-lookup"><span data-stu-id="967de-112">Union view</span></span>](creating-a-union-view-class.md)

    <span data-ttu-id="967de-113">Union d’une ou plusieurs instances.</span><span class="sxs-lookup"><span data-stu-id="967de-113">Union of one or more instances.</span></span>

 

 



