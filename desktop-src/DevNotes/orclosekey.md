---
description: Ferme un handle vers la clé de Registre spécifiée dans une ruche de Registre hors connexion.
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: ORCloseKey, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: df6b8d9176efc1eb1e4ffb4e0453ec665ec19b6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529976"
---
# <a name="orclosekey-function"></a><span data-ttu-id="1076a-103">ORCloseKey fonction)</span><span class="sxs-lookup"><span data-stu-id="1076a-103">ORCloseKey function</span></span>

<span data-ttu-id="1076a-104">Ferme un handle vers la clé de Registre spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="1076a-104">Closes a handle to the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="1076a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1076a-105">Syntax</span></span>


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="1076a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1076a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1076a-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1076a-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1076a-108">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="1076a-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1076a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1076a-109">Return value</span></span>

<span data-ttu-id="1076a-110">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="1076a-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="1076a-111">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="1076a-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="1076a-112">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1076a-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="1076a-113">Si la clé spécifiée est la clé racine de la ruche du Registre, la fonction échoue avec un paramètre d’erreur \_ non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="1076a-113">If the specified key is the root key of the registry hive, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="1076a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1076a-114">Remarks</span></span>

<span data-ttu-id="1076a-115">Le descripteur d’une clé spécifiée ne doit pas être utilisé après avoir été fermé, car il ne sera plus valide.</span><span class="sxs-lookup"><span data-stu-id="1076a-115">The handle for a specified key should not be used after it has been closed, because it will no longer be valid.</span></span> <span data-ttu-id="1076a-116">Les handles de clés ne doivent pas être laissés ouverts plus longtemps que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1076a-116">Key handles should not be left open any longer than necessary.</span></span>

<span data-ttu-id="1076a-117">Utilisez la fonction [**ORCloseHive**](orclosehive.md) pour fermer une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="1076a-117">Use the [**ORCloseHive**](orclosehive.md) function to close an offline registry hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="1076a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1076a-118">Requirements</span></span>



| <span data-ttu-id="1076a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1076a-119">Requirement</span></span> | <span data-ttu-id="1076a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1076a-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1076a-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1076a-121">Redistributable</span></span><br/> | <span data-ttu-id="1076a-122">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="1076a-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="1076a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1076a-123">Header</span></span><br/>          | <dl> <span data-ttu-id="1076a-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1076a-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="1076a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1076a-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="1076a-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1076a-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1076a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1076a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1076a-128">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="1076a-128">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="1076a-129">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="1076a-129">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="1076a-130">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="1076a-130">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="1076a-131">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="1076a-131">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
