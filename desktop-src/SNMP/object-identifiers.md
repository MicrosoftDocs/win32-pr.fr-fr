---
title: Identificateurs d’objets (SNMP)
description: Un identificateur d’objet SNMP désigne un objet de manière unique et identifie son emplacement dans une arborescence de base d’informations de gestion (MIB).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed1f54f67b85000e508dddb42b9c784628a53ab
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739332"
---
# <a name="object-identifiers-snmp"></a><span data-ttu-id="46ddd-103">Identificateurs d’objets (SNMP)</span><span class="sxs-lookup"><span data-stu-id="46ddd-103">Object Identifiers (SNMP)</span></span>

<span data-ttu-id="46ddd-104">Un identificateur d’objet SNMP désigne un objet de manière unique et identifie son emplacement dans une arborescence de base d’informations de gestion (MIB).</span><span class="sxs-lookup"><span data-stu-id="46ddd-104">An SNMP object identifier uniquely names an object and identifies its location within a Management Information Base (MIB) tree structure.</span></span> <span data-ttu-id="46ddd-105">Les identificateurs d’objet sont des types de données ASN. 1 (Abstract Syntax Notation One) indépendants de l’application qui se composent d’une séquence d’entiers non négatifs ou de sous-identificateurs.</span><span class="sxs-lookup"><span data-stu-id="46ddd-105">Object identifiers are application-independent Abstract Syntax Notation One (ASN.1) data types that consist of a sequence of non-negative integers, or subidentifiers.</span></span> <span data-ttu-id="46ddd-106">Les identificateurs d’objet doivent avoir au moins deux sous-identificateurs et ne doivent pas dépasser 128 sous-identificateurs.</span><span class="sxs-lookup"><span data-stu-id="46ddd-106">Object identifiers must have a minimum of two subidentifiers and they must not exceed 128 subidentifiers.</span></span>

<span data-ttu-id="46ddd-107">L’environnement de programmation WinSNMP utilise la structure [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) pour gérer les identificateurs d’objets.</span><span class="sxs-lookup"><span data-stu-id="46ddd-107">The WinSNMP programming environment uses the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure to manage object identifiers.</span></span> <span data-ttu-id="46ddd-108">Le format du tableau d’identificateur d’objet dans une structure **smiOID** est un sous-identificateur par élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="46ddd-108">The format of the object identifier array in an **smiOID** structure is one subidentifier per array element.</span></span>

<span data-ttu-id="46ddd-109">La représentation sous forme de chaîne numérique en pointillés d’un identificateur d’objet sépare ses sous-identificateurs par des points ; par exemple, « 1.2.3.4.5.6 ».</span><span class="sxs-lookup"><span data-stu-id="46ddd-109">The dotted numeric string representation of an object identifier separates its subidentifiers with periods; for example, "1.2.3.4.5.6".</span></span>

<span data-ttu-id="46ddd-110">Pour plus d’informations, consultez [la base de données MIB (Management Information base) SNMP](the-snmp-management-information-base-mib-.md) et les RFC correspondants.</span><span class="sxs-lookup"><span data-stu-id="46ddd-110">For more information, see [The SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) and the relevant RFCs.</span></span>

 

 




