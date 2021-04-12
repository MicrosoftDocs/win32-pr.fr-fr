---
description: 'En savoir plus sur : structure JET_SETSYSPARAM'
title: Structure JET_SETSYSPARAM
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318173"
---
# <a name="jet_setsysparam-structure"></a><span data-ttu-id="cc2d9-103">Structure JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="cc2d9-103">JET_SETSYSPARAM Structure</span></span>


<span data-ttu-id="cc2d9-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="cc2d9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setsysparam-structure"></a><span data-ttu-id="cc2d9-105">Structure JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="cc2d9-105">JET_SETSYSPARAM Structure</span></span>

<span data-ttu-id="cc2d9-106">Un tableau de structures de **JET_SETSYSPARAM** indique un ensemble spécifique de paramètres système globaux définis comme argument lors de l’utilisation de la fonction [JetEnableMultiInstance](./jetenablemultiinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2d9-106">An array of **JET_SETSYSPARAM** structures indicate a specific set of global system parameters that are set as an argument when using the [JetEnableMultiInstance](./jetenablemultiinstance-function.md) function.</span></span>

<span data-ttu-id="cc2d9-107">**Windows XP :** Cette structure est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-107">**Windows XP:** This structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a><span data-ttu-id="cc2d9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cc2d9-108">Members</span></span>

<span data-ttu-id="cc2d9-109">**paramid**</span><span class="sxs-lookup"><span data-stu-id="cc2d9-109">**paramid**</span></span>

<span data-ttu-id="cc2d9-110">ID du paramètre système qui sera défini.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-110">The ID of the system parameter that will be set.</span></span>

<span data-ttu-id="cc2d9-111">Pour obtenir la liste complète des paramètres système et leurs propriétés, consultez [paramètres système du moteur de stockage extensible](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2d9-111">See [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="cc2d9-112">**lParam**</span><span class="sxs-lookup"><span data-stu-id="cc2d9-112">**lParam**</span></span>

<span data-ttu-id="cc2d9-113">Valeur facultative à définir pour le paramètre système sélectionné si ce paramètre système est d’un type entier.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-113">The optional value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="cc2d9-114">**SZ**</span><span class="sxs-lookup"><span data-stu-id="cc2d9-114">**sz**</span></span>

<span data-ttu-id="cc2d9-115">Valeur facultative à définir pour le paramètre système sélectionné si ce paramètre système est un type chaîne.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-115">The optional value to be set for the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="cc2d9-116">**Raise**</span><span class="sxs-lookup"><span data-stu-id="cc2d9-116">**err**</span></span>

<span data-ttu-id="cc2d9-117">Erreur résultant de l’appel à [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec les paramètres spécifiés précédemment.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-117">The error resulting from the call to [JetSetSystemParameter](./jetsetsystemparameter-function.md) with the previously specified parameters.</span></span>

### <a name="requirements"></a><span data-ttu-id="cc2d9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc2d9-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc2d9-119"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cc2d9-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cc2d9-120">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc2d9-121"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="cc2d9-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cc2d9-122">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc2d9-123"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="cc2d9-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cc2d9-124">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="cc2d9-124">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc2d9-125"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="cc2d9-125"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="cc2d9-126">Implémenté comme <strong>JET_ SETSYSPARAM_W</strong> (Unicode) et <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="cc2d9-126">Implemented as <strong>JET_ SETSYSPARAM_W</strong> (Unicode) and <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="cc2d9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc2d9-127">See Also</span></span>

[<span data-ttu-id="cc2d9-128">Paramètres système du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="cc2d9-128">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)  
[<span data-ttu-id="cc2d9-129">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="cc2d9-129">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="cc2d9-130">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cc2d9-130">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cc2d9-131">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="cc2d9-131">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="cc2d9-132">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="cc2d9-132">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
