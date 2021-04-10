---
description: 'En savoir plus sur : méthode API. JetTruncateLogInstance'
title: API. JetTruncateLogInstance, méthode
TOCTitle: 'JetTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jettruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55100815
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc1693b3f84cd594bfeca81a8e854e49e28d955f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953036"
---
# <a name="apijettruncateloginstance-method"></a><span data-ttu-id="ee5e1-103">API. JetTruncateLogInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="ee5e1-103">Api.JetTruncateLogInstance method</span></span>

<span data-ttu-id="ee5e1-104">Utilisé lors d’une sauvegarde initiée par JetBeginExternalBackup pour supprimer tous les fichiers journaux des transactions qui ne seront plus nécessaires une fois la sauvegarde actuelle terminée.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-104">Used during a backup initiated by JetBeginExternalBackup to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="ee5e1-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ee5e1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ee5e1-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ee5e1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ee5e1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee5e1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTruncateLogInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetTruncateLogInstance(instance)
```

``` csharp
public static void JetTruncateLogInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="ee5e1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee5e1-108">Parameters</span></span>

  - <span data-ttu-id="ee5e1-109">instance</span><span class="sxs-lookup"><span data-stu-id="ee5e1-109">instance</span></span>  
    <span data-ttu-id="ee5e1-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ee5e1-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="ee5e1-111">Instance à tronquer.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-111">The instance to truncate.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee5e1-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee5e1-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ee5e1-113">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ee5e1-113">Reference</span></span>

[<span data-ttu-id="ee5e1-114">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="ee5e1-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ee5e1-115">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="ee5e1-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ee5e1-116">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ee5e1-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
