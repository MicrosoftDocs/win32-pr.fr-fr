---
description: 'En savoir plus sur : méthode API. JetGetVersion'
title: API. JetGetVersion, méthode
TOCTitle: 'JetGetVersion method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetVersion(Microsoft.Isam.Esent.Interop.JET_SESID,System.UInt32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetversion(v=EXCHG.10)
ms:contentKeyID: 55100744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetVersion
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetVersion
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8860b21ec2b5db3841b866aa9c1c2cc7cff300aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527579"
---
# <a name="apijetgetversion-method"></a><span data-ttu-id="74774-103">API. JetGetVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="74774-103">Api.JetGetVersion method</span></span>

<span data-ttu-id="74774-104">Récupère la version du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="74774-104">Retrieves the version of the database engine.</span></span>

<span data-ttu-id="74774-105">Cette API n’est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="74774-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="74774-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="74774-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="74774-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="74774-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="74774-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74774-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetVersion ( _
    sesid As JET_SESID, _
    <OutAttribute> ByRef version As UInteger _
)
'Usage
Dim sesid As JET_SESID
Dim version As UIntegerApi.JetGetVersion(sesid, version)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetVersion(
    JET_SESID sesid,
    out uint version
)
```

#### <a name="parameters"></a><span data-ttu-id="74774-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74774-109">Parameters</span></span>

  - <span data-ttu-id="74774-110">sesid</span><span class="sxs-lookup"><span data-stu-id="74774-110">sesid</span></span>  
    <span data-ttu-id="74774-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="74774-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="74774-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="74774-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="74774-113">version</span><span class="sxs-lookup"><span data-stu-id="74774-113">version</span></span>  
    <span data-ttu-id="74774-114">Type : [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="74774-114">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="74774-115">Retourne le numéro de version du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="74774-115">Returns the version number of the database engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="74774-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74774-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="74774-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="74774-117">Reference</span></span>

[<span data-ttu-id="74774-118">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="74774-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="74774-119">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="74774-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="74774-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="74774-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
