---
title: Configuration des limites de durée de vie
description: Un client peut demander une valeur de durée de vie pour une entrée allant de 1 à 31557600 (c’est-à-dire de 1 seconde à 1 an).
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Configuration des limites de durée de vie AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cb3617bd59667f0284c4e383da54752adfbe25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670997"
---
# <a name="configuration-of-ttl-limits"></a><span data-ttu-id="f8230-104">Configuration des limites de durée de vie</span><span class="sxs-lookup"><span data-stu-id="f8230-104">Configuration of TTL Limits</span></span>

<span data-ttu-id="f8230-105">Un client peut demander une valeur de durée de vie pour une entrée allant de 1 à 31557600 (c’est-à-dire de 1 seconde à 1 an).</span><span class="sxs-lookup"><span data-stu-id="f8230-105">A client can request a TTL value for an entry ranging between 1 and 31557600 (that is, from 1 second to 1 year).</span></span> <span data-ttu-id="f8230-106">Cette plage de valeurs d’attribut sera appliquée par les valeurs d’attribut **rangeLower** et **rangeUpper** dans la définition de **schéma** d’attribut pour l’attribut **entryTTL** .</span><span class="sxs-lookup"><span data-stu-id="f8230-106">This attribute value range will be enforced by the **rangeLower** and **rangeUpper** attribute values in the **attributeSchema** definition for the **entryTTL** attribute.</span></span> <span data-ttu-id="f8230-107">Conformément à la norme RFC 2589, les serveurs d’annuaire n’ont pas besoin d’accepter cette valeur et peuvent renvoyer une valeur TTL différente au client.</span><span class="sxs-lookup"><span data-stu-id="f8230-107">As per RFC 2589, directory servers are not required to accept this value and might return a different TTL value to the client.</span></span> <span data-ttu-id="f8230-108">Les clients doivent être en mesure d’utiliser cette valeur dictée par le serveur, car leur période d’actualisation du client (CRP), qui régit la fréquence à laquelle le client doit effectuer l’opération d’actualisation sur l’entrée dynamique.</span><span class="sxs-lookup"><span data-stu-id="f8230-108">Clients must be able to use this server-dictated value as their client refresh period (CRP) which will govern how often the client will need to perform the refresh operation on the dynamic entry.</span></span>

<span data-ttu-id="f8230-109">Active Directory Domain Services fournir aux administrateurs la possibilité de configurer les valeurs de durée de vie par défaut et minimale pour une forêt.</span><span class="sxs-lookup"><span data-stu-id="f8230-109">Active Directory Domain Services provide administrators with the ability to configure the default and minimum TTL values for a forest.</span></span> <span data-ttu-id="f8230-110">La valeur TTL par défaut est celle qui sera affectée à une entrée dynamique nouvellement créée si une durée de vie n’est pas explicitement spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8230-110">The default TTL value is what will be assigned to a newly created dynamic entry if a TTL is not explicitly specified.</span></span> <span data-ttu-id="f8230-111">La durée de vie minimale remplace toute valeur TTL spécifiée par le client inférieure à la valeur minimale configurée.</span><span class="sxs-lookup"><span data-stu-id="f8230-111">The minimum TTL will override any client specified TTL value that is lower than the configured minimum.</span></span> <span data-ttu-id="f8230-112">Aucune valeur de durée de vie maximale configurable ne doit être fournie, car un maximum est imposé par la valeur d’attribut **rangeUpper** dans l’objet **attributeSchema** .</span><span class="sxs-lookup"><span data-stu-id="f8230-112">No configurable maximum TTL value needs to be provided because a maximum will be imposed by the **rangeUpper** attribute value in the **attributeSchema** object.</span></span> <span data-ttu-id="f8230-113">Permettre aux administrateurs de configurer ces valeurs leur permettra de définir des valeurs de durée de vie qui appliqueront un trafic d’actualisation faible ou, à l’autre extrême, fournira un répertoire très à jour.</span><span class="sxs-lookup"><span data-stu-id="f8230-113">Allowing administrators to configure these values will enable them to set TTL values which will enforce a low refresh traffic or, at the other extreme, provide a highly up-to-date directory.</span></span>

<span data-ttu-id="f8230-114">Les valeurs par défaut pour les deux paramètres TTL configurables sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8230-114">The default values for the two configurable TTL parameters will be as follows:</span></span>

-   <span data-ttu-id="f8230-115">Valeur TTL par défaut = 86400 secondes (1 jour)</span><span class="sxs-lookup"><span data-stu-id="f8230-115">Default TTL value = 86400 seconds (1 day)</span></span>
-   <span data-ttu-id="f8230-116">Valeur TTL minimale = 900 secondes (15 minutes)</span><span class="sxs-lookup"><span data-stu-id="f8230-116">Minimum TTL value = 900 seconds (15 minutes)</span></span>

<span data-ttu-id="f8230-117">Les paramètres TTL configurables sont stockés sous la forme d’entrées AVA (attribute value assertion) au format «<Value-Name>=</span><span class="sxs-lookup"><span data-stu-id="f8230-117">The configurable TTL parameters will be stored as AVA (attribute value assertion) entries of the form "<value-name>=</span></span><value><span data-ttu-id="f8230-118">"dans l’attribut **ms-DS-Other-Settings** de l’objet NTDS-Service donné par le nom de domaine suivant dans la partition de configuration :</span><span class="sxs-lookup"><span data-stu-id="f8230-118">" in the attribute **ms-DS-Other-Settings** of the NTDS-Service object given by the following DN in the Configuration partition:</span></span>


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



<span data-ttu-id="f8230-119">La syntaxe d’AVA exacte, pour les deux paramètres TTL configurables, est la suivante, où NNNN est exprimé en secondes :</span><span class="sxs-lookup"><span data-stu-id="f8230-119">The exact AVA syntax, for the two configurable TTL parameters, is as follows where NNNN is expressed in seconds:</span></span>


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



<span data-ttu-id="f8230-120">Ces valeurs peuvent être définies par un administrateur via l’utilitaire de ligne de commande Ntdsutil.</span><span class="sxs-lookup"><span data-stu-id="f8230-120">These values can be set by an administrator through the command-line utility ntdsutil.</span></span>

 

 




