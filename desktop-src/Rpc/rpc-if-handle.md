---
title: RPC_IF_HANDLE (rpcdce. h)
description: Le \_ type de données RPC if \_ handle déclare un handle d’interface.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942592"
---
# <a name="rpc_if_handle"></a><span data-ttu-id="09945-104">\_handle RPC if \_</span><span class="sxs-lookup"><span data-stu-id="09945-104">RPC\_IF\_HANDLE</span></span>

<span data-ttu-id="09945-105">Le type de données **RPC \_ if \_ handle** déclare un handle d’interface.</span><span class="sxs-lookup"><span data-stu-id="09945-105">The **RPC\_IF\_HANDLE** data type declares an interface handle.</span></span>


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="09945-106">Notes</span><span class="sxs-lookup"><span data-stu-id="09945-106">Remarks</span></span>

<span data-ttu-id="09945-107">La bibliothèque Runtime RPC utilise des descripteurs d’interface pour accéder à la structure de données de spécification d’interface.</span><span class="sxs-lookup"><span data-stu-id="09945-107">The RPC run-time library uses interface handles to access the interface-specification data structure.</span></span> <span data-ttu-id="09945-108">Le compilateur MIDL crée automatiquement une structure de données de spécification d’interface à partir de chaque fichier IDL et crée une variable globale de type RPC \_ si \_ handle pour la spécification de l’interface.</span><span class="sxs-lookup"><span data-stu-id="09945-108">The MIDL compiler automatically creates an interface-specification data structure from each IDL file and creates a global variable of type RPC\_IF\_HANDLE for the interface specification.</span></span>

<span data-ttu-id="09945-109">Le compilateur MIDL comprend un handle d’interface dans chaque fichier d’en-tête généré pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="09945-109">The MIDL compiler includes an interface handle in each header file generated for the interface.</span></span> <span data-ttu-id="09945-110">Les fonctions qui requièrent la spécification de l’interface en tant que paramètre affichent un type de données **RPC \_ si \_ handle**.</span><span class="sxs-lookup"><span data-stu-id="09945-110">Functions requiring the interface specification as a parameter show a data type of **RPC\_IF\_HANDLE**.</span></span> <span data-ttu-id="09945-111">Le nom du descripteur de l’interface est le suivant :</span><span class="sxs-lookup"><span data-stu-id="09945-111">The form of each interface handle name is as follows:</span></span>

-   <span data-ttu-id="09945-112">*If-Name* \_ ClientIfHandle (pour le client)</span><span class="sxs-lookup"><span data-stu-id="09945-112">*if-name*\_ClientIfHandle (for the client)</span></span>
-   <span data-ttu-id="09945-113">*If-Name* \_ ServerIfHandle (pour le serveur)</span><span class="sxs-lookup"><span data-stu-id="09945-113">*if-name*\_ServerIfHandle (for the server)</span></span>

<span data-ttu-id="09945-114">La partie *If-Name* spécifie l’identificateur d’interface dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="09945-114">The *if-name* part specifies the interface identifier in the IDL file.</span></span>

<span data-ttu-id="09945-115">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="09945-115">For example:</span></span>

<span data-ttu-id="09945-116">Hello \_ ClientIfHandle</span><span class="sxs-lookup"><span data-stu-id="09945-116">hello\_ClientIfHandle</span></span>

<span data-ttu-id="09945-117">Hello \_ ServerIfHandle</span><span class="sxs-lookup"><span data-stu-id="09945-117">hello\_ServerIfHandle</span></span>

> [!Note]  
> <span data-ttu-id="09945-118">La longueur maximale du nom de handle de l’interface est de 31 caractères.</span><span class="sxs-lookup"><span data-stu-id="09945-118">The maximum length of the interface handle name is 31 characters.</span></span>

 

<span data-ttu-id="09945-119">Étant donné que les \_ parties « ClientIfHandle » et « \_ ServerIfHandle » des noms nécessitent 15 caractères, l’élément *If-Name* ne peut pas comporter plus de 16 caractères.</span><span class="sxs-lookup"><span data-stu-id="09945-119">Because the "\_ClientIfHandle" and "\_ServerIfHandle" parts of the names require 15 characters, the *if-name* element can be no more than 16 characters long.</span></span>

## <a name="requirements"></a><span data-ttu-id="09945-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09945-120">Requirements</span></span>



| <span data-ttu-id="09945-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09945-121">Requirement</span></span> | <span data-ttu-id="09945-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="09945-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09945-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09945-123">Minimum supported client</span></span><br/> | <span data-ttu-id="09945-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09945-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="09945-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09945-125">Minimum supported server</span></span><br/> | <span data-ttu-id="09945-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09945-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="09945-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="09945-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="09945-128"><dt>Rpcdce. h (inclure RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09945-128"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





