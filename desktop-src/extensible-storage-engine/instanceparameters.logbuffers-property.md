---
description: 'En savoir plus sur : InstanceParameters. LogBuffers, propriété'
title: InstanceParameters. LogBuffers, propriété
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f58e43ea38792549d384328dc0fd6c5d31616e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534048"
---
# <a name="instanceparameterslogbuffers-property"></a><span data-ttu-id="c15f2-103">InstanceParameters. LogBuffers, propriété</span><span class="sxs-lookup"><span data-stu-id="c15f2-103">InstanceParameters.LogBuffers property</span></span>

<span data-ttu-id="c15f2-104">Obtient ou définit la quantité de mémoire utilisée pour mettre en cache les enregistrements de journal avant leur écriture dans le fichier journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="c15f2-104">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="c15f2-105">L’unité de ce paramètre correspond à la taille de secteur du volume qui contient les fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="c15f2-105">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="c15f2-106">La taille des secteurs étant presque toujours de 512 octets, il est possible de supposer en toute sécurité la taille de l’unité.</span><span class="sxs-lookup"><span data-stu-id="c15f2-106">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="c15f2-107">Ce paramètre a un impact sur les performances.</span><span class="sxs-lookup"><span data-stu-id="c15f2-107">This parameter has an impact on performance.</span></span> <span data-ttu-id="c15f2-108">Lorsque le moteur de base de données subit une charge de mise à jour importante, cette mémoire tampon peut être entièrement très rapide.</span><span class="sxs-lookup"><span data-stu-id="c15f2-108">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="c15f2-109">Une plus grande taille de cache pour le fichier journal des transactions est essentielle pour garantir une bonne performance des mises à jour dans une condition de charge élevée.</span><span class="sxs-lookup"><span data-stu-id="c15f2-109">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="c15f2-110">La valeur par défaut est trop petite pour ce cas.</span><span class="sxs-lookup"><span data-stu-id="c15f2-110">The default is known to be too small for this case.</span></span> <span data-ttu-id="c15f2-111">Ne définissez pas ce paramètre sur un nombre de mémoires tampons plus grand (en octets) que la moitié de la taille d’un fichier journal de transactions.</span><span class="sxs-lookup"><span data-stu-id="c15f2-111">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<span data-ttu-id="c15f2-112">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c15f2-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c15f2-113">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c15f2-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c15f2-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c15f2-114">Syntax</span></span>

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="c15f2-115">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c15f2-115">Property value</span></span>

<span data-ttu-id="c15f2-116">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c15f2-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c15f2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c15f2-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c15f2-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c15f2-118">Reference</span></span>

[<span data-ttu-id="c15f2-119">InstanceParameters, classe</span><span class="sxs-lookup"><span data-stu-id="c15f2-119">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="c15f2-120">Membres InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="c15f2-120">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="c15f2-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c15f2-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
