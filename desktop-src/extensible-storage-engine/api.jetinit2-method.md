---
description: 'En savoir plus sur : méthode API. JetInit2'
title: API. JetInit2, méthode
TOCTitle: 'JetInit2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetInit2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetinit2(v=EXCHG.10)
ms:contentKeyID: 55100762
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetInit2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetInit2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 138a9830d5a74b887e7e68f3a3833f5f7e7fb8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521351"
---
# <a name="apijetinit2-method"></a><span data-ttu-id="82618-103">API. JetInit2, méthode</span><span class="sxs-lookup"><span data-stu-id="82618-103">Api.JetInit2 method</span></span>

<span data-ttu-id="82618-104">Initialisez le moteur de base de données ESENT.</span><span class="sxs-lookup"><span data-stu-id="82618-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="82618-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82618-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82618-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82618-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82618-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82618-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetInit2 ( _
    ByRef instance As JET_INSTANCE, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetInit2(instance, _
    grbit)
```

``` csharp
public static JET_wrn JetInit2(
    ref JET_INSTANCE instance,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="82618-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82618-108">Parameters</span></span>

  - <span data-ttu-id="82618-109">instance</span><span class="sxs-lookup"><span data-stu-id="82618-109">instance</span></span>  
    <span data-ttu-id="82618-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82618-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="82618-111">Instance à initialiser.</span><span class="sxs-lookup"><span data-stu-id="82618-111">The instance to initialize.</span></span> <span data-ttu-id="82618-112">Si une instance n’a pas été allouée, une nouvelle instance est créée et le moteur fonctionne en mode d’instance unique.</span><span class="sxs-lookup"><span data-stu-id="82618-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

<!-- end list -->

  - <span data-ttu-id="82618-113">grbit</span><span class="sxs-lookup"><span data-stu-id="82618-113">grbit</span></span>  
    <span data-ttu-id="82618-114">Type : [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="82618-114">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="82618-115">Options d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="82618-115">Initialization options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="82618-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82618-116">Return value</span></span>

<span data-ttu-id="82618-117">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="82618-117">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="82618-118">Code d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="82618-118">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="82618-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82618-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82618-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="82618-120">Reference</span></span>

[<span data-ttu-id="82618-121">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="82618-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="82618-122">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="82618-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="82618-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="82618-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
