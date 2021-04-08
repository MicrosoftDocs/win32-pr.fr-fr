---
description: 'En savoir plus sur : méthode instance. ReleaseHandle'
title: Méthode instance. ReleaseHandle
TOCTitle: 'ReleaseHandle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.releasehandle(v=EXCHG.10)
ms:contentKeyID: 55103298
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fcac0fcbffc685fb91bd0c0bf2f97865540cb1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034928"
---
# <a name="instancereleasehandle-method"></a><span data-ttu-id="000bc-103">Méthode instance. ReleaseHandle</span><span class="sxs-lookup"><span data-stu-id="000bc-103">Instance.ReleaseHandle method</span></span>

<span data-ttu-id="000bc-104">Libère le handle pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="000bc-104">Release the handle for this instance.</span></span>

<span data-ttu-id="000bc-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="000bc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="000bc-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="000bc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="000bc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="000bc-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Function ReleaseHandle As Boolean
'Usage
Dim returnValue As Boolean

returnValue = Me.ReleaseHandle()
```

``` csharp
protected override bool ReleaseHandle()
```

#### <a name="return-value"></a><span data-ttu-id="000bc-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="000bc-108">Return value</span></span>

<span data-ttu-id="000bc-109">Type : [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="000bc-109">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="000bc-110">True si le handle peut être relâché.</span><span class="sxs-lookup"><span data-stu-id="000bc-110">True if the handle could be released.</span></span>  

## <a name="see-also"></a><span data-ttu-id="000bc-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="000bc-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="000bc-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="000bc-112">Reference</span></span>

[<span data-ttu-id="000bc-113">Classe d’instance</span><span class="sxs-lookup"><span data-stu-id="000bc-113">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="000bc-114">Membres d’instance</span><span class="sxs-lookup"><span data-stu-id="000bc-114">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="000bc-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="000bc-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
