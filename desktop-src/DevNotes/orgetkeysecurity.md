---
description: Récupère une copie du descripteur de sécurité protégeant la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: ORGetKeySecurity, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533399"
---
# <a name="orgetkeysecurity-function"></a><span data-ttu-id="86d01-103">ORGetKeySecurity fonction)</span><span class="sxs-lookup"><span data-stu-id="86d01-103">ORGetKeySecurity function</span></span>

<span data-ttu-id="86d01-104">Récupère une copie du descripteur de sécurité protégeant la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="86d01-104">Retrieves a copy of the security descriptor protecting the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="86d01-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86d01-105">Syntax</span></span>


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="86d01-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86d01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86d01-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86d01-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86d01-108">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="86d01-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="86d01-109">*SecurityInformation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86d01-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86d01-110">Valeur [des \_ informations de sécurité](../secauthz/security-information.md) qui indique les informations de sécurité demandées.</span><span class="sxs-lookup"><span data-stu-id="86d01-110">A [SECURITY\_INFORMATION](../secauthz/security-information.md) value that indicates the requested security information.</span></span>

</dd> <dt>

<span data-ttu-id="86d01-111">*pSecurityDescriptor* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="86d01-111">*pSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86d01-112">Pointeur vers une mémoire tampon qui reçoit une copie du descripteur de sécurité demandé.</span><span class="sxs-lookup"><span data-stu-id="86d01-112">A pointer to a buffer that receives a copy of the requested security descriptor.</span></span> <span data-ttu-id="86d01-113">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="86d01-113">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="86d01-114">*lpcbSecurityDescriptor* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="86d01-114">*lpcbSecurityDescriptor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86d01-115">Pointeur vers une variable qui spécifie la taille, en octets, de la mémoire tampon vers laquelle pointe le paramètre *pSecurityDescriptor* .</span><span class="sxs-lookup"><span data-stu-id="86d01-115">A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the *pSecurityDescriptor* parameter.</span></span> <span data-ttu-id="86d01-116">Lorsque la fonction retourne, la variable contient le nombre d’octets écrits dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="86d01-116">When the function returns, the variable contains the number of bytes written to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86d01-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86d01-117">Return value</span></span>

<span data-ttu-id="86d01-118">Si la fonction réussit, la fonction retourne une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="86d01-118">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="86d01-119">Si la fonction échoue, elle retourne un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="86d01-119">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="86d01-120">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="86d01-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="86d01-121">Si la mémoire tampon spécifiée par le paramètre *pSecurityDescriptor* est trop petite, la fonction retourne l’erreur \_ mémoire tampon insuffisante \_ et le paramètre *lpcbSecurityDescriptor* contient le nombre d’octets requis pour le descripteur de sécurité demandé.</span><span class="sxs-lookup"><span data-stu-id="86d01-121">If the buffer specified by the *pSecurityDescriptor* parameter is too small, the function returns ERROR\_INSUFFICIENT\_BUFFER and the *lpcbSecurityDescriptor* parameter contains the number of bytes required for the requested security descriptor.</span></span>

## <a name="requirements"></a><span data-ttu-id="86d01-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86d01-122">Requirements</span></span>



| <span data-ttu-id="86d01-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86d01-123">Requirement</span></span> | <span data-ttu-id="86d01-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="86d01-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86d01-125">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="86d01-125">Redistributable</span></span><br/> | <span data-ttu-id="86d01-126">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="86d01-126">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="86d01-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="86d01-127">Header</span></span><br/>          | <dl> <span data-ttu-id="86d01-128"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="86d01-128"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="86d01-129">DLL</span><span class="sxs-lookup"><span data-stu-id="86d01-129">DLL</span></span><br/>             | <dl> <span data-ttu-id="86d01-130"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86d01-130"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86d01-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86d01-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86d01-132">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="86d01-132">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="86d01-133">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="86d01-133">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="86d01-134">**ORSetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="86d01-134">**ORSetKeySecurity**</span></span>](orsetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="86d01-135">informations de sécurité \_</span><span class="sxs-lookup"><span data-stu-id="86d01-135">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
