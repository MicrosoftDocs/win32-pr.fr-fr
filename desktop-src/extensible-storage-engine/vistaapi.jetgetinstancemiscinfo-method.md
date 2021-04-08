---
description: 'En savoir plus sur : méthode VistaApi. JetGetInstanceMiscInfo'
title: Méthode VistaApi. JetGetInstanceMiscInfo (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'JetGetInstanceMiscInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE@,Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetinstancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 55104187
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 204beee343a717d5b45d8003e123bbbe186437d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863693"
---
# <a name="vistaapijetgetinstancemiscinfo-method"></a><span data-ttu-id="783b3-103">Méthode VistaApi. JetGetInstanceMiscInfo</span><span class="sxs-lookup"><span data-stu-id="783b3-103">VistaApi.JetGetInstanceMiscInfo method</span></span>

<span data-ttu-id="783b3-104">Récupère des informations sur une instance.</span><span class="sxs-lookup"><span data-stu-id="783b3-104">Retrieves information about an instance.</span></span>

<span data-ttu-id="783b3-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="783b3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="783b3-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="783b3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="783b3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="783b3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetInstanceMiscInfo ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef signature As JET_SIGNATURE, _
    infoLevel As JET_InstanceMiscInfo _
)
'Usage
Dim instance As JET_INSTANCE
Dim signature As JET_SIGNATURE
Dim infoLevel As JET_InstanceMiscInfoVistaApi.JetGetInstanceMiscInfo(instance, _
    signature, infoLevel)
```

``` csharp
public static void JetGetInstanceMiscInfo(
    JET_INSTANCE instance,
    out JET_SIGNATURE signature,
    JET_InstanceMiscInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="783b3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="783b3-108">Parameters</span></span>

  - <span data-ttu-id="783b3-109">instance</span><span class="sxs-lookup"><span data-stu-id="783b3-109">instance</span></span>  
    <span data-ttu-id="783b3-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="783b3-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="783b3-111">Instance de à propos de laquelle obtenir des informations.</span><span class="sxs-lookup"><span data-stu-id="783b3-111">The instance to get information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="783b3-112">signature</span><span class="sxs-lookup"><span data-stu-id="783b3-112">signature</span></span>  
    <span data-ttu-id="783b3-113">Type : [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="783b3-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="783b3-114">Informations récupérées.</span><span class="sxs-lookup"><span data-stu-id="783b3-114">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="783b3-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="783b3-115">infoLevel</span></span>  
    <span data-ttu-id="783b3-116">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="783b3-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="783b3-117">Type d’informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="783b3-117">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="783b3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="783b3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="783b3-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="783b3-119">Reference</span></span>

[<span data-ttu-id="783b3-120">VistaApi, classe</span><span class="sxs-lookup"><span data-stu-id="783b3-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="783b3-121">Membres VistaApi</span><span class="sxs-lookup"><span data-stu-id="783b3-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="783b3-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="783b3-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
