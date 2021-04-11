---
description: 'En savoir plus sur : méthode API. JetEndExternalBackupInstance2'
title: API. JetEndExternalBackupInstance2, méthode
TOCTitle: 'JetEndExternalBackupInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance2(v=EXCHG.10)
ms:contentKeyID: 55100692
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71a405c5e0ba3a398071cc317e0d42dd98c4953d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201343"
---
# <a name="apijetendexternalbackupinstance2-method"></a><span data-ttu-id="7ea09-103">API. JetEndExternalBackupInstance2, méthode</span><span class="sxs-lookup"><span data-stu-id="7ea09-103">Api.JetEndExternalBackupInstance2 method</span></span>

<span data-ttu-id="7ea09-104">Met fin à une session de sauvegarde externe.</span><span class="sxs-lookup"><span data-stu-id="7ea09-104">Ends an external backup session.</span></span> <span data-ttu-id="7ea09-105">Cette API est la dernière API d’une série d’API qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).</span><span class="sxs-lookup"><span data-stu-id="7ea09-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="7ea09-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7ea09-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7ea09-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7ea09-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7ea09-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ea09-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As EndExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As EndExternalBackupGrbitApi.JetEndExternalBackupInstance2(instance, _
    grbit)
```

``` csharp
public static void JetEndExternalBackupInstance2(
    JET_INSTANCE instance,
    EndExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7ea09-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ea09-109">Parameters</span></span>

  - <span data-ttu-id="7ea09-110">instance</span><span class="sxs-lookup"><span data-stu-id="7ea09-110">instance</span></span>  
    <span data-ttu-id="7ea09-111">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7ea09-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7ea09-112">Instance pour laquelle terminer la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="7ea09-112">The instance to end the backup for.</span></span>

<!-- end list -->

  - <span data-ttu-id="7ea09-113">grbit</span><span class="sxs-lookup"><span data-stu-id="7ea09-113">grbit</span></span>  
    <span data-ttu-id="7ea09-114">Type : [Microsoft. ISAM. esent. Interop. EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7ea09-114">Type: [Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7ea09-115">Options qui spécifient le mode de fin de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="7ea09-115">Options that specify how the backup ended.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ea09-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ea09-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7ea09-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7ea09-117">Reference</span></span>

[<span data-ttu-id="7ea09-118">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="7ea09-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7ea09-119">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="7ea09-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7ea09-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7ea09-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
