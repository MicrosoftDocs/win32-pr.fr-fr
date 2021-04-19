---
description: 'En savoir plus sur : <T> interface IContentEquatable'
title: Interface IContentEquatable (T)
TOCTitle: IContentEquatable(T) interface
ms:assetid: T:Microsoft.Isam.Esent.Interop.IContentEquatable`1
ms:mtpsurl: https://msdn.microsoft.com/library/Hh578046(v=EXCHG.10)
ms:contentKeyID: 39511318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02e237714f020f5bafa3ce8b7465f1c8e2615c01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544741"
---
# <a name="icontentequatablet-interface"></a><span data-ttu-id="10372-103">\<T\>Interface IContentEquatable</span><span class="sxs-lookup"><span data-stu-id="10372-103">IContentEquatable\<T\> interface</span></span>

<span data-ttu-id="10372-104">Interface pour les objets dont le contenu peut être comparé l’un à l’autre.</span><span class="sxs-lookup"><span data-stu-id="10372-104">Interface for objects that can have their contents compared against each other.</span></span> <span data-ttu-id="10372-105">Cette valeur doit être utilisée pour les comparaisons d’égalité sur les objets de référence mutable où la substitution de Equals () et GetHashCode () n’est pas une bonne idée.</span><span class="sxs-lookup"><span data-stu-id="10372-105">This should be used for equality comparisons on mutable reference objects where overriding Equals() and GetHashCode() isn't a good idea.</span></span>

<span data-ttu-id="10372-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="10372-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="10372-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="10372-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10372-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10372-108">Syntax</span></span>

``` vb
'Declaration
Public Interface IContentEquatable(Of T)
'Usage
Dim instance As IContentEquatable(Of T)
```

``` csharp
public interface IContentEquatable<T>
```

#### <a name="type-parameters"></a><span data-ttu-id="10372-109">Paramètres de type</span><span class="sxs-lookup"><span data-stu-id="10372-109">Type parameters</span></span>

  - <span data-ttu-id="10372-110">T</span><span class="sxs-lookup"><span data-stu-id="10372-110">T</span></span>  
    <span data-ttu-id="10372-111">Type des objets à comapre.</span><span class="sxs-lookup"><span data-stu-id="10372-111">The type of objects to comapre.</span></span>

## <a name="see-also"></a><span data-ttu-id="10372-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10372-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10372-113">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="10372-113">Reference</span></span>

[<span data-ttu-id="10372-114">\<T\>Membres IContentEquatable</span><span class="sxs-lookup"><span data-stu-id="10372-114">IContentEquatable\<T\> members</span></span>](./icontentequatable-t-members.md)

[<span data-ttu-id="10372-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="10372-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
