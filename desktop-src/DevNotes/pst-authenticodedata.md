---
description: Définit les données à utiliser dans la vérification Microsoft Authenticode des données d’élément.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: Structure PST_AUTHENTICODEDATA (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: ff53526febcc8eab1a95285ffa3dcb59fe628238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542585"
---
# <a name="pst_authenticodedata-structure"></a><span data-ttu-id="e5ec1-103">AUTHENTICODEDATA PST ( \_ structure)</span><span class="sxs-lookup"><span data-stu-id="e5ec1-103">PST\_AUTHENTICODEDATA structure</span></span>

<span data-ttu-id="e5ec1-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="e5ec1-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="e5ec1-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="e5ec1-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="e5ec1-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="e5ec1-108">Définit les données à utiliser dans la vérification Microsoft Authenticode des données d’élément.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-108">Defines data to be used in Microsoft Authenticode verification of item data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ec1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5ec1-109">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a><span data-ttu-id="e5ec1-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e5ec1-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e5ec1-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="e5ec1-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="e5ec1-112">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="e5ec1-113">**dwModifiers**</span><span class="sxs-lookup"><span data-stu-id="e5ec1-113">**dwModifiers**</span></span>
</dt> <dd>

<span data-ttu-id="e5ec1-114">Valeur qui identifie le modificateur que l’une des chaînes d’appelants doit vérifier.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-114">A value that identifies the modifier that one of a chain of callers must verify.</span></span>



| <span data-ttu-id="e5ec1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5ec1-115">Value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="e5ec1-116">Signification</span><span class="sxs-lookup"><span data-stu-id="e5ec1-116">Meaning</span></span>                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <span data-ttu-id="e5ec1-117"><dt>**Fichier PST \_ \_ \_ Appelant unique AC**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e5ec1-117"><dt>**PST\_AC\_SINGLE\_CALLER**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="e5ec1-118">Un seul niveau dans la chaîne d’appel à PStore.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-118">Only a single level in the call chain to PStore.</span></span> <span data-ttu-id="e5ec1-119">L’appelant passe le contrôle de vérification.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-119">The caller passes the verification check.</span></span> <span data-ttu-id="e5ec1-120">L’image spécifiée est l’appelant immédiat et est une application (. exe).</span><span class="sxs-lookup"><span data-stu-id="e5ec1-120">The specified image is the immediate caller, and is an application (.exe).</span></span><br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <span data-ttu-id="e5ec1-121"><dt>**Fichier PST \_ \_Appelant de \_ niveau \_ supérieur AC**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e5ec1-121"><dt>**PST\_AC\_TOP\_LEVEL\_CALLER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e5ec1-122">L’appelant de niveau supérieur doit réussir la vérification, mais il peut y avoir des dll intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-122">The top-level caller must pass the check, but there may be intermediate DLLs.</span></span> <span data-ttu-id="e5ec1-123">L’image spécifiée n’est pas nécessairement l’appelant immédiat et est une application (. exe).</span><span class="sxs-lookup"><span data-stu-id="e5ec1-123">The specified image is not necessarily the immediate caller, and is an application (.exe).</span></span><br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <span data-ttu-id="e5ec1-124"><dt>**Fichier PST \_ \_ \_ Appelant immédiat AC**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e5ec1-124"><dt>**PST\_AC\_IMMEDIATE\_CALLER**</dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="e5ec1-125">L’appelant immédiat doit réussir la vérification, mais ne doit pas nécessairement être le processus de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-125">The immediate caller must pass the check, but need not be the top-level process.</span></span> <span data-ttu-id="e5ec1-126">L’image spécifiée est l’appelant immédiat, et l’image peut être une application (. exe) ou une DLL.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-126">The specified image is the immediate caller, and the image can be an application (.exe) or a DLL.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e5ec1-127">**szRootCA**</span><span class="sxs-lookup"><span data-stu-id="e5ec1-127">**szRootCA**</span></span>
</dt> <dd>

<span data-ttu-id="e5ec1-128">Pointeur vers une chaîne de caractères larges qui représente l’autorité de certification racine pour le certificat ; Utilisez la **valeur null** pour utiliser une autorité de certification disponible.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-128">A pointer to a wide character string that represents the root certification authority (CA) for the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="e5ec1-129">**szIssuer**</span><span class="sxs-lookup"><span data-stu-id="e5ec1-129">**szIssuer**</span></span>
</dt> <dd>

<span data-ttu-id="e5ec1-130">Pointeur vers une chaîne de caractères larges qui représente l’autorité de certification qui a émis le certificat ; Utilisez la **valeur null** pour utiliser une autorité de certification disponible.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-130">A pointer to a wide character string that represents the CA that issued the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="e5ec1-131">**szPublisher**</span><span class="sxs-lookup"><span data-stu-id="e5ec1-131">**szPublisher**</span></span>
</dt> <dd>

<span data-ttu-id="e5ec1-132">Pointeur vers une chaîne de caractères larges qui représente l’éditeur de logiciel ; Utilisez la **valeur null** pour utiliser une autorité de certification disponible.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-132">A pointer to a wide character string that represents the software publisher; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="e5ec1-133">**szProgramName**</span><span class="sxs-lookup"><span data-stu-id="e5ec1-133">**szProgramName**</span></span>
</dt> <dd>

<span data-ttu-id="e5ec1-134">Pointeur vers une chaîne de caractères larges qui représente le nom du programme ; Utilisez la **valeur null** pour utiliser une autorité de certification disponible.</span><span class="sxs-lookup"><span data-stu-id="e5ec1-134">A pointer to a wide character string that represents the program name; use **NULL** to use any available CA.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5ec1-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5ec1-135">Requirements</span></span>



| <span data-ttu-id="e5ec1-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5ec1-136">Requirement</span></span> | <span data-ttu-id="e5ec1-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5ec1-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ec1-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5ec1-138">Header</span></span><br/> | <dl> <span data-ttu-id="e5ec1-139"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ec1-139"><dt>Pstore.h</dt></span></span> </dl> |



 

 
