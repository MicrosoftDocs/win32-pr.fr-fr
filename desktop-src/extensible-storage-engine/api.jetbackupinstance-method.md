---
description: 'En savoir plus sur : méthode API. JetBackupInstance'
title: API. JetBackupInstance, méthode
TOCTitle: 'JetBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.BackupGrbit,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55107221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73c5b44f1f0b69aaed6066635ad4e82690bc3c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111942"
---
# <a name="apijetbackupinstance-method"></a><span data-ttu-id="721ad-103">API. JetBackupInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="721ad-103">Api.JetBackupInstance method</span></span>

<span data-ttu-id="721ad-104">Effectue une sauvegarde en continu d’une instance de, y compris toutes les bases de données attachées, vers un répertoire.</span><span class="sxs-lookup"><span data-stu-id="721ad-104">Performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="721ad-105">Avec plusieurs méthodes de sauvegarde prises en charge par le moteur, il s’agit de la fonction la plus simple et la plus encapsulée.</span><span class="sxs-lookup"><span data-stu-id="721ad-105">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="721ad-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="721ad-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="721ad-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="721ad-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="721ad-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="721ad-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBackupInstance ( _
    instance As JET_INSTANCE, _
    destination As String, _
    grbit As BackupGrbit, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim destination As String
Dim grbit As BackupGrbit
Dim statusCallback As JET_PFNSTATUSApi.JetBackupInstance(instance, _
    destination, grbit, statusCallback)
```

``` csharp
public static void JetBackupInstance(
    JET_INSTANCE instance,
    string destination,
    BackupGrbit grbit,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="721ad-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="721ad-109">Parameters</span></span>

  - <span data-ttu-id="721ad-110">instance</span><span class="sxs-lookup"><span data-stu-id="721ad-110">instance</span></span>  
    <span data-ttu-id="721ad-111">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="721ad-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="721ad-112">Instance à sauvegarder.</span><span class="sxs-lookup"><span data-stu-id="721ad-112">The instance to backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="721ad-113">destination</span><span class="sxs-lookup"><span data-stu-id="721ad-113">destination</span></span>  
    <span data-ttu-id="721ad-114">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="721ad-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="721ad-115">Répertoire dans lequel la sauvegarde doit être stockée.</span><span class="sxs-lookup"><span data-stu-id="721ad-115">The directory where the backup is to be stored.</span></span> <span data-ttu-id="721ad-116">Si le chemin d’accès de sauvegarde a la valeur null pour utiliser, la fonction tronque les journaux, si possible.</span><span class="sxs-lookup"><span data-stu-id="721ad-116">If the backup path is null to use the function will truncate the logs, if possible.</span></span>

<!-- end list -->

  - <span data-ttu-id="721ad-117">grbit</span><span class="sxs-lookup"><span data-stu-id="721ad-117">grbit</span></span>  
    <span data-ttu-id="721ad-118">Type : [Microsoft. ISAM. esent. Interop. BackupGrbit](./backupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="721ad-118">Type: [Microsoft.Isam.Esent.Interop.BackupGrbit](./backupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="721ad-119">Options de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="721ad-119">Backup options.</span></span>

<!-- end list -->

  - <span data-ttu-id="721ad-120">statusCallback</span><span class="sxs-lookup"><span data-stu-id="721ad-120">statusCallback</span></span>  
    <span data-ttu-id="721ad-121">Type : [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="721ad-121">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="721ad-122">Rappel de notification d’État facultatif.</span><span class="sxs-lookup"><span data-stu-id="721ad-122">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="721ad-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="721ad-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="721ad-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="721ad-124">Reference</span></span>

[<span data-ttu-id="721ad-125">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="721ad-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="721ad-126">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="721ad-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="721ad-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="721ad-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
