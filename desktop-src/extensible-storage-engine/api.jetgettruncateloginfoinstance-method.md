---
description: 'En savoir plus sur : méthode API. JetGetTruncateLogInfoInstance'
title: API. JetGetTruncateLogInfoInstance, méthode
TOCTitle: 'JetGetTruncateLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettruncateloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100743
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc54d12796a724b382343c4a3514f03102df305f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210719"
---
# <a name="apijetgettruncateloginfoinstance-method"></a><span data-ttu-id="f7b1c-103">API. JetGetTruncateLogInfoInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="f7b1c-103">Api.JetGetTruncateLogInfoInstance method</span></span>

<span data-ttu-id="f7b1c-104">Utilisé lors d’une sauvegarde initiée par [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) pour interroger une instance pour connaître les noms des fichiers du journal des transactions qui peuvent être supprimés en toute sécurité une fois la sauvegarde terminée.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="f7b1c-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f7b1c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f7b1c-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f7b1c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b1c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7b1c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTruncateLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetTruncateLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetTruncateLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="f7b1c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7b1c-108">Parameters</span></span>

  - <span data-ttu-id="f7b1c-109">instance</span><span class="sxs-lookup"><span data-stu-id="f7b1c-109">instance</span></span>  
    <span data-ttu-id="f7b1c-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f7b1c-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="f7b1c-111">Instance pour laquelle obtenir les informations.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-111">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7b1c-112">files</span><span class="sxs-lookup"><span data-stu-id="f7b1c-112">files</span></span>  
    <span data-ttu-id="f7b1c-113">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f7b1c-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f7b1c-114">Retourne une liste de chaînes terminées par null qui décrivent l’ensemble des fichiers journaux de base de données qui peuvent être supprimés en toute sécurité une fois la sauvegarde terminée.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-114">Returns a list of null terminated strings describing the set of database log files that can be safely deleted after the backup completes.</span></span> <span data-ttu-id="f7b1c-115">La liste de chaînes retournée dans cette mémoire tampon est dans le même format qu’une chaîne multiple utilisée par le registre.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-115">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="f7b1c-116">Chaque chaîne se terminant par un caractère NULL est retournée dans la séquence suivie d’une marque de fin null finale.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-116">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7b1c-117">maxChars</span><span class="sxs-lookup"><span data-stu-id="f7b1c-117">maxChars</span></span>  
    <span data-ttu-id="f7b1c-118">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f7b1c-118">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f7b1c-119">Nombre maximal de caractères à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-119">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7b1c-120">actualChars</span><span class="sxs-lookup"><span data-stu-id="f7b1c-120">actualChars</span></span>  
    <span data-ttu-id="f7b1c-121">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f7b1c-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f7b1c-122">Taille réelle de la liste de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-122">Actual size of the file list.</span></span> <span data-ttu-id="f7b1c-123">Si cette valeur est supérieure à maxChars, la liste a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-123">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b1c-124">Notes</span><span class="sxs-lookup"><span data-stu-id="f7b1c-124">Remarks</span></span>

<span data-ttu-id="f7b1c-125">Il est important de noter que cette API ne retourne pas d’erreur ou d’avertissement si la mémoire tampon de sortie est trop petite pour accepter la liste complète des fichiers qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-125">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7b1c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7b1c-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f7b1c-127">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f7b1c-127">Reference</span></span>

[<span data-ttu-id="f7b1c-128">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="f7b1c-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f7b1c-129">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="f7b1c-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f7b1c-130">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f7b1c-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
