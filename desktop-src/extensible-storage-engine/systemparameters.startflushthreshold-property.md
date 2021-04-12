---
description: 'En savoir plus sur : SystemParameters. StartFlushThreshold, propriété'
title: Propriété SystemParameters. StartFlushThreshold
TOCTitle: 'StartFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.startflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104050
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StartFlushThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0e520682253d7a586c36366d229be59e014c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320165"
---
# <a name="systemparametersstartflushthreshold-property"></a><span data-ttu-id="8b097-103">Propriété SystemParameters. StartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="8b097-103">SystemParameters.StartFlushThreshold property</span></span>

<span data-ttu-id="8b097-104">Obtient ou définit le seuil auquel le cache de la page de base de données commence à supprimer les pages du cache pour libérer de l’espace pour les pages qui ne sont pas mises en cache.</span><span class="sxs-lookup"><span data-stu-id="8b097-104">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="8b097-105">Lorsque le nombre de tampons de page dans le cache descend sous ce seuil, un processus en arrière-plan est démarré pour réapprovisionner ce pool de mémoires tampons disponibles.</span><span class="sxs-lookup"><span data-stu-id="8b097-105">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="8b097-106">Ce seuil est toujours relatif à la taille maximale du cache définie par JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="8b097-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="8b097-107">Ce seuil doit également toujours être inférieur au seuil d’arrêt défini par JET_paramStopFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="8b097-107">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="8b097-108">La hauteur de distance du seuil de démarrage détermine le temps de réponse que le cache de page de la base de données doit avoir pour produire des tampons disponibles avant que l’application en ait besoin.</span><span class="sxs-lookup"><span data-stu-id="8b097-108">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="8b097-109">Un seuil de démarrage élevé donnera plus de temps au processus en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8b097-109">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="8b097-110">Toutefois, un seuil de démarrage élevé implique un seuil d’arrêt plus élevé et réduit la taille effective du cache des pages de la base de données.</span><span class="sxs-lookup"><span data-stu-id="8b097-110">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="8b097-111">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8b097-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8b097-112">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8b097-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8b097-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b097-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StartFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StartFlushThreshold

SystemParameters.StartFlushThreshold = value
```

``` csharp
public static int StartFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="8b097-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8b097-114">Property value</span></span>

<span data-ttu-id="8b097-115">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8b097-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8b097-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b097-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8b097-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8b097-117">Reference</span></span>

[<span data-ttu-id="8b097-118">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="8b097-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="8b097-119">Membres SystemParameters</span><span class="sxs-lookup"><span data-stu-id="8b097-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="8b097-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8b097-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
