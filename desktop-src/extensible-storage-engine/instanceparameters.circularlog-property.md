---
description: 'En savoir plus sur : InstanceParameters. CircularLog, propriété'
title: InstanceParameters. CircularLog, propriété
TOCTitle: 'CircularLog property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.circularlog(v=EXCHG.10)
ms:contentKeyID: 55103320
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CircularLog
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f9a77aa0d0f60b49269dc939787b165a3f2f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531420"
---
# <a name="instanceparameterscircularlog-property"></a><span data-ttu-id="e5782-103">InstanceParameters. CircularLog, propriété</span><span class="sxs-lookup"><span data-stu-id="e5782-103">InstanceParameters.CircularLog property</span></span>

<span data-ttu-id="e5782-104">Obtient ou définit une valeur indiquant si la journalisation circulaire est activée.</span><span class="sxs-lookup"><span data-stu-id="e5782-104">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="e5782-105">Lorsque la journalisation circulaire est désactivée, tous les fichiers journaux des transactions générés sont conservés sur le disque jusqu’à ce qu’ils ne soient plus nécessaires, car une sauvegarde complète de la base de données a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="e5782-105">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="e5782-106">Lorsque la journalisation circulaire est activée, seuls les fichiers journaux des transactions qui sont plus récents que le point de contrôle actuel sont conservés sur le disque.</span><span class="sxs-lookup"><span data-stu-id="e5782-106">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="e5782-107">L’avantage de ce mode est que les sauvegardes ne sont pas nécessaires pour supprimer les anciens fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="e5782-107">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span>

<span data-ttu-id="e5782-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e5782-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e5782-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e5782-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e5782-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5782-110">Syntax</span></span>

``` vb
'Declaration
Public Property CircularLog As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CircularLog

instance.CircularLog = value
```

``` csharp
public bool CircularLog { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e5782-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e5782-111">Property value</span></span>

<span data-ttu-id="e5782-112">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e5782-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e5782-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5782-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e5782-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e5782-114">Reference</span></span>

[<span data-ttu-id="e5782-115">InstanceParameters, classe</span><span class="sxs-lookup"><span data-stu-id="e5782-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="e5782-116">Membres InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="e5782-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="e5782-117">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e5782-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
