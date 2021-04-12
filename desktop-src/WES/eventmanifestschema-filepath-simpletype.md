---
title: filePath (type simple)
description: Définit une chaîne qui contient un chemin d’accès qualifié complet à un fichier.
ms.assetid: a9b8f40a-fecd-4325-b068-a5aca3133134
keywords:
- filePath type simple EventLog
topic_type:
- apiref
api_name:
- filePath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 492580634c1a48c88df6f50de2582c215ec7ecb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464570"
---
# <a name="filepath-simple-type"></a><span data-ttu-id="5074a-104">filePath (type simple)</span><span class="sxs-lookup"><span data-stu-id="5074a-104">filePath Simple Type</span></span>

<span data-ttu-id="5074a-105">Définit une chaîne qui contient un chemin d’accès qualifié complet à un fichier.</span><span class="sxs-lookup"><span data-stu-id="5074a-105">Defines a string that contains a fully qualified path to a file.</span></span> <span data-ttu-id="5074a-106">Le chemin d’accès peut contenir des variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="5074a-106">The path may contain environment variables.</span></span>

``` syntax
<xs:simpleType name="filePath">
    <xs:restriction
        base="xs:string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="5074a-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5074a-107">Requirements</span></span>



| <span data-ttu-id="5074a-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5074a-108">Requirement</span></span> | <span data-ttu-id="5074a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="5074a-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5074a-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5074a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5074a-111">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5074a-111">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5074a-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5074a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5074a-113">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5074a-113">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





