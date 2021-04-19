---
description: Définit les informations de paramètre spécifiées.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: 'IPStore :: SetProvParam, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: edbbb7bd2f5d889568623390d805659e1cf840f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545353"
---
# <a name="ipstoresetprovparam-method"></a><span data-ttu-id="b4cec-103">IPStore :: SetProvParam, méthode</span><span class="sxs-lookup"><span data-stu-id="b4cec-103">IPStore::SetProvParam method</span></span>

<span data-ttu-id="b4cec-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b4cec-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b4cec-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b4cec-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b4cec-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="b4cec-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b4cec-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="b4cec-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b4cec-108">Définit les informations de paramètre spécifiées.</span><span class="sxs-lookup"><span data-stu-id="b4cec-108">Sets the specified parameter information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4cec-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4cec-109">Syntax</span></span>


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b4cec-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4cec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4cec-111">*dwParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4cec-111">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4cec-112">Contient un **fichier PST \_ pp \_ flush \_ PW \_ cache** pour vider le cache des mots de passe utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4cec-112">Contains **PST\_PP\_FLUSH\_PW\_CACHE** to flush the user password cache.</span></span>

</dd> <dt>

<span data-ttu-id="b4cec-113">*cbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4cec-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4cec-114">Longueur du mot de passe dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b4cec-114">The length of the password in the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b4cec-115">*pbData*</span><span class="sxs-lookup"><span data-stu-id="b4cec-115">*pbData*</span></span> 
</dt> <dd>

<span data-ttu-id="b4cec-116">Pointeur vers une mémoire tampon qui contient le mot de passe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4cec-116">A pointer to a buffer that contains the user's password.</span></span> <span data-ttu-id="b4cec-117">La valeur doit être **null**.</span><span class="sxs-lookup"><span data-stu-id="b4cec-117">This must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4cec-118">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b4cec-118">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b4cec-119">Réservé : doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="b4cec-119">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4cec-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4cec-120">Return value</span></span>

<span data-ttu-id="b4cec-121">La valeur de retour est une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4cec-121">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="b4cec-122">La valeur **PST \_ E \_ OK** indique que la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="b4cec-122">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4cec-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4cec-123">Requirements</span></span>



| <span data-ttu-id="b4cec-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4cec-124">Requirement</span></span> | <span data-ttu-id="b4cec-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4cec-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4cec-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4cec-126">Header</span></span><br/> | <dl> <span data-ttu-id="b4cec-127"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4cec-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="b4cec-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b4cec-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="b4cec-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4cec-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4cec-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4cec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4cec-131">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="b4cec-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
