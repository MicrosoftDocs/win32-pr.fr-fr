---
description: 'En savoir plus sur : méthode API. JetEndExternalBackupInstance'
title: API. JetEndExternalBackupInstance, méthode
TOCTitle: 'JetEndExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100691
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16ec4dc235f677ba42b4ae3bae10a79b9d494576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951056"
---
# <a name="apijetendexternalbackupinstance-method"></a><span data-ttu-id="63157-103">API. JetEndExternalBackupInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="63157-103">Api.JetEndExternalBackupInstance method</span></span>

<span data-ttu-id="63157-104">Met fin à une session de sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="63157-104">Ends an external backup session.</span></span> <span data-ttu-id="63157-105">Cette API est la dernière API d’une série d’API qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).</span><span class="sxs-lookup"><span data-stu-id="63157-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="63157-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="63157-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="63157-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="63157-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="63157-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63157-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetEndExternalBackupInstance(instance)
```

``` csharp
public static void JetEndExternalBackupInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="63157-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63157-109">Parameters</span></span>

  - <span data-ttu-id="63157-110">instance</span><span class="sxs-lookup"><span data-stu-id="63157-110">instance</span></span>  
    <span data-ttu-id="63157-111">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="63157-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="63157-112">Instance pour laquelle terminer la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="63157-112">The instance to end the backup for.</span></span>

## <a name="see-also"></a><span data-ttu-id="63157-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63157-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="63157-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="63157-114">Reference</span></span>

[<span data-ttu-id="63157-115">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="63157-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="63157-116">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="63157-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="63157-117">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="63157-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
