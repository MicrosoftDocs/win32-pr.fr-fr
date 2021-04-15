---
description: 'En savoir plus sur : classe EsentRecoveredWithoutUndoException'
title: EsentRecoveredWithoutUndoException, classe
TOCTitle: EsentRecoveredWithoutUndoException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecoveredwithoutundoexception(v=EXCHG.10)
ms:contentKeyID: 55102607
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c644705fb514f96bb565ba84b1106bdc1dc37305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529464"
---
# <a name="esentrecoveredwithoutundoexception-class"></a><span data-ttu-id="f59f2-103">EsentRecoveredWithoutUndoException, classe</span><span class="sxs-lookup"><span data-stu-id="f59f2-103">EsentRecoveredWithoutUndoException class</span></span>

<span data-ttu-id="f59f2-104">Classe de base pour JET_err. Exceptions RecoveredWithoutUndo.</span><span class="sxs-lookup"><span data-stu-id="f59f2-104">Base class for JET_err.RecoveredWithoutUndo exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f59f2-105">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="f59f2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f59f2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f59f2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f59f2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f59f2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f59f2-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f59f2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f59f2-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f59f2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f59f2-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="f59f2-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f59f2-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="f59f2-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="f59f2-112">Microsoft. ISAM. esent. Interop. EsentRecoveredWithoutUndoException</span><span class="sxs-lookup"><span data-stu-id="f59f2-112">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoException</span></span>  

<span data-ttu-id="f59f2-113">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f59f2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f59f2-114">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f59f2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f59f2-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f59f2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecoveredWithoutUndoException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecoveredWithoutUndoException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecoveredWithoutUndoException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="f59f2-116">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="f59f2-116">Thread safety</span></span>

<span data-ttu-id="f59f2-117">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f59f2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f59f2-118">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f59f2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f59f2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f59f2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f59f2-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f59f2-120">Reference</span></span>

[<span data-ttu-id="f59f2-121">Membres EsentRecoveredWithoutUndoException</span><span class="sxs-lookup"><span data-stu-id="f59f2-121">EsentRecoveredWithoutUndoException members</span></span>](./esentrecoveredwithoutundoexception-members.md)

[<span data-ttu-id="f59f2-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f59f2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
