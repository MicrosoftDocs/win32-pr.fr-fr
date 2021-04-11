---
description: 'En savoir plus sur : champ VistaParam. CachedClosedTables'
title: Champ VistaParam. CachedClosedTables (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: CachedClosedTables field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55104337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff72925e34c731e57d11170753ecff13f4b96a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112034"
---
# <a name="vistaparamcachedclosedtables-field"></a><span data-ttu-id="bf1c1-103">Champ VistaParam. CachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="bf1c1-103">VistaParam.CachedClosedTables field</span></span>

<span data-ttu-id="bf1c1-104">Ce paramètre contrôle le nombre de ressources de l’arborescence B + mises en cache par l’instance une fois que les tables qu’elles représentent ont été fermées par l’application.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-104">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="bf1c1-105">Des valeurs élevées pour ce paramètre forcent le moteur de base de données à utiliser plus de mémoire, mais augmentent la vitesse avec laquelle un grand nombre de tables peut être ouvert de façon aléatoire par l’application.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="bf1c1-106">Cela est utile pour les applications qui ont un schéma avec un très grand nombre de tables.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-106">This is useful for applications that have a schema with a very large number of tables.</span></span>

<span data-ttu-id="bf1c1-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bf1c1-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="bf1c1-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bf1c1-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1c1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf1c1-109">Syntax</span></span>

``` vb
'Declaration
Public Const CachedClosedTables As JET_param
'Usage
Dim value As JET_param

value = VistaParam.CachedClosedTables
```

``` csharp
public const JET_param CachedClosedTables
```

## <a name="see-also"></a><span data-ttu-id="bf1c1-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf1c1-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bf1c1-111">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="bf1c1-111">Reference</span></span>

[<span data-ttu-id="bf1c1-112">VistaParam, classe</span><span class="sxs-lookup"><span data-stu-id="bf1c1-112">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="bf1c1-113">Membres VistaParam</span><span class="sxs-lookup"><span data-stu-id="bf1c1-113">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="bf1c1-114">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="bf1c1-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
