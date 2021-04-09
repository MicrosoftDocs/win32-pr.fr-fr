---
description: 'En savoir plus sur les éléments suivants : SystemParameters.Configpropriété figuration'
title: SystemParameters.Configpropriété figuration
TOCTitle: 'Configuration property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.configuration(v=EXCHG.10)
ms:contentKeyID: 55104117
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.set_Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.get_Configuration
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5eaa387f63df1dd91641ff38f2a6f6450629fe99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865602"
---
# <a name="systemparametersconfiguration-property"></a><span data-ttu-id="89398-103">SystemParameters.Configpropriété figuration</span><span class="sxs-lookup"><span data-stu-id="89398-103">SystemParameters.Configuration property</span></span>

<span data-ttu-id="89398-104">Obtient ou définit une valeur qui spécifie les valeurs par défaut pour l’ensemble des paramètres système.</span><span class="sxs-lookup"><span data-stu-id="89398-104">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="89398-105">Quand ce paramètre est défini sur une configuration spécifique, toutes les valeurs des paramètres système sont réinitialisées à leurs valeurs par défaut pour cette configuration.</span><span class="sxs-lookup"><span data-stu-id="89398-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="89398-106">Si la configuration est définie pour une instance spécifique, les valeurs par défaut des paramètres système globaux ne sont pas réinitialisées.</span><span class="sxs-lookup"><span data-stu-id="89398-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="89398-107">Petite configuration (0) : le moteur de base de données est optimisé pour l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="89398-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="89398-108">Configuration héritée (1) : le moteur de base de données a ses valeurs par défaut traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="89398-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="89398-109">Pris en charge sur Windows Vista et les autres.</span><span class="sxs-lookup"><span data-stu-id="89398-109">Supported on Windows Vista and up.</span></span> <span data-ttu-id="89398-110">Ignoré sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="89398-110">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="89398-111">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89398-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89398-112">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89398-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89398-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89398-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property Configuration As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.Configuration

SystemParameters.Configuration = value
```

``` csharp
public static int Configuration { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="89398-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="89398-114">Property value</span></span>

<span data-ttu-id="89398-115">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="89398-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="89398-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89398-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89398-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="89398-117">Reference</span></span>

[<span data-ttu-id="89398-118">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="89398-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="89398-119">Membres SystemParameters</span><span class="sxs-lookup"><span data-stu-id="89398-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="89398-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="89398-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
