---
description: 'En savoir plus sur : méthode API. JetOpenFileInstance'
title: API. JetOpenFileInstance, méthode
TOCTitle: 'JetOpenFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.JET_HANDLE@,System.Int64@,System.Int64@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopenfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100767
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b58b3a426fd2eb7e33cce1f5f539418bcc993ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522423"
---
# <a name="apijetopenfileinstance-method"></a><span data-ttu-id="1a782-103">API. JetOpenFileInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="1a782-103">Api.JetOpenFileInstance method</span></span>

<span data-ttu-id="1a782-104">Ouvre une base de données attachée, un fichier de correctif de base de données ou un fichier journal de transactions d’une instance active pour effectuer une sauvegarde de diffusion en continu floue.</span><span class="sxs-lookup"><span data-stu-id="1a782-104">Opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="1a782-105">Les données de ces fichiers peuvent ensuite être lues par le handle retourné à l’aide de JetReadFileInstance.</span><span class="sxs-lookup"><span data-stu-id="1a782-105">The data from these files can subsequently be read through the returned handle using JetReadFileInstance.</span></span> <span data-ttu-id="1a782-106">Le handle retourné doit être fermé à l’aide de JetCloseFileInstance.</span><span class="sxs-lookup"><span data-stu-id="1a782-106">The returned handle must be closed using JetCloseFileInstance.</span></span> <span data-ttu-id="1a782-107">Une sauvegarde externe de l’instance doit avoir été précédemment lancée à l’aide de JetBeginExternalBackupInstance.</span><span class="sxs-lookup"><span data-stu-id="1a782-107">An external backup of the instance must have been previously initiated using JetBeginExternalBackupInstance.</span></span>

<span data-ttu-id="1a782-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1a782-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1a782-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1a782-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1a782-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a782-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenFileInstance ( _
    instance As JET_INSTANCE, _
    file As String, _
    <OutAttribute> ByRef handle As JET_HANDLE, _
    <OutAttribute> ByRef fileSizeLow As Long, _
    <OutAttribute> ByRef fileSizeHigh As Long _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As String
Dim handle As JET_HANDLE
Dim fileSizeLow As Long
Dim fileSizeHigh As LongApi.JetOpenFileInstance(instance, _
    file, handle, fileSizeLow, fileSizeHigh)
```

``` csharp
public static void JetOpenFileInstance(
    JET_INSTANCE instance,
    string file,
    out JET_HANDLE handle,
    out long fileSizeLow,
    out long fileSizeHigh
)
```

#### <a name="parameters"></a><span data-ttu-id="1a782-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a782-111">Parameters</span></span>

  - <span data-ttu-id="1a782-112">instance</span><span class="sxs-lookup"><span data-stu-id="1a782-112">instance</span></span>  
    <span data-ttu-id="1a782-113">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a782-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="1a782-114">Instance à utiliser.</span><span class="sxs-lookup"><span data-stu-id="1a782-114">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a782-115">fichier</span><span class="sxs-lookup"><span data-stu-id="1a782-115">file</span></span>  
    <span data-ttu-id="1a782-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1a782-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1a782-117">Fichier à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="1a782-117">The file to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a782-118">traitée</span><span class="sxs-lookup"><span data-stu-id="1a782-118">handle</span></span>  
    <span data-ttu-id="1a782-119">Type : [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a782-119">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="1a782-120">Retourne un handle au fichier.</span><span class="sxs-lookup"><span data-stu-id="1a782-120">Returns a handle to the file.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a782-121">fileSizeLow</span><span class="sxs-lookup"><span data-stu-id="1a782-121">fileSizeLow</span></span>  
    <span data-ttu-id="1a782-122">Type : [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="1a782-122">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="1a782-123">Retourne les 32 bits les moins significatifs de la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="1a782-123">Returns the least significant 32 bits of the file size.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a782-124">fileSizeHigh</span><span class="sxs-lookup"><span data-stu-id="1a782-124">fileSizeHigh</span></span>  
    <span data-ttu-id="1a782-125">Type : [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="1a782-125">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="1a782-126">Retourne les 32 bits les plus significatifs de la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="1a782-126">Returns the most significant 32 bits of the file size.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a782-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a782-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1a782-128">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1a782-128">Reference</span></span>

[<span data-ttu-id="1a782-129">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="1a782-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1a782-130">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="1a782-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1a782-131">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1a782-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
