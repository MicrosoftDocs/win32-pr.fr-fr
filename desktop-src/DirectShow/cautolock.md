---
description: La classe CAutoLock contient une section critique pour l’étendue d’un bloc de code.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: CAutoLock, classe (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525472"
---
# <a name="cautolock-class"></a><span data-ttu-id="32d91-103">CAutoLock, classe</span><span class="sxs-lookup"><span data-stu-id="32d91-103">CAutoLock class</span></span>

<span data-ttu-id="32d91-104">La `CAutoLock` classe contient une section critique pour la portée d’un bloc de code.</span><span class="sxs-lookup"><span data-stu-id="32d91-104">The `CAutoLock` class holds a critical section for the scope of a code block.</span></span>

<span data-ttu-id="32d91-105">Cette classe fonctionne conjointement avec la classe [**CCritSec**](ccritsec.md) , qui est un wrapper pour les objets de section critiques.</span><span class="sxs-lookup"><span data-stu-id="32d91-105">This class works in conjunction with the [**CCritSec**](ccritsec.md) class, which is a wrapper for critical section objects.</span></span> <span data-ttu-id="32d91-106">Le `CAutoLock` constructeur verrouille la section critique et le destructeur le déverrouille.</span><span class="sxs-lookup"><span data-stu-id="32d91-106">The `CAutoLock` constructor locks the critical section, and the destructor unlocks it.</span></span> <span data-ttu-id="32d91-107">En utilisant un `CAutoLock` objet en tant que variable locale, vous pouvez verrouiller une section critique avec la garantie que tous les chemins de code déverrouilleront la section critique.</span><span class="sxs-lookup"><span data-stu-id="32d91-107">By using a `CAutoLock` object as a local variable, you can lock a critical section with the guarantee that all code paths will unlock the critical section.</span></span>

<span data-ttu-id="32d91-108">L’exemple de code suivant montre comment utiliser cette classe :</span><span class="sxs-lookup"><span data-stu-id="32d91-108">The following code example shows how to use this class:</span></span>


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



<span data-ttu-id="32d91-109">Les méthodes de cette classe ne sont pas conçues pour être substituées.</span><span class="sxs-lookup"><span data-stu-id="32d91-109">The methods in this class are not designed to be overridden.</span></span>



| <span data-ttu-id="32d91-110">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="32d91-110">Protected Member Variables</span></span>                 | <span data-ttu-id="32d91-111">Description</span><span class="sxs-lookup"><span data-stu-id="32d91-111">Description</span></span>                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="32d91-112">**m \_ pLock**</span><span class="sxs-lookup"><span data-stu-id="32d91-112">**m\_pLock**</span></span>](cautolock-m-plock.md)      | <span data-ttu-id="32d91-113">Section critique pour ce verrou.</span><span class="sxs-lookup"><span data-stu-id="32d91-113">Critical section for this lock.</span></span>                                  |
| <span data-ttu-id="32d91-114">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="32d91-114">Public Methods</span></span>                             | <span data-ttu-id="32d91-115">Description</span><span class="sxs-lookup"><span data-stu-id="32d91-115">Description</span></span>                                                      |
| [<span data-ttu-id="32d91-116">**CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="32d91-116">**CAutoLock**</span></span>](cautolock-cautolock.md)   | <span data-ttu-id="32d91-117">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="32d91-117">Constructor method.</span></span> <span data-ttu-id="32d91-118">Verrouille l’objet de section critique spécifié.</span><span class="sxs-lookup"><span data-stu-id="32d91-118">Locks the specified critical section object.</span></span> |
| [<span data-ttu-id="32d91-119">**~ CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="32d91-119">**~CAutoLock**</span></span>](cautolock--cautolock.md) | <span data-ttu-id="32d91-120">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="32d91-120">Destructor method.</span></span> <span data-ttu-id="32d91-121">Déverrouille l’objet de section critique.</span><span class="sxs-lookup"><span data-stu-id="32d91-121">Unlocks the critical section object.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="32d91-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32d91-122">Requirements</span></span>



| <span data-ttu-id="32d91-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32d91-123">Requirement</span></span> | <span data-ttu-id="32d91-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="32d91-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32d91-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="32d91-125">Header</span></span><br/>  | <dl> <span data-ttu-id="32d91-126"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32d91-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="32d91-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="32d91-127">Library</span></span><br/> | <dl> <span data-ttu-id="32d91-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="32d91-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




