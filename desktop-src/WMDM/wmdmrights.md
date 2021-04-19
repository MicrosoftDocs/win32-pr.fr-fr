---
title: WMDMRIGHTS, structure
description: La structure WMDMRIGHTS décrit les droits d’utilisation de contenu.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Structure WMDMRIGHTS Windows Media Gestionnaire de périphériques
- Pointeur de structure PWMDMRIGHTS Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535864"
---
# <a name="wmdmrights-structure"></a><span data-ttu-id="d35c0-105">WMDMRIGHTS, structure</span><span class="sxs-lookup"><span data-stu-id="d35c0-105">WMDMRIGHTS structure</span></span>

<span data-ttu-id="d35c0-106">La structure **WMDMRIGHTS** décrit les droits d’utilisation de contenu.</span><span class="sxs-lookup"><span data-stu-id="d35c0-106">The **WMDMRIGHTS** structure describes content-use rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="d35c0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d35c0-107">Syntax</span></span>


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a><span data-ttu-id="d35c0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d35c0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d35c0-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d35c0-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d35c0-110">Taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="d35c0-110">Size of the structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d35c0-111">**dwContentType**</span><span class="sxs-lookup"><span data-stu-id="d35c0-111">**dwContentType**</span></span>
</dt> <dd>

<span data-ttu-id="d35c0-112">**Valeur DWORD** contenant le type de contenu.</span><span class="sxs-lookup"><span data-stu-id="d35c0-112">**DWORD** containing the type of content.</span></span>

</dd> <dt>

<span data-ttu-id="d35c0-113">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="d35c0-113">**fuFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d35c0-114">Champ de bits spécifiant les options de droits en cours d’utilisation pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="d35c0-114">Bit field specifying the rights options in use for the content.</span></span>



| <span data-ttu-id="d35c0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d35c0-115">Value</span></span>                        | <span data-ttu-id="d35c0-116">Description</span><span class="sxs-lookup"><span data-stu-id="d35c0-116">Description</span></span>                                  |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="d35c0-117">WMDM \_ droits \_ PLAYBACKCOUNT</span><span class="sxs-lookup"><span data-stu-id="d35c0-117">WMDM\_RIGHTS\_PLAYBACKCOUNT</span></span>  | <span data-ttu-id="d35c0-118">Nombre de fois où le fichier peut être lu.</span><span class="sxs-lookup"><span data-stu-id="d35c0-118">Number of times that the file can be played.</span></span> |
| <span data-ttu-id="d35c0-119">WMDM- \_ droits \_ EXPIRATIONDATE</span><span class="sxs-lookup"><span data-stu-id="d35c0-119">WMDM\_RIGHTS\_EXPIRATIONDATE</span></span> | <span data-ttu-id="d35c0-120">Date d’expiration du fichier.</span><span class="sxs-lookup"><span data-stu-id="d35c0-120">Expiration date of the file.</span></span>                 |
| <span data-ttu-id="d35c0-121">WMDM \_ droits \_ FREESERIALIDS</span><span class="sxs-lookup"><span data-stu-id="d35c0-121">WMDM\_RIGHTS\_FREESERIALIDS</span></span>  | <span data-ttu-id="d35c0-122">Identificateur de série gratuit du fichier.</span><span class="sxs-lookup"><span data-stu-id="d35c0-122">Free serial identifier of the file.</span></span>          |
| <span data-ttu-id="d35c0-123">WMDM \_ \_ groupe GROUPID de droits</span><span class="sxs-lookup"><span data-stu-id="d35c0-123">WMDM\_RIGHTS\_GROUPID Group</span></span>  | <span data-ttu-id="d35c0-124">Identificateur du fichier.</span><span class="sxs-lookup"><span data-stu-id="d35c0-124">Identifier of the file.</span></span>                      |
| <span data-ttu-id="d35c0-125">WMDM \_ droits \_ NAMEDSERIALIDS</span><span class="sxs-lookup"><span data-stu-id="d35c0-125">WMDM\_RIGHTS\_NAMEDSERIALIDS</span></span> | <span data-ttu-id="d35c0-126">Identificateur de série nommé du fichier.</span><span class="sxs-lookup"><span data-stu-id="d35c0-126">Named serial identifier of the file.</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d35c0-127">**fuRights**</span><span class="sxs-lookup"><span data-stu-id="d35c0-127">**fuRights**</span></span>
</dt> <dd>

<span data-ttu-id="d35c0-128">Champ de bits contenant les bits de droits pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="d35c0-128">Bit field containing the rights bits for the content.</span></span>



