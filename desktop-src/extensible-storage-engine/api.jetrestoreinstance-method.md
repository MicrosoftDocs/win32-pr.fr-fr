---
description: 'En savoir plus sur : méthode API. JetRestoreInstance'
title: API. JetRestoreInstance, méthode
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514996"
---
# <a name="apijetrestoreinstance-method"></a><span data-ttu-id="0dabe-103">API. JetRestoreInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="0dabe-103">Api.JetRestoreInstance method</span></span>

<span data-ttu-id="0dabe-104">Restaure et récupère une sauvegarde en continu d’une instance, y compris toutes les bases de données attachées.</span><span class="sxs-lookup"><span data-stu-id="0dabe-104">Restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="0dabe-105">Il est conçu pour fonctionner avec une sauvegarde créée avec la fonction [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) .</span><span class="sxs-lookup"><span data-stu-id="0dabe-105">It is designed to work with a backup created with the [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) function.</span></span> <span data-ttu-id="0dabe-106">Il s’agit de la fonction de restauration la plus simple et la plus encapsulée.</span><span class="sxs-lookup"><span data-stu-id="0dabe-106">This is the simplest and most encapsulated restore function.</span></span>

<span data-ttu-id="0dabe-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0dabe-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0dabe-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0dabe-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0dabe-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0dabe-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="0dabe-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0dabe-110">Parameters</span></span>

  - <span data-ttu-id="0dabe-111">instance</span><span class="sxs-lookup"><span data-stu-id="0dabe-111">instance</span></span>  
    <span data-ttu-id="0dabe-112">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0dabe-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="0dabe-113">Instance à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0dabe-113">The instance to use.</span></span> <span data-ttu-id="0dabe-114">L’instance ne doit pas être initialisée.</span><span class="sxs-lookup"><span data-stu-id="0dabe-114">The instance should not be initialized.</span></span> <span data-ttu-id="0dabe-115">La restauration des fichiers va initialiser l’instance.</span><span class="sxs-lookup"><span data-stu-id="0dabe-115">Restoring the files will initialize the instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="0dabe-116">source</span><span class="sxs-lookup"><span data-stu-id="0dabe-116">source</span></span>  
    <span data-ttu-id="0dabe-117">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0dabe-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0dabe-118">Emplacement de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="0dabe-118">Location of the backup.</span></span> <span data-ttu-id="0dabe-119">La sauvegarde doit avoir été créée avec [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="0dabe-119">The backup should have been created with [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<!-- end list -->

  - <span data-ttu-id="0dabe-120">destination</span><span class="sxs-lookup"><span data-stu-id="0dabe-120">destination</span></span>  
    <span data-ttu-id="0dabe-121">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0dabe-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0dabe-122">Nom du dossier dans lequel les fichiers de base de données du jeu de sauvegarde seront copiés et récupérés.</span><span class="sxs-lookup"><span data-stu-id="0dabe-122">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="0dabe-123">Si la valeur est null, les fichiers de base de données sont copiés et récupérés à leur emplacement d’origine.</span><span class="sxs-lookup"><span data-stu-id="0dabe-123">If this is set to null, the database files will be copied and recovered to their original location.</span></span>

<!-- end list -->

  - <span data-ttu-id="0dabe-124">statusCallback</span><span class="sxs-lookup"><span data-stu-id="0dabe-124">statusCallback</span></span>  
    <span data-ttu-id="0dabe-125">Type : [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="0dabe-125">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="0dabe-126">Rappel de notification d’État facultatif.</span><span class="sxs-lookup"><span data-stu-id="0dabe-126">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="0dabe-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dabe-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0dabe-128">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="0dabe-128">Reference</span></span>

[<span data-ttu-id="0dabe-129">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="0dabe-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0dabe-130">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="0dabe-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0dabe-131">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0dabe-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
