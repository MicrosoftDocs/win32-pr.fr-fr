---
description: 'En savoir plus sur : méthode API. JetCloseFileInstance'
title: API. JetCloseFileInstance, méthode
TOCTitle: 'JetCloseFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosefileinstance(v=EXCHG.10)
ms:contentKeyID: 55100663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ac29dec4032d83197a57746789afc770d84ec30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515191"
---
# <a name="apijetclosefileinstance-method"></a><span data-ttu-id="c7dd9-103">API. JetCloseFileInstance, méthode</span><span class="sxs-lookup"><span data-stu-id="c7dd9-103">Api.JetCloseFileInstance method</span></span>

<span data-ttu-id="c7dd9-104">Ferme un fichier qui a été ouvert avec JetOpenFileInstance une fois que les données de ce fichier ont été extraites à l’aide de JetReadFileInstance.</span><span class="sxs-lookup"><span data-stu-id="c7dd9-104">Closes a file that was opened with JetOpenFileInstance after the data from that file has been extracted using JetReadFileInstance.</span></span>

<span data-ttu-id="c7dd9-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c7dd9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c7dd9-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c7dd9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c7dd9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7dd9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseFileInstance ( _
    instance As JET_INSTANCE, _
    handle As JET_HANDLE _
)
'Usage
Dim instance As JET_INSTANCE
Dim handle As JET_HANDLEApi.JetCloseFileInstance(instance, _
    handle)
```

``` csharp
public static void JetCloseFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE handle
)
```

#### <a name="parameters"></a><span data-ttu-id="c7dd9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7dd9-108">Parameters</span></span>

  - <span data-ttu-id="c7dd9-109">instance</span><span class="sxs-lookup"><span data-stu-id="c7dd9-109">instance</span></span>  
    <span data-ttu-id="c7dd9-110">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c7dd9-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="c7dd9-111">Instance à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c7dd9-111">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c7dd9-112">traitée</span><span class="sxs-lookup"><span data-stu-id="c7dd9-112">handle</span></span>  
    <span data-ttu-id="c7dd9-113">Type : [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c7dd9-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="c7dd9-114">Handle à fermer.</span><span class="sxs-lookup"><span data-stu-id="c7dd9-114">The handle to close.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7dd9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7dd9-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c7dd9-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c7dd9-116">Reference</span></span>

[<span data-ttu-id="c7dd9-117">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="c7dd9-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c7dd9-118">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="c7dd9-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c7dd9-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c7dd9-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
