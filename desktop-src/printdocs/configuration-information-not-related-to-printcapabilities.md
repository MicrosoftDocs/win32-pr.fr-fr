---
description: Outre PrintCapabilities, le PrintTicket autorise l’ajout d’informations supplémentaires par les clients sous la forme d’éléments de propriété.
ms.assetid: 00f1d2c4-3c71-4b64-b689-83b4399aa61d
title: Informations de configuration non liées à PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e4ac332d6e9b106ab9d68c29d03366761c01d5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409652"
---
# <a name="configuration-information-not-related-to-printcapabilities"></a><span data-ttu-id="c72d6-103">Informations de configuration non liées à PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="c72d6-103">Configuration Information Not Related to PrintCapabilities</span></span>

<span data-ttu-id="c72d6-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="c72d6-104">This topic is not current.</span></span> <span data-ttu-id="c72d6-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c72d6-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c72d6-106">En plus de fournir des sélections pour les attributs d’appareil définis dans le PrintCapabilities, l’élément PrintTicket autorise l’ajout d’informations supplémentaires par les clients sous la forme d’éléments de propriété.</span><span class="sxs-lookup"><span data-stu-id="c72d6-106">In addition to providing selections for the device attributes defined in the PrintCapabilities, the PrintTicket allows additional information to be added by clients in the form of Property elements.</span></span> <span data-ttu-id="c72d6-107">Le schéma d’impression définit un certain nombre d’instances de propriétés standard, et le fournisseur d’interface est libre d’introduire également des instances de propriété privées.</span><span class="sxs-lookup"><span data-stu-id="c72d6-107">The Print Schema defines a number of standard Property instances, and the interface provider is free to introduce private Property instances as well.</span></span> <span data-ttu-id="c72d6-108">Par exemple, si les membres d’une organisation envoient la plupart de leurs travaux d’impression à une fonctionnalité de traitement par lots centrale, ils peuvent spécifier pour chaque tâche une instance de propriété privée qui contient une adresse de retour.</span><span class="sxs-lookup"><span data-stu-id="c72d6-108">For example, if members of an organization send most of their print jobs to a central batch facility, they can specify for each job a private Property instance that contains a return address.</span></span> <span data-ttu-id="c72d6-109">Cette propriété peut faciliter la remise du travail terminé à l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="c72d6-109">This Property can make it easier to deliver the completed job can be delivered to the originator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c72d6-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c72d6-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c72d6-111">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="c72d6-111">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



