---
description: 'En savoir plus sur : méthode API. JetDupSession'
title: API. JetDupSession, méthode
TOCTitle: 'JetDupSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupsession(v=EXCHG.10)
ms:contentKeyID: 55100689
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9013c3c99c1d6c6067386038ec4a51f37f978650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112594"
---
# <a name="apijetdupsession-method"></a><span data-ttu-id="722d5-103">API. JetDupSession, méthode</span><span class="sxs-lookup"><span data-stu-id="722d5-103">Api.JetDupSession method</span></span>

<span data-ttu-id="722d5-104">Initialise une nouvelle session ESE dans la même instance que le sesid donné.</span><span class="sxs-lookup"><span data-stu-id="722d5-104">Initialize a new ESE session in the same instance as the given sesid.</span></span>

<span data-ttu-id="722d5-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="722d5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="722d5-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="722d5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="722d5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="722d5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupSession ( _
    sesid As JET_SESID, _
    <OutAttribute> ByRef newSesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESID
Dim newSesid As JET_SESIDApi.JetDupSession(sesid, newSesid)
```

``` csharp
public static void JetDupSession(
    JET_SESID sesid,
    out JET_SESID newSesid
)
```

#### <a name="parameters"></a><span data-ttu-id="722d5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="722d5-108">Parameters</span></span>

  - <span data-ttu-id="722d5-109">sesid</span><span class="sxs-lookup"><span data-stu-id="722d5-109">sesid</span></span>  
    <span data-ttu-id="722d5-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="722d5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="722d5-111">Session à dupliquer.</span><span class="sxs-lookup"><span data-stu-id="722d5-111">The session to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="722d5-112">newSesid</span><span class="sxs-lookup"><span data-stu-id="722d5-112">newSesid</span></span>  
    <span data-ttu-id="722d5-113">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="722d5-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="722d5-114">Retourne la nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="722d5-114">Returns the new session.</span></span>

## <a name="see-also"></a><span data-ttu-id="722d5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="722d5-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="722d5-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="722d5-116">Reference</span></span>

[<span data-ttu-id="722d5-117">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="722d5-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="722d5-118">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="722d5-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="722d5-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="722d5-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
