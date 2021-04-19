---
description: 'En savoir plus sur : classe EsentException'
title: EsentException, classe (Microsoft. ISAM. esent)
TOCTitle: EsentException class
ms:assetid: T:Microsoft.Isam.Esent.EsentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100645
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.EsentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.EsentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 775d63c6b1d234696790b1187538a6d1ee734a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530760"
---
# <a name="esentexception-class"></a><span data-ttu-id="eeda2-103">EsentException, classe</span><span class="sxs-lookup"><span data-stu-id="eeda2-103">EsentException class</span></span>

<span data-ttu-id="eeda2-104">Classe de base pour les exceptions ESENT.</span><span class="sxs-lookup"><span data-stu-id="eeda2-104">Base class for ESENT exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="eeda2-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="eeda2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="eeda2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="eeda2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="eeda2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="eeda2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    <span data-ttu-id="eeda2-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="eeda2-108">Microsoft.Isam.Esent.EsentException</span></span>  
      [<span data-ttu-id="eeda2-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="eeda2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
      [<span data-ttu-id="eeda2-110">Microsoft. ISAM. esent. Interop. EsentInvalidColumnException</span><span class="sxs-lookup"><span data-stu-id="eeda2-110">Microsoft.Isam.Esent.Interop.EsentInvalidColumnException</span></span>](./esentinvalidcolumnexception-class.md)  

<span data-ttu-id="eeda2-111">**Espace de noms :**  [Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eeda2-111">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="eeda2-112">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eeda2-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eeda2-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eeda2-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentException _
    Inherits Exception
'Usage
Dim instance As EsentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentException : Exception
```

## <a name="thread-safety"></a><span data-ttu-id="eeda2-114">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="eeda2-114">Thread safety</span></span>

<span data-ttu-id="eeda2-115">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="eeda2-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="eeda2-116">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="eeda2-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="eeda2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eeda2-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eeda2-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="eeda2-118">Reference</span></span>

[<span data-ttu-id="eeda2-119">Membres EsentException</span><span class="sxs-lookup"><span data-stu-id="eeda2-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="eeda2-120">Espace de noms Microsoft. ISAM. esent</span><span class="sxs-lookup"><span data-stu-id="eeda2-120">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
