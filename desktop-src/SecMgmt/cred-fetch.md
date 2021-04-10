---
description: Définit des valeurs qui déterminent la manière de récupérer les informations d’identification d’un compte de service administré de groupe (gMSA).
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: Énumération CRED_FETCH (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952506"
---
# <a name="cred_fetch-enumeration"></a><span data-ttu-id="3b0b1-103">\_Énumération d’extraction de cred</span><span class="sxs-lookup"><span data-stu-id="3b0b1-103">CRED\_FETCH enumeration</span></span>

<span data-ttu-id="3b0b1-104">Définit des valeurs qui déterminent la manière de récupérer les informations d’identification d’un compte de service administré de groupe (gMSA).</span><span class="sxs-lookup"><span data-stu-id="3b0b1-104">Defines values that determine how to fetch the credential of a Group Managed Service Account (gMSA).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b0b1-105">Syntax</span></span>


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a><span data-ttu-id="3b0b1-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3b0b1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3b0b1-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span><span class="sxs-lookup"><span data-stu-id="3b0b1-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span></span>
</dt> <dd>

<span data-ttu-id="3b0b1-108">Signifie que le système d’exploitation doit tout d’abord tenter de récupérer le mot de passe à partir du cache local.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-108">Signifies that the operating system should first attempt to retrieve the password from the local cache.</span></span> <span data-ttu-id="3b0b1-109">S’il est temps de récupérer le mot de passe, le système d’exploitation doit contacter un contrôleur de domaine pour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-109">If it is time to fetch the password, then the operating system should contact a domain controller for the password.</span></span> <span data-ttu-id="3b0b1-110">En cas d’échec, retourne tous les mots de passe mis en cache avec la valeur d’État Success.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-110">If that fails, then return any cached passwords with the status value of success.</span></span>

</dd> <dt>

<span data-ttu-id="3b0b1-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span><span class="sxs-lookup"><span data-stu-id="3b0b1-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span></span>
</dt> <dd>

<span data-ttu-id="3b0b1-112">Retourne les informations d’identification DPAPI locales à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-112">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="3b0b1-113">Les fournisseurs SSP ( [*Security Support Provider*](/windows/desktop/SecGloss/s-gly) ) ne nécessitent généralement pas l’utilisation de cette énumération.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-113">[*Security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs) generally would not require the use of this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="3b0b1-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span><span class="sxs-lookup"><span data-stu-id="3b0b1-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span></span>
</dt> <dd>

<span data-ttu-id="3b0b1-115">Force le système d’exploitation à tenter de lire le mot de passe à partir du contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-115">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="3b0b1-116">Pendant l’heure de substitution du mot de passe, le mot de passe peut avoir changé au niveau du contrôleur de domaine et d’autres hôtes membres, mais l’hôte du membre gMSA reconnaît le mot de passe comme étant toujours valide.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-116">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="3b0b1-117">Cela peut se produire en raison de problèmes d’inclinaison de l’horloge entre les différents contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-117">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="3b0b1-118">Lorsque cette valeur est spécifiée, le système d’exploitation détermine s’il peut y avoir une possibilité de modification de mot de passe en raison de l’inclinaison de l’horloge et, le cas échéant, récupère le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-118">When this value is specified, the operating system determines if there could be a possible password change due to clock skew, and if so, retrieves the password.</span></span> <span data-ttu-id="3b0b1-119">Dans le cas contraire, les informations d’identification mises en cache sont retournées.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-119">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="3b0b1-120">S’il n’y a pas d’informations d’identification mises en cache, le système d’exploitation tente d’en récupérer un à partir du contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="3b0b1-120">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b0b1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b0b1-121">Requirements</span></span>



| <span data-ttu-id="3b0b1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b0b1-122">Requirement</span></span> | <span data-ttu-id="3b0b1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b0b1-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3b0b1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b0b1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3b0b1-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b0b1-125">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3b0b1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b0b1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3b0b1-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b0b1-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b0b1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b0b1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b0b1-129"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b0b1-129"><dt>Secpkg.h</dt></span></span> </dl> |



 

