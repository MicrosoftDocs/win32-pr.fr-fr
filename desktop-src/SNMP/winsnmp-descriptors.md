---
title: Descripteurs WinSNMP
description: Dans l’environnement de programmation WinSNMP, un descripteur est l’une des deux structures suivantes.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309442"
---
# <a name="winsnmp-descriptors"></a><span data-ttu-id="3f863-103">Descripteurs WinSNMP</span><span class="sxs-lookup"><span data-stu-id="3f863-103">WinSNMP Descriptors</span></span>

<span data-ttu-id="3f863-104">Dans l’environnement de programmation WinSNMP, un *descripteur* est l’une des deux structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="3f863-104">In the WinSNMP programming environment a *descriptor* is one of the following two structures:</span></span>

-   <span data-ttu-id="3f863-105">Une structure [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) qui décrit une variable de chaîne d’octets</span><span class="sxs-lookup"><span data-stu-id="3f863-105">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure which describes an octet string variable</span></span>
-   <span data-ttu-id="3f863-106">Une structure [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) qui décrit une variable d’identificateur d’objet SNMP</span><span class="sxs-lookup"><span data-stu-id="3f863-106">An [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure which describes an SNMP object identifier variable</span></span>

<span data-ttu-id="3f863-107">Un descripteur WinSNMP est une structure qui a deux membres : un membre de longueur, **Len** et un membre de pointeur, **ptr**.</span><span class="sxs-lookup"><span data-stu-id="3f863-107">A WinSNMP descriptor is a structure that has two members: a length member, **len**, and a pointer member, **ptr**.</span></span> <span data-ttu-id="3f863-108">Le membre **ptr** pointe vers la chaîne d’octets ou l’identificateur d’objet qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="3f863-108">The **ptr** member points to the octet string or object identifier of interest.</span></span> <span data-ttu-id="3f863-109">Le membre **ptr** peut être le type de données **smiLPBYTE** ou **smiLPUINT32** .</span><span class="sxs-lookup"><span data-stu-id="3f863-109">The **ptr** member can be either the **smiLPBYTE** or **smiLPUINT32** data type.</span></span>

<span data-ttu-id="3f863-110">Un descripteur [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) ou un descripteur [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) peut être le membre **value** d’une structure **smiVALUE** .</span><span class="sxs-lookup"><span data-stu-id="3f863-110">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor or an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) descriptor can be the **value** member of an **smiVALUE** structure.</span></span> <span data-ttu-id="3f863-111">La structure [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) décrit la valeur associée à un nom de variable dans une entrée de liaison de variable.</span><span class="sxs-lookup"><span data-stu-id="3f863-111">The [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure describes the value associated with a variable name in a variable binding entry.</span></span>

<span data-ttu-id="3f863-112">L’implémentation de l’WinSNMP Microsoft alloue et libère de la mémoire pour toutes les structures **smiOCTETS** et **smiOID** de sortie.</span><span class="sxs-lookup"><span data-stu-id="3f863-112">The Microsoft WinSNMP implementation allocates and deallocates memory for all output **smiOCTETS** and **smiOID** structures.</span></span> <span data-ttu-id="3f863-113">Par conséquent, l’application doit appeler la fonction [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) pour libérer la mémoire pour le membre **ptr** de ces structures.</span><span class="sxs-lookup"><span data-stu-id="3f863-113">Therefore, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free the memory for the **ptr** member of these structures.</span></span>

<span data-ttu-id="3f863-114">Les membres de chaîne dans les descripteurs ne requièrent pas d’octet de fin **null** .</span><span class="sxs-lookup"><span data-stu-id="3f863-114">String members in descriptors do not require a **NULL** terminating byte.</span></span> <span data-ttu-id="3f863-115">Pour plus d’informations sur la gestion de la mémoire allouée pour les descripteurs, consultez [allocation d’objets mémoire WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3f863-115">For additional information about managing the memory allocated for descriptors, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




