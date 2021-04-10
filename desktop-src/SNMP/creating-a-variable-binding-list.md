---
title: Création d’une liste de liaisons de variables
description: La fonction SnmpCreateVbl crée une nouvelle liste de liaisons de variables.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196898"
---
# <a name="creating-a-variable-binding-list"></a><span data-ttu-id="47756-103">Création d’une liste de liaisons de variables</span><span class="sxs-lookup"><span data-stu-id="47756-103">Creating a Variable Binding List</span></span>

<span data-ttu-id="47756-104">La fonction [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) crée une nouvelle liste de liaisons de variables.</span><span class="sxs-lookup"><span data-stu-id="47756-104">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function creates a new variable binding list.</span></span> <span data-ttu-id="47756-105">Si l’application WinSNMP spécifie un nom de variable et une valeur, la fonction crée la liste et ajoute le nom et la valeur comme première entrée de la liste.</span><span class="sxs-lookup"><span data-stu-id="47756-105">If the WinSNMP application specifies a variable name and a value, the function creates the list and adds the name and value as the first entry in the list.</span></span> <span data-ttu-id="47756-106">Si l’application spécifie la **valeur null** pour le nom de la variable, la fonction crée une liste vide.</span><span class="sxs-lookup"><span data-stu-id="47756-106">If the application specifies **NULL** for the variable name, the function creates an empty list.</span></span>

<span data-ttu-id="47756-107">Pour copier une liste de liaisons de variables, appelez la fonction [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) .</span><span class="sxs-lookup"><span data-stu-id="47756-107">To copy a variable binding list, call the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function.</span></span> <span data-ttu-id="47756-108">La fonction crée une nouvelle liste de liaisons de variables et initialise la nouvelle liste à l’aide d’une copie des données dans la liste de liaisons de la variable source.</span><span class="sxs-lookup"><span data-stu-id="47756-108">The function creates a new variable binding list and initializes the new list with a copy of the data in the source variable binding list.</span></span>

<span data-ttu-id="47756-109">La fonction [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) et la fonction [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) allouent toute mémoire nécessaire pour la nouvelle liste de liaisons de variables.</span><span class="sxs-lookup"><span data-stu-id="47756-109">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function and the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function allocate any necessary memory for the new variable binding list.</span></span> <span data-ttu-id="47756-110">L’application WinSNMP doit libérer les ressources associées à ces listes.</span><span class="sxs-lookup"><span data-stu-id="47756-110">The WinSNMP application must release the resources associated with these lists.</span></span> <span data-ttu-id="47756-111">Il est recommandé que l’application effectue cette opération en faisant correspondre chaque appel à [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) et [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) avec un appel correspondant à la fonction [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) lorsqu’il est approprié de libérer la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="47756-111">It is recommended that the application do this by matching each call to [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) and [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) with a corresponding call to the [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) function when it is appropriate to free the allocated memory.</span></span>

 

 




