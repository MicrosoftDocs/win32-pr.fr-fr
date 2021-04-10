---
description: 'En savoir plus sur : méthode API. JetIdle'
title: API. JetIdle, méthode
TOCTitle: 'JetIdle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIdle(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.IdleGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetidle(v=EXCHG.10)
ms:contentKeyID: 55100757
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIdle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIdle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e524a23d5e8fb20b1b6db1fb7e82fbb07bf3df0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953040"
---
# <a name="apijetidle-method"></a><span data-ttu-id="d93f3-103">API. JetIdle, méthode</span><span class="sxs-lookup"><span data-stu-id="d93f3-103">Api.JetIdle method</span></span>

<span data-ttu-id="d93f3-104">Effectue des tâches de nettoyage inactives ou vérifie l’état de la Banque des versions dans ESE.</span><span class="sxs-lookup"><span data-stu-id="d93f3-104">Performs idle cleanup tasks or checks the version store status in ESE.</span></span>

<span data-ttu-id="d93f3-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d93f3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d93f3-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d93f3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d93f3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d93f3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetIdle ( _
    sesid As JET_SESID, _
    grbit As IdleGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim grbit As IdleGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetIdle(sesid, _
    grbit)
```

``` csharp
public static JET_wrn JetIdle(
    JET_SESID sesid,
    IdleGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d93f3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d93f3-108">Parameters</span></span>

  - <span data-ttu-id="d93f3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d93f3-109">sesid</span></span>  
    <span data-ttu-id="d93f3-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d93f3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d93f3-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d93f3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d93f3-112">grbit</span><span class="sxs-lookup"><span data-stu-id="d93f3-112">grbit</span></span>  
    <span data-ttu-id="d93f3-113">Type : [Microsoft. ISAM. esent. Interop. IdleGrbit](./idlegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d93f3-113">Type: [Microsoft.Isam.Esent.Interop.IdleGrbit](./idlegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d93f3-114">Combinaison d’indicateurs JetIdleGrbit.</span><span class="sxs-lookup"><span data-stu-id="d93f3-114">A combination of JetIdleGrbit flags.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d93f3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d93f3-115">Return value</span></span>

<span data-ttu-id="d93f3-116">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d93f3-116">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="d93f3-117">Code d’erreur si l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="d93f3-117">An error code if the operation fails.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d93f3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d93f3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d93f3-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d93f3-119">Reference</span></span>

[<span data-ttu-id="d93f3-120">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="d93f3-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d93f3-121">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="d93f3-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d93f3-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d93f3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
