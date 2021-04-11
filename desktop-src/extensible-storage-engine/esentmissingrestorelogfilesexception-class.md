---
description: 'En savoir plus sur : classe EsentMissingRestoreLogFilesException'
title: EsentMissingRestoreLogFilesException, classe
TOCTitle: EsentMissingRestoreLogFilesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingrestorelogfilesexception(v=EXCHG.10)
ms:contentKeyID: 55102315
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3e13e2101291dc130700531f4e4245c547cfb30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113923"
---
# <a name="esentmissingrestorelogfilesexception-class"></a><span data-ttu-id="cbbfc-103">EsentMissingRestoreLogFilesException, classe</span><span class="sxs-lookup"><span data-stu-id="cbbfc-103">EsentMissingRestoreLogFilesException class</span></span>

<span data-ttu-id="cbbfc-104">Classe de base pour JET_err. Exceptions MissingRestoreLogFiles.</span><span class="sxs-lookup"><span data-stu-id="cbbfc-104">Base class for JET_err.MissingRestoreLogFiles exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="cbbfc-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="cbbfc-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="cbbfc-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="cbbfc-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="cbbfc-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="cbbfc-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="cbbfc-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="cbbfc-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="cbbfc-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="cbbfc-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="cbbfc-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="cbbfc-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="cbbfc-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="cbbfc-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="cbbfc-112">Microsoft. ISAM. esent. Interop. EsentMissingRestoreLogFilesException</span><span class="sxs-lookup"><span data-stu-id="cbbfc-112">Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException</span></span>  

<span data-ttu-id="cbbfc-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cbbfc-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cbbfc-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cbbfc-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cbbfc-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbbfc-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingRestoreLogFilesException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingRestoreLogFilesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingRestoreLogFilesException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="cbbfc-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="cbbfc-116">Thread safety</span></span>

<span data-ttu-id="cbbfc-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="cbbfc-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="cbbfc-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="cbbfc-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbbfc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbbfc-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cbbfc-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="cbbfc-120">Reference</span></span>

[<span data-ttu-id="cbbfc-121">Membres EsentMissingRestoreLogFilesException</span><span class="sxs-lookup"><span data-stu-id="cbbfc-121">EsentMissingRestoreLogFilesException members</span></span>](./esentmissingrestorelogfilesexception-members.md)

[<span data-ttu-id="cbbfc-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cbbfc-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
