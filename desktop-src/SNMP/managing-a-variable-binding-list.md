---
title: Gestion d’une liste de liaisons de variables
description: La fonction SnmpGetVb récupère les informations de liaison de variable d’une liste de liaisons de variables. La fonction récupère le nom de la variable et la valeur associée à la variable à partir de l’entrée de liaison de variable spécifiée par l’application WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028963"
---
# <a name="managing-a-variable-binding-list"></a><span data-ttu-id="06c81-104">Gestion d’une liste de liaisons de variables</span><span class="sxs-lookup"><span data-stu-id="06c81-104">Managing a Variable Binding List</span></span>

<span data-ttu-id="06c81-105">La fonction [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) récupère les informations de liaison de variable d’une liste de liaisons de variables.</span><span class="sxs-lookup"><span data-stu-id="06c81-105">The [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) function retrieves variable binding information from a variable binding list.</span></span> <span data-ttu-id="06c81-106">La fonction récupère le nom de la variable et la valeur associée à la variable à partir de l’entrée de liaison de variable spécifiée par l’application WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="06c81-106">The function retrieves the variable name and the variable's associated value from the variable binding entry specified by the WinSNMP application.</span></span>

<span data-ttu-id="06c81-107">Pour mettre à jour les entrées de liaison de variable dans une liste de liaisons de variables, appelez la fonction [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) .</span><span class="sxs-lookup"><span data-stu-id="06c81-107">To update variable binding entries in a variable binding list, call the [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) function.</span></span> <span data-ttu-id="06c81-108">La fonction **SnmpSetVb** ajoute également de nouvelles entrées de liaison de variable à une liste de liaisons de variables existante.</span><span class="sxs-lookup"><span data-stu-id="06c81-108">The **SnmpSetVb** function also appends new variable binding entries to an existing variable binding list.</span></span>

<span data-ttu-id="06c81-109">L’application WinSNMP doit appeler la fonction [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) pour supprimer les entrées d’une liste de liaisons de variables.</span><span class="sxs-lookup"><span data-stu-id="06c81-109">The WinSNMP application must call the [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) function to remove entries from a variable binding list.</span></span>

<span data-ttu-id="06c81-110">Pour récupérer, modifier ou supprimer une entrée de liaison de variable, l’application WinSNMP doit spécifier la position de l’entrée dans la liste des liaisons de variables.</span><span class="sxs-lookup"><span data-stu-id="06c81-110">To retrieve, modify or delete a variable binding entry, the WinSNMP application must specify the position of the entry in the variable binding list.</span></span>

<span data-ttu-id="06c81-111">Un appel à la fonction [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) associe une liste de liaisons de variables à un PDU.</span><span class="sxs-lookup"><span data-stu-id="06c81-111">A call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function associates a variable binding list with a PDU.</span></span> <span data-ttu-id="06c81-112">Un appel à la fonction [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) récupère une liste de liaisons de variables à partir d’une PDU.</span><span class="sxs-lookup"><span data-stu-id="06c81-112">A call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function retrieves a variable binding list from a PDU.</span></span> <span data-ttu-id="06c81-113">Une liaison de variable individuelle n’est pas directement associée à un PDU, mais elle est indirectement associée par son inclusion dans une liste de liaisons de variables.</span><span class="sxs-lookup"><span data-stu-id="06c81-113">An individual variable binding is not directly associated with a PDU, but it is indirectly associated through its inclusion in a variable binding list.</span></span>

 

 




