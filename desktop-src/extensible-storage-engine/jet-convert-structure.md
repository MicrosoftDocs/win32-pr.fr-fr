---
description: 'En savoir plus sur : structure JET_CONVERT'
title: Structure JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863185"
---
# <a name="jet_convert-structure"></a><span data-ttu-id="9100a-103">Structure JET_CONVERT</span><span class="sxs-lookup"><span data-stu-id="9100a-103">JET_CONVERT Structure</span></span>


<span data-ttu-id="9100a-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="9100a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_convert-structure"></a><span data-ttu-id="9100a-105">Structure JET_CONVERT</span><span class="sxs-lookup"><span data-stu-id="9100a-105">JET_CONVERT Structure</span></span>

<span data-ttu-id="9100a-106">La structure **JET_CONVERT** contient le nom d’une dll de version ESE antérieure qui est utilisée pour lire les bases de données créées avec cette version antérieure.</span><span class="sxs-lookup"><span data-stu-id="9100a-106">The **JET_CONVERT** structure contains the name of an earlier ESE version DLL that is used for reading a databases that are created with that earlier version.</span></span> <span data-ttu-id="9100a-107">En outre, d’autres indicateurs sont fournis pour contrôler la nature de la conversion.</span><span class="sxs-lookup"><span data-stu-id="9100a-107">In addition, other flags are provided to control the nature of the conversion.</span></span>

<span data-ttu-id="9100a-108">**Windows Server 2003 :** La fonctionnalité de [JetCompact](./jetcompact-function.md) qui a effectué une conversion a été supprimée du produit dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9100a-108">**Windows Server 2003:** The feature in [JetCompact](./jetcompact-function.md) that performed a conversion was removed from the product in Windows Server 2003.</span></span> <span data-ttu-id="9100a-109">Il est uniquement pris en charge dans Windows 2000 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9100a-109">It is only supported in Windows 2000 and Windows XP.</span></span>

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a><span data-ttu-id="9100a-110">Membres</span><span class="sxs-lookup"><span data-stu-id="9100a-110">Members</span></span>

<span data-ttu-id="9100a-111">**SzOldDll**</span><span class="sxs-lookup"><span data-stu-id="9100a-111">**SzOldDll**</span></span>

<span data-ttu-id="9100a-112">Nom, y compris les informations de chemin d’accès, à la version antérieure de la DLL ESE.</span><span class="sxs-lookup"><span data-stu-id="9100a-112">The name, including path information, to the earlier version of the ESE DLL.</span></span>

<span data-ttu-id="9100a-113">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="9100a-113">**fFlags**</span></span>

<span data-ttu-id="9100a-114">Réservé pour le système.</span><span class="sxs-lookup"><span data-stu-id="9100a-114">Reserved for system use.</span></span>

<span data-ttu-id="9100a-115">**fSchemaChangesOnly**</span><span class="sxs-lookup"><span data-stu-id="9100a-115">**fSchemaChangesOnly**</span></span>

<span data-ttu-id="9100a-116">Réservé pour le système.</span><span class="sxs-lookup"><span data-stu-id="9100a-116">Reserved for system use.</span></span>

### <a name="requirements"></a><span data-ttu-id="9100a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9100a-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9100a-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9100a-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9100a-119">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="9100a-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9100a-120"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="9100a-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9100a-121">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9100a-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9100a-122"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="9100a-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9100a-123">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="9100a-123">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9100a-124"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9100a-124"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9100a-125">Implémenté comme <strong>JET_CONVERT_W</strong> (Unicode) et <strong>JET_CONVERT_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9100a-125">Implemented as <strong>JET_CONVERT_W</strong> (Unicode) and <strong>JET_CONVERT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9100a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9100a-126">See Also</span></span>

[<span data-ttu-id="9100a-127">JetCompact</span><span class="sxs-lookup"><span data-stu-id="9100a-127">JetCompact</span></span>](./jetcompact-function.md)
