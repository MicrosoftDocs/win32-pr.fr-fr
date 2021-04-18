---
description: 'En savoir plus sur : méthode API. JetCreateInstance2'
title: API. JetCreateInstance2, méthode
TOCTitle: 'JetCreateInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String,System.String,Microsoft.Isam.Esent.Interop.CreateInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance2(v=EXCHG.10)
ms:contentKeyID: 55100675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d21974d5c3bd5ca6dfbab2ac493d19b202ca6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519270"
---
# <a name="apijetcreateinstance2-method"></a><span data-ttu-id="8bc71-103">API. JetCreateInstance2, méthode</span><span class="sxs-lookup"><span data-stu-id="8bc71-103">Api.JetCreateInstance2 method</span></span>

<span data-ttu-id="8bc71-104">Allouez une nouvelle instance du moteur de base de données pour une utilisation dans un processus unique, avec un nom d’affichage spécifié.</span><span class="sxs-lookup"><span data-stu-id="8bc71-104">Allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="8bc71-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8bc71-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8bc71-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8bc71-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8bc71-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bc71-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance2 ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String, _
    displayName As String, _
    grbit As CreateInstanceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As String
Dim displayName As String
Dim grbit As CreateInstanceGrbitApi.JetCreateInstance2(instance, _
    name, displayName, grbit)
```

``` csharp
public static void JetCreateInstance2(
    out JET_INSTANCE instance,
    string name,
    string displayName,
    CreateInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8bc71-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bc71-108">Parameters</span></span>

  - <span data-ttu-id="8bc71-109">instance</span><span class="sxs-lookup"><span data-stu-id="8bc71-109">instance</span></span>  
    <span data-ttu-id="8bc71-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8bc71-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="8bc71-111">Retourne l’instance nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="8bc71-111">Returns the newly create instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="8bc71-112">name</span><span class="sxs-lookup"><span data-stu-id="8bc71-112">name</span></span>  
    <span data-ttu-id="8bc71-113">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8bc71-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8bc71-114">Spécifie un identificateur de chaîne unique pour l’instance à créer.</span><span class="sxs-lookup"><span data-stu-id="8bc71-114">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="8bc71-115">Cette chaîne doit être unique au sein d’un processus donné hébergeant le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="8bc71-115">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="8bc71-116">displayName</span><span class="sxs-lookup"><span data-stu-id="8bc71-116">displayName</span></span>  
    <span data-ttu-id="8bc71-117">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8bc71-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8bc71-118">Nom complet de l’instance à créer.</span><span class="sxs-lookup"><span data-stu-id="8bc71-118">A display name for the instance to be created.</span></span> <span data-ttu-id="8bc71-119">Il sera utilisé dans les entrées du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="8bc71-119">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="8bc71-120">grbit</span><span class="sxs-lookup"><span data-stu-id="8bc71-120">grbit</span></span>  
    <span data-ttu-id="8bc71-121">Type : [Microsoft. ISAM. esent. Interop. CreateInstanceGrbit](./createinstancegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8bc71-121">Type: [Microsoft.Isam.Esent.Interop.CreateInstanceGrbit](./createinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8bc71-122">Options de création.</span><span class="sxs-lookup"><span data-stu-id="8bc71-122">Creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="8bc71-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bc71-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8bc71-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8bc71-124">Reference</span></span>

[<span data-ttu-id="8bc71-125">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="8bc71-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8bc71-126">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="8bc71-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8bc71-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8bc71-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
