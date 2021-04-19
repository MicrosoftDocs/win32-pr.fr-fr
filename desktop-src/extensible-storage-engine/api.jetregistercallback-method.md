---
description: 'En savoir plus sur : méthode API. JetRegisterCallback'
title: API. JetRegisterCallback, méthode
TOCTitle: 'JetRegisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.IntPtr,Microsoft.Isam.Esent.Interop.JET_HANDLE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100784
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97ba91d776575285d71e0ad4ec8d94eeb10a743a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543744"
---
# <a name="apijetregistercallback-method"></a><span data-ttu-id="5ee30-103">API. JetRegisterCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="5ee30-103">Api.JetRegisterCallback method</span></span>

<span data-ttu-id="5ee30-104">Permet à l’application de configurer le moteur de base de données pour émettre des notifications à l’application pour des événements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5ee30-104">Allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="5ee30-105">Ces notifications sont associées à une table spécifique et restent effectives uniquement jusqu’à ce que l’instance contenant la table soit arrêtée à l’aide de [JetTerm (JET_INSTANCE)](./api.jetterm-method.md).</span><span class="sxs-lookup"><span data-stu-id="5ee30-105">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm(JET_INSTANCE)](./api.jetterm-method.md).</span></span>

<span data-ttu-id="5ee30-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5ee30-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5ee30-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5ee30-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee30-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ee30-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRegisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callback As JET_CALLBACK, _
    context As IntPtr, _
    <OutAttribute> ByRef callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callback As JET_CALLBACK
Dim context As IntPtr
Dim callbackId As JET_HANDLEApi.JetRegisterCallback(sesid, _
    tableid, cbtyp, callback, context, _
    callbackId)
```

``` csharp
public static void JetRegisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_CALLBACK callback,
    IntPtr context,
    out JET_HANDLE callbackId
)
```

#### <a name="parameters"></a><span data-ttu-id="5ee30-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ee30-109">Parameters</span></span>

  - <span data-ttu-id="5ee30-110">sesid</span><span class="sxs-lookup"><span data-stu-id="5ee30-110">sesid</span></span>  
    <span data-ttu-id="5ee30-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5ee30-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5ee30-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5ee30-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5ee30-113">TableID</span><span class="sxs-lookup"><span data-stu-id="5ee30-113">tableid</span></span>  
    <span data-ttu-id="5ee30-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5ee30-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5ee30-115">Curseur ouvert sur la table sur laquelle le rappel doit être enregistré.</span><span class="sxs-lookup"><span data-stu-id="5ee30-115">A cursor opened on the table that the callback should be registered on.</span></span>

<!-- end list -->

  - <span data-ttu-id="5ee30-116">cbtyp</span><span class="sxs-lookup"><span data-stu-id="5ee30-116">cbtyp</span></span>  
    <span data-ttu-id="5ee30-117">Type : [Microsoft.ISAM.esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5ee30-117">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="5ee30-118">Raisons de rappel pour lesquelles l’application souhaite recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="5ee30-118">The callback reasons for which the application wishes to receive notifications.</span></span>

<!-- end list -->

  - <span data-ttu-id="5ee30-119">rappel</span><span class="sxs-lookup"><span data-stu-id="5ee30-119">callback</span></span>  
    <span data-ttu-id="5ee30-120">Type : [Microsoft.ISAM.esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="5ee30-120">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="5ee30-121">Fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="5ee30-121">The callback function.</span></span>

<!-- end list -->

  - <span data-ttu-id="5ee30-122">contexte</span><span class="sxs-lookup"><span data-stu-id="5ee30-122">context</span></span>  
    <span data-ttu-id="5ee30-123">Type : [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="5ee30-123">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="5ee30-124">Contexte qui sera donné au rappel.</span><span class="sxs-lookup"><span data-stu-id="5ee30-124">A context that will be given to the callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="5ee30-125">callbackId</span><span class="sxs-lookup"><span data-stu-id="5ee30-125">callbackId</span></span>  
    <span data-ttu-id="5ee30-126">Type : [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5ee30-126">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="5ee30-127">Handle qui peut être utilisé ultérieurement pour annuler l’inscription de la fonction de rappel donnée à l’aide de [JetUnregisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md).</span><span class="sxs-lookup"><span data-stu-id="5ee30-127">A handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5ee30-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ee30-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5ee30-129">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="5ee30-129">Reference</span></span>

[<span data-ttu-id="5ee30-130">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="5ee30-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5ee30-131">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="5ee30-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5ee30-132">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5ee30-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
