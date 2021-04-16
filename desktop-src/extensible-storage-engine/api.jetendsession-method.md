---
description: 'En savoir plus sur : méthode API. JetEndSession'
title: API. JetEndSession, méthode
TOCTitle: 'JetEndSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.EndSessionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendsession(v=EXCHG.10)
ms:contentKeyID: 55100690
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10412f6b01b14d63557bf024d65975c271bbe31b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525624"
---
# <a name="apijetendsession-method"></a><span data-ttu-id="7f33f-103">API. JetEndSession, méthode</span><span class="sxs-lookup"><span data-stu-id="7f33f-103">Api.JetEndSession method</span></span>

<span data-ttu-id="7f33f-104">Met fin à une session.</span><span class="sxs-lookup"><span data-stu-id="7f33f-104">Ends a session.</span></span>

<span data-ttu-id="7f33f-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7f33f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7f33f-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7f33f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7f33f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f33f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndSession ( _
    sesid As JET_SESID, _
    grbit As EndSessionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As EndSessionGrbitApi.JetEndSession(sesid, grbit)
```

``` csharp
public static void JetEndSession(
    JET_SESID sesid,
    EndSessionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7f33f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f33f-108">Parameters</span></span>

  - <span data-ttu-id="7f33f-109">sesid</span><span class="sxs-lookup"><span data-stu-id="7f33f-109">sesid</span></span>  
    <span data-ttu-id="7f33f-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7f33f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7f33f-111">Session à terminer.</span><span class="sxs-lookup"><span data-stu-id="7f33f-111">The session to end.</span></span>

<!-- end list -->

  - <span data-ttu-id="7f33f-112">grbit</span><span class="sxs-lookup"><span data-stu-id="7f33f-112">grbit</span></span>  
    <span data-ttu-id="7f33f-113">Type : [Microsoft. ISAM. esent. Interop. EndSessionGrbit](./endsessiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7f33f-113">Type: [Microsoft.Isam.Esent.Interop.EndSessionGrbit](./endsessiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7f33f-114">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="7f33f-114">This parameter is not used.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f33f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f33f-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7f33f-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7f33f-116">Reference</span></span>

[<span data-ttu-id="7f33f-117">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="7f33f-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7f33f-118">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="7f33f-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7f33f-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7f33f-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
