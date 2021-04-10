---
description: Moniteur réseau fournit une structure PROPERTYINFO pour définir les propriétés d’un protocole, et une structure PROPERTYINST et PROPERTYINSTEX pour définir une instance d’une propriété.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Définition de propriété et structures d’instance de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55aa67efb5054d93184b56c53f84f9fac0893abf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756212"
---
# <a name="property-definition-and-property-instance-structures"></a><span data-ttu-id="f730f-103">Définition de propriété et structures d’instance de propriété</span><span class="sxs-lookup"><span data-stu-id="f730f-103">Property Definition and Property Instance Structures</span></span>

<span data-ttu-id="f730f-104">Moniteur réseau fournit une structure [**PROPERTYINFO**](propertyinfo.md) pour définir les propriétés d’un protocole, et une structure [**PROPERTYINST**](propertyinst.md)et [**PROPERTYINSTEX**](propertyinstex.md) pour définir une instance d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="f730f-104">Network Monitor provides a [**PROPERTYINFO**](propertyinfo.md) structure to define the properties of a protocol, and a [**PROPERTYINST**](propertyinst.md), and [**PROPERTYINSTEX**](propertyinstex.md) structure to define an instance of a property.</span></span>

![structures du moniteur réseau](images/property1.png)

<span data-ttu-id="f730f-106">L’analyseur alloue et remplit la structure [**PROPERTYINFO**](propertyinfo.md) pour toutes les propriétés qu’un protocole prend en charge.</span><span class="sxs-lookup"><span data-stu-id="f730f-106">The parser allocates and fills-in the [**PROPERTYINFO**](propertyinfo.md) structure for all the properties that a protocol supports.</span></span> <span data-ttu-id="f730f-107">L’analyseur passe la structure à Moniteur réseau où la structure est ajoutée à la [*base de données de propriétés de*](p.md)protocole.</span><span class="sxs-lookup"><span data-stu-id="f730f-107">The parser passes the structure to Network Monitor where the structure is added to the protocol [*property database*](p.md).</span></span> <span data-ttu-id="f730f-108">Les informations contenues dans la structure **PROPERTYINFO** sont utilisées lors de l’analyse d’une instance d’une propriété, ainsi que lors de la mise en forme des données affichées dans l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="f730f-108">The information in the **PROPERTYINFO** structure is used when parsing an instance of a property, and when formatting the data that is displayed in the Network Monitor UI.</span></span>

<span data-ttu-id="f730f-109">Moniteur réseau alloue les structures [**PROPERTYINST**](propertyinst.md) et [**PROPERTYINSTEX**](propertyinstex.md) lorsque l’analyseur attache une définition de propriété à une instance d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="f730f-109">Network Monitor allocates the [**PROPERTYINST**](propertyinst.md) and [**PROPERTYINSTEX**](propertyinstex.md) structures when the parser attaches a property definition to an instance of a property.</span></span>

<span data-ttu-id="f730f-110">La procédure suivante identifie les étapes nécessaires à l’attachement d’une définition de propriété.</span><span class="sxs-lookup"><span data-stu-id="f730f-110">The following procedure identifies the steps necessary to attach a property definition.</span></span>

<span data-ttu-id="f730f-111">**Pour attacher une définition de propriété**</span><span class="sxs-lookup"><span data-stu-id="f730f-111">**To attach a property definition**</span></span>

1.  <span data-ttu-id="f730f-112">Identifiez chaque propriété qui existe dans une instance du protocole.</span><span class="sxs-lookup"><span data-stu-id="f730f-112">Identify each property that exists in an instance of the protocol.</span></span> <span data-ttu-id="f730f-113">Lors de l’attachement d’une définition, Moniteur réseau transmet les données capturées à l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="f730f-113">When attaching a definition, Network Monitor passes the captured data to the parser.</span></span> <span data-ttu-id="f730f-114">Les données sont transmises sur la base d’une instance de protocole.</span><span class="sxs-lookup"><span data-stu-id="f730f-114">The data is passed on a protocol instance basis.</span></span>
2.  <span data-ttu-id="f730f-115">Déterminez l’emplacement de la propriété dans l’instance de protocole.</span><span class="sxs-lookup"><span data-stu-id="f730f-115">Determine the location of the property in the protocol instance.</span></span>
3.  <span data-ttu-id="f730f-116">Attachez une définition de propriété à l’emplacement de la propriété.</span><span class="sxs-lookup"><span data-stu-id="f730f-116">Attach a property definition to the property location.</span></span>

<span data-ttu-id="f730f-117">Moniteur réseau implémente une structure [**PROPERTYINST**](propertyinst.md) lorsque l’analyseur utilise les données de propriété telles qu’elles existent dans la capture.</span><span class="sxs-lookup"><span data-stu-id="f730f-117">Network Monitor implements a [**PROPERTYINST**](propertyinst.md) structure when the parser uses the property data as it exists in the capture.</span></span> <span data-ttu-id="f730f-118">Moniteur réseau implémente une structure [**PROPERTYINSTEX**](propertyinstex.md) lorsque l’analyseur doit modifier les données de la propriété dans la capture.</span><span class="sxs-lookup"><span data-stu-id="f730f-118">Network Monitor implements a [**PROPERTYINSTEX**](propertyinstex.md) structure when the parser must modify the property data in the capture.</span></span>

 

 



