---
description: 'En savoir plus sur : VistaParam.Configchamp figuration'
title: VistaParam.Configchamp figuration (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: Configuration field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.configuration(v=EXCHG.10)
ms:contentKeyID: 55104229
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b330afb7158c616ba7bb9683a7bbe226d8d63542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749693"
---
# <a name="vistaparamconfiguration-field"></a><span data-ttu-id="264f3-103">VistaParam.Configchamp figuration</span><span class="sxs-lookup"><span data-stu-id="264f3-103">VistaParam.Configuration field</span></span>

<span data-ttu-id="264f3-104">Ce paramètre expose plusieurs jeux de valeurs par défaut pour l’ensemble des paramètres système.</span><span class="sxs-lookup"><span data-stu-id="264f3-104">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="264f3-105">Quand ce paramètre est défini sur une configuration spécifique, toutes les valeurs des paramètres système sont réinitialisées à leurs valeurs par défaut pour cette configuration.</span><span class="sxs-lookup"><span data-stu-id="264f3-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="264f3-106">Si la configuration est définie pour une instance spécifique, les valeurs par défaut des paramètres système globaux ne sont pas réinitialisées.</span><span class="sxs-lookup"><span data-stu-id="264f3-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="264f3-107">Petite configuration (0) : le moteur de base de données est optimisé pour l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="264f3-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="264f3-108">Configuration héritée (1) : le moteur de base de données a ses valeurs par défaut traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="264f3-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="264f3-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="264f3-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="264f3-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="264f3-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="264f3-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="264f3-111">Syntax</span></span>

``` vb
'Declaration
Public Const Configuration As JET_param
'Usage
Dim value As JET_param

value = VistaParam.Configuration
```

``` csharp
public const JET_param Configuration
```

## <a name="see-also"></a><span data-ttu-id="264f3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="264f3-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="264f3-113">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="264f3-113">Reference</span></span>

[<span data-ttu-id="264f3-114">VistaParam, classe</span><span class="sxs-lookup"><span data-stu-id="264f3-114">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="264f3-115">Membres VistaParam</span><span class="sxs-lookup"><span data-stu-id="264f3-115">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="264f3-116">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="264f3-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
