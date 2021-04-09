---
description: 'En savoir plus sur : InstanceParameters. CleanupMismatchedLogFiles, propriété'
title: InstanceParameters. CleanupMismatchedLogFiles, propriété
TOCTitle: 'CleanupMismatchedLogFiles property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cleanupmismatchedlogfiles(v=EXCHG.10)
ms:contentKeyID: 55103296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e80bb8877335e26cb233a09b2fa3ec3a6f12615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114442"
---
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a><span data-ttu-id="68126-103">InstanceParameters. CleanupMismatchedLogFiles, propriété</span><span class="sxs-lookup"><span data-stu-id="68126-103">InstanceParameters.CleanupMismatchedLogFiles property</span></span>

<span data-ttu-id="68126-104">Obtient ou définit une valeur indiquant si JetInit échoue lorsque le moteur de base de données est configuré pour démarrer à l’aide des fichiers du journal des transactions sur un disque d’une taille différente de celle configurée.</span><span class="sxs-lookup"><span data-stu-id="68126-104">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="68126-105">Normalement, [JetInit (JET_INSTANCE)](./api.jetinit-method.md) récupère les bases de données, mais échoue avec [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) pour indiquer que la taille du fichier journal n’est pas correctement configurée.</span><span class="sxs-lookup"><span data-stu-id="68126-105">Normally, [JetInit(JET_INSTANCE)](./api.jetinit-method.md) will successfully recover the databases but will fail with [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="68126-106">Toutefois, lorsque ce paramètre est défini sur true, le moteur de base de données supprime silencieusement tous les anciens fichiers journaux, puis démarre un nouvel ensemble de fichiers journaux de transactions à l’aide de la taille de fichier journal configurée.</span><span class="sxs-lookup"><span data-stu-id="68126-106">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="68126-107">Ce paramètre est utile lorsque l’application souhaite modifier en toute transparence la taille du fichier journal des transactions, tout en continuant à travailler de manière transparente dans les scénarios de mise à niveau et de restauration.</span><span class="sxs-lookup"><span data-stu-id="68126-107">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<span data-ttu-id="68126-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="68126-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="68126-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="68126-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="68126-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68126-110">Syntax</span></span>

``` vb
'Declaration
Public Property CleanupMismatchedLogFiles As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CleanupMismatchedLogFiles

instance.CleanupMismatchedLogFiles = value
```

``` csharp
public bool CleanupMismatchedLogFiles { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="68126-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="68126-111">Property value</span></span>

<span data-ttu-id="68126-112">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="68126-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="68126-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68126-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="68126-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="68126-114">Reference</span></span>

[<span data-ttu-id="68126-115">InstanceParameters, classe</span><span class="sxs-lookup"><span data-stu-id="68126-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="68126-116">Membres InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="68126-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="68126-117">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="68126-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
