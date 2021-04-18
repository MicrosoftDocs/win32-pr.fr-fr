---
description: Crée une ruche de Registre hors connexion qui contient une clé racine vide unique.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: ORCreateHive, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540644"
---
# <a name="orcreatehive-function"></a><span data-ttu-id="891d2-103">ORCreateHive fonction)</span><span class="sxs-lookup"><span data-stu-id="891d2-103">ORCreateHive function</span></span>

<span data-ttu-id="891d2-104">Crée une ruche de Registre hors connexion qui contient une clé racine vide unique.</span><span class="sxs-lookup"><span data-stu-id="891d2-104">Creates an offline registry hive that contains a single empty root key.</span></span>

## <a name="syntax"></a><span data-ttu-id="891d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="891d2-105">Syntax</span></span>


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="891d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="891d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="891d2-107">*phkResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="891d2-107">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="891d2-108">Pointe vers une variable pour recevoir un descripteur de la clé racine de la ruche de Registre hors connexion nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="891d2-108">Points to a variable to receive a handle to the root key of the newly created offline registry hive.</span></span> <span data-ttu-id="891d2-109">Si la ruche ne peut pas être créée, la fonction affecte la **valeur null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="891d2-109">If the hive cannot be created, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="891d2-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="891d2-110">Return value</span></span>

<span data-ttu-id="891d2-111">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="891d2-111">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="891d2-112">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="891d2-112">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="891d2-113">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="891d2-113">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="891d2-114">Si la mémoire est insuffisante pour créer la ruche du Registre, la fonction retourne une erreur de \_ \_ mémoire insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="891d2-114">If there is insufficient memory to create the registry hive, the function returns ERROR\_NOT\_ENOUGH\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="891d2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="891d2-115">Remarks</span></span>

<span data-ttu-id="891d2-116">La fonction **ORCreateHive** crée une ruche de Registre hors connexion vide en mémoire.</span><span class="sxs-lookup"><span data-stu-id="891d2-116">The **ORCreateHive** function creates an empty offline registry hive in memory.</span></span> <span data-ttu-id="891d2-117">Utilisez les fonctions [**ORCreateKey**](orcreatekey.md) et [**ORSetValue**](orsetvalue.md) pour ajouter des clés et définir leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="891d2-117">Use the [**ORCreateKey**](orcreatekey.md) and [**ORSetValue**](orsetvalue.md) functions to add keys and set their values.</span></span>

## <a name="requirements"></a><span data-ttu-id="891d2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="891d2-118">Requirements</span></span>



| <span data-ttu-id="891d2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="891d2-119">Requirement</span></span> | <span data-ttu-id="891d2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="891d2-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="891d2-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="891d2-121">Redistributable</span></span><br/> | <span data-ttu-id="891d2-122">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="891d2-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="891d2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="891d2-123">Header</span></span><br/>          | <dl> <span data-ttu-id="891d2-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="891d2-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="891d2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="891d2-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="891d2-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="891d2-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="891d2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="891d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891d2-128">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="891d2-128">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="891d2-129">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="891d2-129">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="891d2-130">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="891d2-130">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="891d2-131">**ORSetValue**</span><span class="sxs-lookup"><span data-stu-id="891d2-131">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
