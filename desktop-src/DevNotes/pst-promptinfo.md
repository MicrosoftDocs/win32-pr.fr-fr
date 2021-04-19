---
description: Définit le comportement d’invite du magasin protégé chaque fois qu’il affiche une interface utilisateur.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: Structure PST_PROMPTINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532630"
---
# <a name="pst_promptinfo-structure"></a><span data-ttu-id="86f11-103">PROMPTINFO PST ( \_ structure)</span><span class="sxs-lookup"><span data-stu-id="86f11-103">PST\_PROMPTINFO structure</span></span>

<span data-ttu-id="86f11-104">\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="86f11-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="86f11-105">Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="86f11-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="86f11-106">Pstore utilise une implémentation plus ancienne de la protection des données.</span><span class="sxs-lookup"><span data-stu-id="86f11-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="86f11-107">Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="86f11-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="86f11-108">Définit le comportement d’invite du magasin protégé chaque fois qu’il affiche une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="86f11-108">Defines the prompting behavior of the Protected Store whenever it displays a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="86f11-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86f11-109">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a><span data-ttu-id="86f11-110">Membres</span><span class="sxs-lookup"><span data-stu-id="86f11-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="86f11-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="86f11-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="86f11-112">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="86f11-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="86f11-113">**dwPromptFlags**</span><span class="sxs-lookup"><span data-stu-id="86f11-113">**dwPromptFlags**</span></span>
</dt> <dd>

<span data-ttu-id="86f11-114">Cet indicateur est ignoré.</span><span class="sxs-lookup"><span data-stu-id="86f11-114">This flag is ignored.</span></span>



| <span data-ttu-id="86f11-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="86f11-115">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="86f11-116">Signification</span><span class="sxs-lookup"><span data-stu-id="86f11-116">Meaning</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <span data-ttu-id="86f11-117"><dt>**Fichier PST \_ PF \_ \_ affiche toujours**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="86f11-117"><dt>**PST\_PF\_ALWAYS\_SHOW**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="86f11-118">Demande que le fournisseur affiche la boîte de dialogue d’invite à l’utilisateur, même s’il n’est pas requis pour cet accès.</span><span class="sxs-lookup"><span data-stu-id="86f11-118">Requests that the provider show the prompt dialog to the user even if it is not required for this access.</span></span> <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <span data-ttu-id="86f11-119"><dt>**Fichier PST \_ PF \_ ne jamais \_ Afficher**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="86f11-119"><dt>**PST\_PF\_NEVER\_SHOW**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="86f11-120">N’affiche pas la boîte de dialogue d’invite à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="86f11-120">Do not show the prompt dialog to the user.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="86f11-121">**hwndApp**</span><span class="sxs-lookup"><span data-stu-id="86f11-121">**hwndApp**</span></span>
</dt> <dd>

<span data-ttu-id="86f11-122">Handle de la fenêtre parente pour l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="86f11-122">The handle to the parent window for the user interface.</span></span> <span data-ttu-id="86f11-123">Le membre **hwndApp** détermine l’emplacement où l’interface utilisateur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="86f11-123">The **hwndApp** member determines where the user interface appears.</span></span> <span data-ttu-id="86f11-124">Si la **valeur null** est passée, le bureau est considéré comme la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="86f11-124">If **NULL** is passed, the desktop is considered to be the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="86f11-125">**szPrompt**</span><span class="sxs-lookup"><span data-stu-id="86f11-125">**szPrompt**</span></span>
</dt> <dd>

<span data-ttu-id="86f11-126">Chaîne d’invite.</span><span class="sxs-lookup"><span data-stu-id="86f11-126">The prompt string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86f11-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86f11-127">Requirements</span></span>



| <span data-ttu-id="86f11-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86f11-128">Requirement</span></span> | <span data-ttu-id="86f11-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="86f11-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="86f11-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="86f11-130">Header</span></span><br/> | <dl> <span data-ttu-id="86f11-131"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="86f11-131"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86f11-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86f11-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f11-133">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="86f11-133">**DeleteItem**</span></span>](ipstore-deleteitem.md)
</dt> <dt>

[<span data-ttu-id="86f11-134">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="86f11-134">**OpenItem**</span></span>](ipstore-openitem.md)
</dt> <dt>

[<span data-ttu-id="86f11-135">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="86f11-135">**ReadItem**</span></span>](ipstore-readitem.md)
</dt> <dt>

[<span data-ttu-id="86f11-136">**WriteItem**</span><span class="sxs-lookup"><span data-stu-id="86f11-136">**WriteItem**</span></span>](ipstore-writeitem.md)
</dt> </dl>

 

 