| <span data-ttu-id="d35c0-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="d35c0-129">Value</span></span>                                     | <span data-ttu-id="d35c0-130">Description</span><span class="sxs-lookup"><span data-stu-id="d35c0-130">Description</span></span>                                   |
|-------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="d35c0-131">WMDM \_ les \_ droits \_ de lecture sur le \_ PC</span><span class="sxs-lookup"><span data-stu-id="d35c0-131">WMDM\_RIGHTS\_PLAY\_ON\_PC</span></span>                | <span data-ttu-id="d35c0-132">Le contenu peut être lu sur un ordinateur personnel.</span><span class="sxs-lookup"><span data-stu-id="d35c0-132">Content can be played on a personal computer.</span></span> |
| <span data-ttu-id="d35c0-133">WMDM \_ copier les droits \_ \_ sur un \_ \_ appareil non SDMI \_</span><span class="sxs-lookup"><span data-stu-id="d35c0-133">WMDM\_RIGHTS\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="d35c0-134">Le contenu peut être copié sur un appareil non-SDMI.</span><span class="sxs-lookup"><span data-stu-id="d35c0-134">Content can be copied to a non-SDMI device.</span></span>   |
| <span data-ttu-id="d35c0-135">\_copier les droits WMDM \_ \_ sur \_ CD</span><span class="sxs-lookup"><span data-stu-id="d35c0-135">WMDM\_RIGHTS\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="d35c0-136">Le contenu peut être copié sur un CD.</span><span class="sxs-lookup"><span data-stu-id="d35c0-136">Content can be copied to a CD.</span></span>                |
| <span data-ttu-id="d35c0-137">\_copier les droits WMDM sur l' \_ \_ \_ \_ appareil SDMI</span><span class="sxs-lookup"><span data-stu-id="d35c0-137">WMDM\_RIGHTS\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="d35c0-138">Le contenu peut être copié sur un appareil SDMI.</span><span class="sxs-lookup"><span data-stu-id="d35c0-138">Content can be copied to an SDMI device.</span></span>      |



 

</dd> <dt>

<span data-ttu-id="d35c0-139">**dwAppSec**</span><span class="sxs-lookup"><span data-stu-id="d35c0-139">**dwAppSec**</span></span>
</dt> <dd>

<span data-ttu-id="d35c0-140">Tableau d’octets qui spécifie le niveau minimal de sécurité de l’application.</span><span class="sxs-lookup"><span data-stu-id="d35c0-140">Byte array that specifies the minimum level of application security.</span></span>

</dd> <dt>

<span data-ttu-id="d35c0-141">**dwPlaybackCount**</span><span class="sxs-lookup"><span data-stu-id="d35c0-141">**dwPlaybackCount**</span></span>
</dt> <dd>

<span data-ttu-id="d35c0-142">**Valeur DWORD** qui contient le nombre de fois où le contenu peut être rendu.</span><span class="sxs-lookup"><span data-stu-id="d35c0-142">**DWORD** containing the number of remaining times that the content can be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="d35c0-143">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="d35c0-143">**ExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="d35c0-144">Structure [**WMDMDATETIME**](wmdmdatetime.md) contenant la date et l’heure d’expiration du contenu.</span><span class="sxs-lookup"><span data-stu-id="d35c0-144">[**WMDMDATETIME**](wmdmdatetime.md) structure containing the expiration date and time for the content.</span></span> <span data-ttu-id="d35c0-145">Si la licence n’a pas de date d’expiration, le membre **wYear** a la valeur 0xFFFF et tous les autres membres de **WMDMDATETIME** sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="d35c0-145">If the license has no expiration date, the **wYear** member is set to 0xFFFF, and all other members of **WMDMDATETIME** are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d35c0-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d35c0-146">Requirements</span></span>



| <span data-ttu-id="d35c0-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d35c0-147">Requirement</span></span> | <span data-ttu-id="d35c0-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="d35c0-148">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d35c0-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="d35c0-149">Header</span></span><br/> | <dl> <span data-ttu-id="d35c0-150"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d35c0-150"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d35c0-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d35c0-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d35c0-152">**IMDSPStorage :: GetRight**</span><span class="sxs-lookup"><span data-stu-id="d35c0-152">**IMDSPStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[<span data-ttu-id="d35c0-153">**IWMDMStorage :: GetRight**</span><span class="sxs-lookup"><span data-stu-id="d35c0-153">**IWMDMStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[<span data-ttu-id="d35c0-154">**WMDMDATETIME**</span><span class="sxs-lookup"><span data-stu-id="d35c0-154">**WMDMDATETIME**</span></span>](wmdmdatetime.md)
</dt> <dt>

[<span data-ttu-id="d35c0-155">**Structures**</span><span class="sxs-lookup"><span data-stu-id="d35c0-155">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





