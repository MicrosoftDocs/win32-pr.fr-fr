---
title: Opérations de Access Control et de lecture
description: La sécurité est un filtre implicite pour la recherche, l’énumération des conteneurs ou la lecture des propriétés.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Opérations de Access Control et de lecture AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028513"
---
# <a name="access-control-and-read-operations"></a><span data-ttu-id="e7ccf-104">Opérations de Access Control et de lecture</span><span class="sxs-lookup"><span data-stu-id="e7ccf-104">Access Control and Read Operations</span></span>

<span data-ttu-id="e7ccf-105">La sécurité est un filtre implicite pour la recherche, l’énumération des conteneurs ou la lecture des propriétés.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-105">Security is an implicit filter for searching, enumerating containers, or reading properties.</span></span> <span data-ttu-id="e7ccf-106">Si vous ne disposez pas des droits d’accès nécessaires, les tentatives d’énumération des objets ou de lecture des propriétés peuvent échouer avec les codes d’erreur suivants, même si l’objet ou la propriété existe :</span><span class="sxs-lookup"><span data-stu-id="e7ccf-106">If you do not have the necessary access rights, attempts to list objects or read properties can fail with the following error codes even thought the object or property exists:</span></span>

-   <span data-ttu-id="e7ccf-107">**\_objet domaine E ADS \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-107">**E\_ADS\_INVALID\_DOMAIN\_OBJECT**</span></span>
-   <span data-ttu-id="e7ccf-108">**\_propriété E \_ ADS \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-108">**E\_ADS\_PROPERTY\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="e7ccf-109">**\_propriété ADS \_ E \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-109">**E\_ADS\_PROPERTY\_NOT\_FOUND**</span></span>

<span data-ttu-id="e7ccf-110">N’oubliez pas qu’un appelant avec des **publicités appropriées à la \_ \_ \_ liste ACTRL DS \_ List** pour un conteneur peut énumérer les objets enfants dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-110">Be aware that a caller with **ADS\_RIGHT\_ACTRL\_DS\_LIST** access to a container can enumerate the child objects in the container.</span></span> <span data-ttu-id="e7ccf-111">Toutefois, une tentative d’accès à un objet enfant peut encore échouer avec une erreur telle que **E \_ ADS \_ \_ objet inconnu** si l’appelant n’a pas d' **\_ \_ objet de \_ \_ liste \_ ACTRL DS** pour accéder à l’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-111">But an attempt to access a child object can still fail with an error such as **E\_ADS\_UNKNOWN\_OBJECT** if the caller does not have **ADS\_RIGHT\_ACTRL\_DS\_LIST\_OBJECT** access to the child object.</span></span>

<span data-ttu-id="e7ccf-112">L’impact de la sécurité sur les opérations de lecture n’est pas nécessairement représenté par une erreur.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-112">The impact of security on read operations is not necessarily manifested as an error.</span></span> <span data-ttu-id="e7ccf-113">Par exemple, une opération de recherche peut être effectuée, mais les résultats de la recherche n’incluent pas les objets ou les propriétés auxquels l’appelant n’a pas accès.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-113">For example, a search operation can succeed, but the search results do not include objects or properties to which the caller does not have access.</span></span>

 

 




