---
title: Utilisation des listes de liaisons de variables
description: Une liaison de variable correspond à l’Association d’un nom d’instance d’objet SNMP à une valeur associée. Une liste de liaisons de variables est une série d’entrées de liaison de variable. Dans WinSNMP, une unité de données de protocole (PDU) comprend une liste de liaisons de variables.
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- Utilisation des listes de liaisons de variables SNMP
- Liste de liaisons de variables SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723666"
---
# <a name="working-with-variable-binding-lists"></a><span data-ttu-id="a8cc1-107">Utilisation des listes de liaisons de variables</span><span class="sxs-lookup"><span data-stu-id="a8cc1-107">Working with Variable Binding Lists</span></span>

<span data-ttu-id="a8cc1-108">Une *liaison de variable* correspond à l’Association d’un nom d’instance d’objet SNMP à une valeur associée.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-108">A *variable binding* is the pairing of an SNMP object instance name with an associated value.</span></span> <span data-ttu-id="a8cc1-109">Une *liste de liaisons de variables* est une série d’entrées de liaison de variable.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-109">A *variable binding list* is a series of variable binding entries.</span></span> <span data-ttu-id="a8cc1-110">Dans WinSNMP, une unité de données de protocole (PDU) comprend une liste de liaisons de variables.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-110">In WinSNMP, a protocol data unit (PDU) includes a variable binding list.</span></span>

<span data-ttu-id="a8cc1-111">Les détails de la structure de la liste de liaisons de variables sont limités à l’implémentation de l’WinSNMP Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-111">The details of the variable binding list structure are restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="a8cc1-112">Une application WinSNMP peut accéder à une liste de liaisons de variables avec un handle de type **HSNMP \_ VBL**.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-112">A WinSNMP application can access a variable binding list with a handle of type **HSNMP\_VBL**.</span></span> <span data-ttu-id="a8cc1-113">Pour plus d’informations, consultez [objets descripteur de ressource](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a8cc1-113">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="a8cc1-114">L’application WinSNMP peut construire et manipuler des listes de liaisons de variables, et les inclure dans des PDU.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-114">The WinSNMP application can construct and manipulate variable binding lists, and include them in PDUs.</span></span> <span data-ttu-id="a8cc1-115">Pour effectuer ces opérations, l’application utilise les [fonctions de liaison de variable](winsnmp-functions.md)winsnmp.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-115">To perform these operations, the application uses the WinSNMP [variable binding functions](winsnmp-functions.md).</span></span> <span data-ttu-id="a8cc1-116">Pour plus d’informations sur l’utilisation des listes de liaisons de variables et WinSNMP, consultez les rubriques répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-116">For more information about working with WinSNMP and variable binding lists, see the topics listed in the following table.</span></span>



| <span data-ttu-id="a8cc1-117">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a8cc1-117">Topic</span></span>                                                                    | <span data-ttu-id="a8cc1-118">Description</span><span class="sxs-lookup"><span data-stu-id="a8cc1-118">Description</span></span>                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="a8cc1-119">Création d’une liste de liaisons de variables</span><span class="sxs-lookup"><span data-stu-id="a8cc1-119">Creating a Variable Binding List</span></span>](creating-a-variable-binding-list.md) | <span data-ttu-id="a8cc1-120">Décrit comment créer une liste de liaisons de variables.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-120">Describes how to create a variable binding list.</span></span> |
| [<span data-ttu-id="a8cc1-121">Gestion d’une liste de liaisons de variables</span><span class="sxs-lookup"><span data-stu-id="a8cc1-121">Managing a Variable Binding List</span></span>](managing-a-variable-binding-list.md) | <span data-ttu-id="a8cc1-122">Décrit comment gérer une liste de liaisons de variables.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-122">Describes how to manage a variable binding list.</span></span> |



 

<span data-ttu-id="a8cc1-123">Pour plus d’informations sur les liaisons de variables et les listes de liaisons de variables, consultez [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), « protocole Operations for version 2 of simple Network Management Protocol (SNMPv2) » et les [fonctions de liaison de variable](winsnmp-functions.md)winsnmp.</span><span class="sxs-lookup"><span data-stu-id="a8cc1-123">For more information about variable bindings and variable binding lists, see [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "Protocol Operations for Version 2 of the Simple Network Management Protocol (SNMPv2)," and the WinSNMP [Variable Binding Functions](winsnmp-functions.md).</span></span>

 

 




