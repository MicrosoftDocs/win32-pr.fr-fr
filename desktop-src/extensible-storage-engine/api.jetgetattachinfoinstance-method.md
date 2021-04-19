---
description: 'En savoir plus sur : méthode API. JetGetAttachInfoInstance'
title: API. JetGetAttachInfoInstance, méthode
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94865042edf8b049b7140673a8aee1b4e2d91573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515216"
---
# <a name="apijetgetattachinfoinstance-method"></a><span data-ttu-id="2fecb-103">API. JetGetAttachInfoInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="2fecb-103">Api.JetGetAttachInfoInstance method</span></span>

<span data-ttu-id="2fecb-104">Utilisé lors d’une sauvegarde initiée par [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) pour interroger une instance pour obtenir les noms des fichiers de base de données qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="2fecb-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="2fecb-105">Seules les bases de données qui sont actuellement attachées à l’instance à l’aide de [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) sont prises en compte.</span><span class="sxs-lookup"><span data-stu-id="2fecb-105">Only databases that are currently attached to the instance using [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) will be considered.</span></span> <span data-ttu-id="2fecb-106">Ces fichiers peuvent ensuite être ouverts à l’aide de [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) et lus à l’aide de [JetReadFileInstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="2fecb-106">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="2fecb-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2fecb-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2fecb-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2fecb-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2fecb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fecb-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="2fecb-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fecb-110">Parameters</span></span>

  - <span data-ttu-id="2fecb-111">instance</span><span class="sxs-lookup"><span data-stu-id="2fecb-111">instance</span></span>  
    <span data-ttu-id="2fecb-112">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2fecb-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="2fecb-113">Instance pour laquelle obtenir les informations.</span><span class="sxs-lookup"><span data-stu-id="2fecb-113">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="2fecb-114">files</span><span class="sxs-lookup"><span data-stu-id="2fecb-114">files</span></span>  
    <span data-ttu-id="2fecb-115">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2fecb-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2fecb-116">Retourne une liste de chaînes terminées par le caractère null qui décrivent l’ensemble des fichiers de base de données qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="2fecb-116">Returns a list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="2fecb-117">La liste de chaînes retournée dans cette mémoire tampon est dans le même format qu’une chaîne multiple utilisée par le registre.</span><span class="sxs-lookup"><span data-stu-id="2fecb-117">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="2fecb-118">Chaque chaîne se terminant par un caractère NULL est retournée dans la séquence suivie d’une marque de fin null finale.</span><span class="sxs-lookup"><span data-stu-id="2fecb-118">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="2fecb-119">maxChars</span><span class="sxs-lookup"><span data-stu-id="2fecb-119">maxChars</span></span>  
    <span data-ttu-id="2fecb-120">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2fecb-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2fecb-121">Nombre maximal de caractères à récupérer.</span><span class="sxs-lookup"><span data-stu-id="2fecb-121">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="2fecb-122">actualChars</span><span class="sxs-lookup"><span data-stu-id="2fecb-122">actualChars</span></span>  
    <span data-ttu-id="2fecb-123">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2fecb-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2fecb-124">Taille réelle de la liste de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2fecb-124">Actual size of the file list.</span></span> <span data-ttu-id="2fecb-125">Si cette valeur est supérieure à maxChars, la liste a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="2fecb-125">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fecb-126">Notes</span><span class="sxs-lookup"><span data-stu-id="2fecb-126">Remarks</span></span>

<span data-ttu-id="2fecb-127">Il est important de noter que cette API ne retourne pas d’erreur ou d’avertissement si la mémoire tampon de sortie est trop petite pour accepter la liste complète des fichiers qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="2fecb-127">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="2fecb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fecb-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2fecb-129">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2fecb-129">Reference</span></span>

[<span data-ttu-id="2fecb-130">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="2fecb-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2fecb-131">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="2fecb-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2fecb-132">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2fecb-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
