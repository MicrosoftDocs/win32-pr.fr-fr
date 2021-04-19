---
description: Définit la sécurité d’une clé de Registre ouverte dans une ruche de Registre hors connexion.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: ORSetKeySecurity, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545339"
---
# <a name="orsetkeysecurity-function"></a><span data-ttu-id="522f9-103">ORSetKeySecurity fonction)</span><span class="sxs-lookup"><span data-stu-id="522f9-103">ORSetKeySecurity function</span></span>

<span data-ttu-id="522f9-104">Définit la sécurité d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="522f9-104">Sets the security of an open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="522f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="522f9-105">Syntax</span></span>


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="522f9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="522f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="522f9-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="522f9-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="522f9-108">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="522f9-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="522f9-109">*SecurityInformation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="522f9-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="522f9-110">Indicateurs binaires qui indiquent le type d’informations de sécurité à définir.</span><span class="sxs-lookup"><span data-stu-id="522f9-110">Bit flags that indicate the type of security information to set.</span></span> <span data-ttu-id="522f9-111">Ce paramètre peut être une combinaison des indicateurs binaires d' [ \_ informations de sécurité](../secauthz/security-information.md) .</span><span class="sxs-lookup"><span data-stu-id="522f9-111">This parameter can be a combination of the [SECURITY\_INFORMATION](../secauthz/security-information.md) bit flags.</span></span>

</dd> <dt>

<span data-ttu-id="522f9-112">*pSecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="522f9-112">*pSecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="522f9-113">Pointeur vers une structure [de \_ descripteur de sécurité](/windows/win32/api/winnt/ns-winnt-security_descriptor) qui spécifie les attributs de sécurité à définir pour la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="522f9-113">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that specifies the security attributes to set for the specified key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="522f9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="522f9-114">Return value</span></span>

<span data-ttu-id="522f9-115">Si la fonction réussit, la fonction retourne une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="522f9-115">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="522f9-116">Si la fonction échoue, elle retourne un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="522f9-116">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="522f9-117">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="522f9-117">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="522f9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="522f9-118">Requirements</span></span>



| <span data-ttu-id="522f9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="522f9-119">Requirement</span></span> | <span data-ttu-id="522f9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="522f9-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="522f9-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="522f9-121">Redistributable</span></span><br/> | <span data-ttu-id="522f9-122">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="522f9-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="522f9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="522f9-123">Header</span></span><br/>          | <dl> <span data-ttu-id="522f9-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="522f9-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="522f9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="522f9-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="522f9-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="522f9-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="522f9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="522f9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522f9-128">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="522f9-128">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="522f9-129">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="522f9-129">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="522f9-130">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="522f9-130">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="522f9-131">**ORGetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="522f9-131">**ORGetKeySecurity**</span></span>](orgetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="522f9-132">descripteur de sécurité \_</span><span class="sxs-lookup"><span data-stu-id="522f9-132">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="522f9-133">informations de sécurité \_</span><span class="sxs-lookup"><span data-stu-id="522f9-133">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
