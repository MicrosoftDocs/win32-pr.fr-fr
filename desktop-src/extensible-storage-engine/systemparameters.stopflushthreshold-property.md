---
description: 'En savoir plus sur : SystemParameters. StopFlushThreshold, propriété'
title: Propriété SystemParameters. StopFlushThreshold
TOCTitle: 'StopFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.stopflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b79a9e5894de6539e8ab7dc0db4218b5f6cb3bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320162"
---
# <a name="systemparametersstopflushthreshold-property"></a><span data-ttu-id="5830a-103">Propriété SystemParameters. StopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="5830a-103">SystemParameters.StopFlushThreshold property</span></span>

<span data-ttu-id="5830a-104">Obtient ou définit le seuil auquel le cache de la page de base de données met fin à la suppression des pages du cache pour libérer de l’espace pour les pages qui ne sont pas mises en cache.</span><span class="sxs-lookup"><span data-stu-id="5830a-104">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="5830a-105">Lorsque le nombre de tampons de page dans le cache dépasse ce seuil, le processus en arrière-plan qui a démarré pour réapprovisionner ce pool de mémoires tampons disponibles est arrêté.</span><span class="sxs-lookup"><span data-stu-id="5830a-105">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="5830a-106">Ce seuil est toujours relatif à la taille maximale du cache définie par JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="5830a-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="5830a-107">Ce seuil doit également être toujours supérieur au seuil de démarrage défini par JET_paramStartFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="5830a-107">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="5830a-108">La distance entre le seuil de démarrage et le seuil d’arrêt affecte l’efficacité avec laquelle les pages de base de données sont vidées par le processus en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="5830a-108">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="5830a-109">Un plus grand fossé rendra plus probable l’Association des écritures aux pages voisines.</span><span class="sxs-lookup"><span data-stu-id="5830a-109">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="5830a-110">Toutefois, un seuil d’arrêt élevé réduit la taille effective du cache des pages de la base de données.</span><span class="sxs-lookup"><span data-stu-id="5830a-110">However, a high stop threshold will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="5830a-111">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5830a-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5830a-112">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5830a-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5830a-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5830a-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StopFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StopFlushThreshold

SystemParameters.StopFlushThreshold = value
```

``` csharp
public static int StopFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="5830a-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5830a-114">Property value</span></span>

<span data-ttu-id="5830a-115">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5830a-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5830a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5830a-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5830a-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="5830a-117">Reference</span></span>

[<span data-ttu-id="5830a-118">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="5830a-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="5830a-119">Membres SystemParameters</span><span class="sxs-lookup"><span data-stu-id="5830a-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="5830a-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5830a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
