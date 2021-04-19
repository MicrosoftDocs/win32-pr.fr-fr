---
description: Obtient une référence à un objet pilote TCP v4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: ReferenceTcpDriver fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 4a9068739517cceedee72a675739b2d8b067b2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539251"
---
# <a name="referencetcpdriver-function"></a><span data-ttu-id="9a0cb-103">ReferenceTcpDriver fonction)</span><span class="sxs-lookup"><span data-stu-id="9a0cb-103">ReferenceTcpDriver function</span></span>

<span data-ttu-id="9a0cb-104">Obtient une référence à un objet pilote TCP v4.</span><span class="sxs-lookup"><span data-stu-id="9a0cb-104">Obtains a reference to a TCP v4 driver object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a0cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a0cb-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a><span data-ttu-id="9a0cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a0cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a0cb-107">*ppDriverObject* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9a0cb-107">*ppDriverObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a0cb-108">Pointeur vers une structure **d' \_ objet de pilote** .</span><span class="sxs-lookup"><span data-stu-id="9a0cb-108">A pointer to a **DRIVER\_OBJECT** structure.</span></span> <span data-ttu-id="9a0cb-109">Pour plus d’informations, consultez la documentation du kit WDK.</span><span class="sxs-lookup"><span data-stu-id="9a0cb-109">For more information, see the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a0cb-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a0cb-110">Return value</span></span>

<span data-ttu-id="9a0cb-111">Si la fonction réussit, elle retourne l' **état \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="9a0cb-111">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="9a0cb-112">En cas d’échec, il retourne le code d’état approprié.</span><span class="sxs-lookup"><span data-stu-id="9a0cb-112">If it fails, it will return the appropriate status code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a0cb-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9a0cb-113">Remarks</span></span>

<span data-ttu-id="9a0cb-114">Cette fonction ne peut être appelée qu’à partir du mode noyau.</span><span class="sxs-lookup"><span data-stu-id="9a0cb-114">This function can be called only from kernel mode.</span></span> <span data-ttu-id="9a0cb-115">L’appelant doit décrémenter le décompte de références en appelant la fonction **ObDereferenceObject** lorsqu’il a fini d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="9a0cb-115">The caller must decrement the reference count by calling the **ObDereferenceObject** function when it has finished with the object.</span></span>

<span data-ttu-id="9a0cb-116">Cette fonction est implémentée dans Drvref. lib, qui est disponible au téléchargement.</span><span class="sxs-lookup"><span data-stu-id="9a0cb-116">This function is implemented in Drvref.lib, which is available for download.</span></span> <span data-ttu-id="9a0cb-117">Consultez [bibliothèque d’API de référence du pilote réseau Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span><span class="sxs-lookup"><span data-stu-id="9a0cb-117">See [Windows Network Driver Reference API Library](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0cb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a0cb-118">Requirements</span></span>



| <span data-ttu-id="9a0cb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a0cb-119">Requirement</span></span> | <span data-ttu-id="9a0cb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a0cb-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0cb-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9a0cb-121">Library</span></span><br/> | <dl> <span data-ttu-id="9a0cb-122"><dt>Drvref. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a0cb-122"><dt>Drvref.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a0cb-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a0cb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0cb-124">**ReferenceTcpDriverV6**</span><span class="sxs-lookup"><span data-stu-id="9a0cb-124">**ReferenceTcpDriverV6**</span></span>](referencetcpdriverv6.md)
</dt> </dl>

 

 




