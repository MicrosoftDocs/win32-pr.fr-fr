---
description: 'En savoir plus sur : structure JET_SNPROG'
title: Structure JET_SNPROG
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484265"
---
# <a name="jet_snprog-structure"></a><span data-ttu-id="01043-103">Structure JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="01043-103">JET_SNPROG Structure</span></span>


<span data-ttu-id="01043-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="01043-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snprog-structure"></a><span data-ttu-id="01043-105">Structure JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="01043-105">JET_SNPROG Structure</span></span>

<span data-ttu-id="01043-106">La structure **JET_SNPROG** contient des informations sur la progression d’une opération de longue durée.</span><span class="sxs-lookup"><span data-stu-id="01043-106">The **JET_SNPROG** structure contains information about the progress of a long-running operation.</span></span> <span data-ttu-id="01043-107">Lorsque la fonction de rappel est appelée pour notifier l’état de l’opération et que l’opération est toujours en cours, le dernier paramètre de la fonction de rappel est un pointeur vers une structure de **JET_SNPROG** .</span><span class="sxs-lookup"><span data-stu-id="01043-107">When the callback function is called to notify the status of the operation and the operation is still in progress, the last parameter of the callback function is a pointer to a **JET_SNPROG** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a><span data-ttu-id="01043-108">Membres</span><span class="sxs-lookup"><span data-stu-id="01043-108">Members</span></span>

<span data-ttu-id="01043-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="01043-109">**cbStruct**</span></span>

<span data-ttu-id="01043-110">Taille de la structure **JET_SNPROG** , en octets.</span><span class="sxs-lookup"><span data-stu-id="01043-110">The size of the **JET_SNPROG** structure, in bytes.</span></span> <span data-ttu-id="01043-111">Cette valeur confirme la présence des champs suivants.</span><span class="sxs-lookup"><span data-stu-id="01043-111">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="01043-112">**cunitDone**</span><span class="sxs-lookup"><span data-stu-id="01043-112">**cunitDone**</span></span>

<span data-ttu-id="01043-113">Nombre d’unités de travail déjà terminées pendant la fonction de longue durée.</span><span class="sxs-lookup"><span data-stu-id="01043-113">The number of work units that are already completed during the long running function.</span></span>

<span data-ttu-id="01043-114">**cunitTotal**</span><span class="sxs-lookup"><span data-stu-id="01043-114">**cunitTotal**</span></span>

<span data-ttu-id="01043-115">Nombre d’unités de travail qui doivent être terminées.</span><span class="sxs-lookup"><span data-stu-id="01043-115">The number of work units that need to be completed.</span></span> <span data-ttu-id="01043-116">Cette valeur doit toujours être supérieure ou égale à **cunitDone**.</span><span class="sxs-lookup"><span data-stu-id="01043-116">This value should always be bigger than or equal to **cunitDone**.</span></span>

### <a name="requirements"></a><span data-ttu-id="01043-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01043-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01043-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="01043-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="01043-119">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="01043-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01043-120"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="01043-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="01043-121">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="01043-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01043-122"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="01043-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="01043-123">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="01043-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

