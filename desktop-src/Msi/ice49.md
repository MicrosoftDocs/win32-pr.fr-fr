---
description: ICE49 recherche les entrées de Registre par défaut qui ne sont pas de type de Registre \_ sz.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867294"
---
# <a name="ice49"></a><span data-ttu-id="3af38-103">ICE49</span><span class="sxs-lookup"><span data-stu-id="3af38-103">ICE49</span></span>

<span data-ttu-id="3af38-104">ICE49 recherche les entrées de Registre par défaut qui ne sont pas de type de Registre **\_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="3af38-104">ICE49 checks for default registry entries that are not a **REG\_SZ** type.</span></span>

## <a name="result"></a><span data-ttu-id="3af38-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="3af38-105">Result</span></span>

<span data-ttu-id="3af38-106">ICE49 publie un avertissement s’il existe une entrée de Registre par défaut qui n’est pas un type de Registre **\_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="3af38-106">ICE49 posts an warning if there is a default registry entry that is not a **REG\_SZ** type.</span></span>

## <a name="example"></a><span data-ttu-id="3af38-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="3af38-107">Example</span></span>

<span data-ttu-id="3af38-108">ICE49 signale l’avertissement suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="3af38-108">ICE49 reports the following warning for the example shown.</span></span>

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

<span data-ttu-id="3af38-109">La valeur « \# 123 » est une valeur de Registre **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="3af38-109">The value '\#123' is a **DWORD** registry value.</span></span>

<span data-ttu-id="3af38-110">[Table du Registre](registry-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="3af38-110">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="3af38-111">Registre</span><span class="sxs-lookup"><span data-stu-id="3af38-111">Registry</span></span> | <span data-ttu-id="3af38-112">Nom</span><span class="sxs-lookup"><span data-stu-id="3af38-112">Name</span></span> | <span data-ttu-id="3af38-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="3af38-113">Value</span></span> |
|----------|------|-------|
| <span data-ttu-id="3af38-114">Reg1</span><span class="sxs-lookup"><span data-stu-id="3af38-114">Reg1</span></span>     |      | <span data-ttu-id="3af38-115">\#123</span><span class="sxs-lookup"><span data-stu-id="3af38-115">\#123</span></span> |



 

<span data-ttu-id="3af38-116">Pour résoudre cet avertissement, remplacez la valeur par tapez **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="3af38-116">To fix this warning, change the value to type **REG\_SZ**.</span></span>

<span data-ttu-id="3af38-117">Les composants avec des **\_ SZS** non-reg sont valides.</span><span class="sxs-lookup"><span data-stu-id="3af38-117">Components with non-**REG\_SZ** are valid.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3af38-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3af38-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3af38-119">Syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="3af38-119">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="3af38-120">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="3af38-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



