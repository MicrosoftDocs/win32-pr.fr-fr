---
title: Gestion des identificateurs d’objets
description: L’API WinSNMP fournit plusieurs fonctions utilitaires WinSNMP qui simplifient la manipulation des identificateurs d’objet pour les applications WinSNMP.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462407"
---
# <a name="managing-object-identifiers"></a><span data-ttu-id="18eb9-103">Gestion des identificateurs d’objets</span><span class="sxs-lookup"><span data-stu-id="18eb9-103">Managing Object Identifiers</span></span>

<span data-ttu-id="18eb9-104">L’API WinSNMP fournit plusieurs [fonctions utilitaires WinSNMP](winsnmp-functions.md) qui simplifient la manipulation des identificateurs d’objet pour les applications winsnmp.</span><span class="sxs-lookup"><span data-stu-id="18eb9-104">The WinSNMP API provides several [WinSNMP utility functions](winsnmp-functions.md) that simplify the manipulation of object identifiers for WinSNMP applications.</span></span>

<span data-ttu-id="18eb9-105">La fonction [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) convertit la représentation binaire interne d’un identificateur d’objet en son format de chaîne numérique en pointillés.</span><span class="sxs-lookup"><span data-stu-id="18eb9-105">The [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) function converts the internal binary representation of an object identifier to its dotted numeric string format.</span></span> <span data-ttu-id="18eb9-106">Quand vous appelez [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), spécifiez une mémoire tampon de chaîne de longueur MAXOBJIDSTRSIZE (1408 octets) pour vous assurer que la mémoire tampon de sortie est suffisamment grande pour contenir la chaîne convertie.</span><span class="sxs-lookup"><span data-stu-id="18eb9-106">When you call [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), specify a string buffer of MAXOBJIDSTRSIZE length (1408 bytes) to ensure that the output buffer is large enough to hold the converted string.</span></span> <span data-ttu-id="18eb9-107">Pour convertir un identificateur d’objet à partir du format de chaîne numérique avec points en sa représentation binaire interne, appelez la fonction [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) .</span><span class="sxs-lookup"><span data-stu-id="18eb9-107">To convert an object identifier from the dotted numeric string format to its internal binary representation, call the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) function.</span></span>

<span data-ttu-id="18eb9-108">Pour copier un identificateur d’objet SNMP, appelez la fonction [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .</span><span class="sxs-lookup"><span data-stu-id="18eb9-108">To copy an SNMP object identifier call the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) function.</span></span> <span data-ttu-id="18eb9-109">Cette fonction alloue la mémoire nécessaire pour le nouvel identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="18eb9-109">This function allocates any necessary memory for the new object identifier.</span></span>

<span data-ttu-id="18eb9-110">Une application WinSNMP doit appeler la fonction [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) pour libérer les ressources allouées pour le membre **ptr** de la structure [**SmiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) spécifiée par les fonctions [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) et [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .</span><span class="sxs-lookup"><span data-stu-id="18eb9-110">A WinSNMP application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free resources allocated for the **ptr** member of the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure specified by both the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) and the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) functions.</span></span>

<span data-ttu-id="18eb9-111">La fonction [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) compare deux identificateurs d’objet SNMP.</span><span class="sxs-lookup"><span data-stu-id="18eb9-111">The [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) function compares two SNMP object identifiers.</span></span> <span data-ttu-id="18eb9-112">L’application WinSNMP peut spécifier le nombre de sous-identificateurs à comparer.</span><span class="sxs-lookup"><span data-stu-id="18eb9-112">The WinSNMP application can specify the number of subidentifiers to compare.</span></span> <span data-ttu-id="18eb9-113">Appelez **SnmpOidCompare** pour déterminer si deux identificateurs d’objet ont des préfixes communs.</span><span class="sxs-lookup"><span data-stu-id="18eb9-113">Call **SnmpOidCompare** to determine whether two object identifiers have common prefixes.</span></span>

<span data-ttu-id="18eb9-114">Pour plus d’informations sur la gestion de la mémoire allouée pour les identificateurs d’objets, consultez [allocation d’objets mémoire WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="18eb9-114">For additional information about managing the memory allocated for object identifiers, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




