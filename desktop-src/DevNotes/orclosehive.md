---
description: Ferme la ruche de Registre hors connexion spécifiée et libère la mémoire allouée pour la ruche.
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: ORCloseHive, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a7f018e2ccdb98de14f908224ade52d0cdf7819f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535349"
---
# <a name="orclosehive-function"></a><span data-ttu-id="67393-103">ORCloseHive fonction)</span><span class="sxs-lookup"><span data-stu-id="67393-103">ORCloseHive function</span></span>

<span data-ttu-id="67393-104">Ferme la ruche de Registre hors connexion spécifiée et libère la mémoire allouée pour la ruche.</span><span class="sxs-lookup"><span data-stu-id="67393-104">Closes the specified offline registry hive and frees memory allocated for the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="67393-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67393-105">Syntax</span></span>


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="67393-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67393-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67393-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67393-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67393-108">Handle de la clé racine de la ruche de Registre hors connexion à fermer.</span><span class="sxs-lookup"><span data-stu-id="67393-108">A handle to the root key of the offline registry hive to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67393-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67393-109">Return value</span></span>

<span data-ttu-id="67393-110">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="67393-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="67393-111">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="67393-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="67393-112">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="67393-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="67393-113">Notes</span><span class="sxs-lookup"><span data-stu-id="67393-113">Remarks</span></span>

<span data-ttu-id="67393-114">La fonction **ORCloseHive** libère toute la mémoire allouée par les fonctions de Registre hors connexion pour le compte de la ruche spécifiée.</span><span class="sxs-lookup"><span data-stu-id="67393-114">The **ORCloseHive** function frees all memory allocated by the offline registry functions on behalf of the specified hive.</span></span>

<span data-ttu-id="67393-115">Pour conserver les modifications apportées à la ruche, appelez la fonction [**ORSaveHive**](orsavehive.md) avant d’appeler **ORCloseHive**.</span><span class="sxs-lookup"><span data-stu-id="67393-115">To preserve changes to the hive, call the [**ORSaveHive**](orsavehive.md) function before calling **ORCloseHive**.</span></span>

## <a name="requirements"></a><span data-ttu-id="67393-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67393-116">Requirements</span></span>



| <span data-ttu-id="67393-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67393-117">Requirement</span></span> | <span data-ttu-id="67393-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="67393-118">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67393-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="67393-119">Redistributable</span></span><br/> | <span data-ttu-id="67393-120">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="67393-120">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="67393-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="67393-121">Header</span></span><br/>          | <dl> <span data-ttu-id="67393-122"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="67393-122"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="67393-123">DLL</span><span class="sxs-lookup"><span data-stu-id="67393-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="67393-124"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67393-124"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67393-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67393-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67393-126">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="67393-126">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="67393-127">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="67393-127">**ORSaveHive**</span></span>](orsavehive.md)
</dt> </dl>

 

 
