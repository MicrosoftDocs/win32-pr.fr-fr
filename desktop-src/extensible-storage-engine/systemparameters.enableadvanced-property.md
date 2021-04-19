---
description: 'En savoir plus sur : SystemParameters. EnableAdvanced, propriété'
title: Propriété SystemParameters. EnableAdvanced
TOCTitle: 'EnableAdvanced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104116
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e311685bf5ef436be11d4593523aceee73b955b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530727"
---
# <a name="systemparametersenableadvanced-property"></a><span data-ttu-id="a8dbc-103">Propriété SystemParameters. EnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="a8dbc-103">SystemParameters.EnableAdvanced property</span></span>

<span data-ttu-id="a8dbc-104">Obtient ou définit une valeur indiquant si le moteur de base de données accepte ou rejette les modifications apportées à un sous-ensemble des paramètres système.</span><span class="sxs-lookup"><span data-stu-id="a8dbc-104">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="a8dbc-105">Ce paramètre est utilisé conjointement avec la [configuration](./systemparameters.configuration-property.md) pour empêcher la définition de certains paramètres système à partir des valeurs par défaut de la configuration sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="a8dbc-105">This parameter is used in conjunction with [Configuration](./systemparameters.configuration-property.md) to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="a8dbc-106">Pris en charge sur Windows Vista et les autres.</span><span class="sxs-lookup"><span data-stu-id="a8dbc-106">Supported on Windows Vista and up.</span></span> <span data-ttu-id="a8dbc-107">Ignoré sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a8dbc-107">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="a8dbc-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a8dbc-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a8dbc-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a8dbc-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a8dbc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8dbc-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EnableAdvanced As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableAdvanced

SystemParameters.EnableAdvanced = value
```

``` csharp
public static bool EnableAdvanced { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="a8dbc-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a8dbc-111">Property value</span></span>

<span data-ttu-id="a8dbc-112">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a8dbc-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a8dbc-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8dbc-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a8dbc-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a8dbc-114">Reference</span></span>

[<span data-ttu-id="a8dbc-115">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="a8dbc-115">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="a8dbc-116">Membres SystemParameters</span><span class="sxs-lookup"><span data-stu-id="a8dbc-116">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="a8dbc-117">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a8dbc-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
