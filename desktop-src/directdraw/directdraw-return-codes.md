---
title: Codes de retour DirectDraw (Ddraw. h)
description: Codes de retour DirectDraw-les erreurs sont représentées par des valeurs négatives et ne peuvent pas être combinées.
ms.assetid: F713193E-3614-4741-B293-D312C170270A
topic_type:
- apiref
api_name:
- DD_OK
- DDERR_ALREADYINITIALIZED
- DDERR_BLTFASTCANTCLIP
- DDERR_CANNOTATTACHSURFACE
- DDERR_CANNOTDETACHSURFACE
- DDERR_CANTCREATEDC
- DDERR_CANTDUPLICATE
- DDERR_CANTLOCKSURFACE
- DDERR_CANTPAGELOCK
- DDERR_CANTPAGEUNLOCK
- DDERR_CLIPPERISUSINGHWND
- DDERR_COLORKEYNOTSET
- DDERR_CURRENTLYNOTAVAIL
- DDERR_DDSCAPSCOMPLEXREQUIRED
- DDERR_DCALREADYCREATED
- DDERR_DEVICEDOESNTOWNSURFACE
- DDERR_DIRECTDRAWALREADYCREATED
- DDERR_EXCEPTION
- DDERR_EXCLUSIVEMODEALREADYSET
- DDERR_EXPIRED
- DDERR_GENERIC
- DDERR_HEIGHTALIGN
- DDERR_HWNDALREADYSET
- DDERR_HWNDSUBCLASSED
- DDERR_IMPLICITLYCREATED
- DDERR_INCOMPATIBLEPRIMARY
- DDERR_INVALIDCAPS
- DDERR_INVALIDCLIPLIST
- DDERR_INVALIDDIRECTDRAWGUID
- DDERR_INVALIDMODE
- DDERR_INVALIDOBJECT
- DDERR_INVALIDPARAMS
- DDERR_INVALIDPIXELFORMAT
- DDERR_INVALIDPOSITION
- DDERR_INVALIDRECT
- DDERR_INVALIDSTREAM
- DDERR_INVALIDSURFACETYPE
- DDERR_LOCKEDSURFACES
- DDERR_MOREDATA
- DDERR_NEWMODE
- DDERR_NO3D
- DDERR_NOALPHAHW
- DDERR_NOBLTHW
- DDERR_NOCLIPLIST
- DDERR_NOCLIPPERATTACHED
- DDERR_NOCOLORCONVHW
- DDERR_NOCOLORKEY
- DDERR_NOCOLORKEYHW
- DDERR_NOCOOPERATIVELEVELSET
- DDERR_NODC
- DDERR_NODDROPSHW
- DDERR_NODIRECTDRAWHW
- DDERR_NODIRECTDRAWSUPPORT
- DDERR_NODRIVERSUPPORT
- DDERR_NOEMULATION
- DDERR_NOEXCLUSIVEMODE
- DDERR_NOFLIPHW
- DDERR_NOFOCUSWINDOW
- DDERR_NOGDI
- DDERR_NOHWND
- DDERR_NOMIPMAPHW
- DDERR_NOMIRRORHW
- DDERR_NOMONITORINFORMATION
- DDERR_NONONLOCALVIDMEM
- DDERR_NOOPTIMIZEHW
- DDERR_NOOVERLAYDEST
- DDERR_NOOVERLAYHW
- DDERR_NOPALETTEATTACHED
- DDERR_NOPALETTEHW
- DDERR_NORASTEROPHW
- DDERR_NOROTATIONHW
- DDERR_NOSTEREOHARDWARE
- DDERR_NOSTRETCHHW
- DDERR_NOSURFACELEFT
- DDERR_NOT4BITCOLOR
- DDERR_NOT4BITCOLORINDEX
- DDERR_NOT8BITCOLOR
- DDERR_NOTAOVERLAYSURFACE
- DDERR_NOTEXTUREHW
- DDERR_NOTFLIPPABLE
- DDERR_NOTFOUND
- DDERR_NOTINITIALIZED
- DDERR_NOTLOADED
- DDERR_NOTLOCKED
- DDERR_NOTPAGELOCKED
- DDERR_NOTPALETTIZED
- DDERR_NOVSYNCHW
- DDERR_NOZBUFFERHW
- DDERR_NOZOVERLAYHW
- DDERR_OUTOFCAPS
- DDERR_OUTOFMEMORY
- DDERR_OUTOFVIDEOMEMORY
- DDERR_OVERLAPPINGRECTS
- DDERR_OVERLAYCANTCLIP
- DDERR_OVERLAYCOLORKEYONLYONEACTIVE
- DDERR_OVERLAYNOTVISIBLE
- DDERR_PALETTEBUSY
- DDERR_PRIMARYSURFACEALREADYEXISTS
- DDERR_REGIONTOOSMALL
- DDERR_SURFACEALREADYATTACHED
- DDERR_SURFACEALREADYDEPENDENT
- DDERR_SURFACEBUSY
- DDERR_SURFACEISOBSCURED
- DDERR_SURFACELOST
- DDERR_SURFACENOTATTACHED
- DDERR_TESTFINISHED
- DDERR_TOOBIGHEIGHT
- DDERR_TOOBIGSIZE
- DDERR_TOOBIGWIDTH
- DDERR_UNSUPPORTED
- DDERR_UNSUPPORTEDFORMAT
- DDERR_UNSUPPORTEDMASK
- DDERR_UNSUPPORTEDMODE
- DDERR_VERTICALBLANKINPROGRESS
- DDERR_VIDEONOTACTIVE
- DDERR_WASSTILLDRAWING
- DDERR_WRONGMODE
- DDERR_XALIGN
api_location:
- Ddraw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d789a233df777d98860e519f7e877a030aba55a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087807"
---
# <a name="directdraw-return-codes"></a><span data-ttu-id="f52e6-103">Codes de retour DirectDraw</span><span class="sxs-lookup"><span data-stu-id="f52e6-103">DirectDraw Return Codes</span></span>

<span data-ttu-id="f52e6-104">Les erreurs sont représentées par des valeurs négatives et ne peuvent pas être combinées.</span><span class="sxs-lookup"><span data-stu-id="f52e6-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="f52e6-105">Ce tableau répertorie les valeurs qui peuvent être retournées par toutes les méthodes des [interfaces DirectDraw](directdraw-interfaces.md) et des [fonctions DirectDraw](directdraw-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f52e6-105">This table lists the values that can be returned by all methods of the [DirectDraw Interfaces](directdraw-interfaces.md) and [DirectDraw Functions](directdraw-functions.md).</span></span> <span data-ttu-id="f52e6-106">Pour obtenir la liste des codes d’erreur que chaque méthode ou fonction peut retourner, consultez la description de la méthode ou de la fonction.</span><span class="sxs-lookup"><span data-stu-id="f52e6-106">For a list of the error codes that each method or function can return, see the method or function description.</span></span>

<dl> <dt>

<span data-ttu-id="f52e6-107"><span id="DD_OK"></span><span id="dd_ok"></span>**JJ \_ OK**</span><span class="sxs-lookup"><span data-stu-id="f52e6-107"><span id="DD_OK"></span><span id="dd_ok"></span>**DD\_OK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-108">La demande s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="f52e6-108">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR \_ ALREADYINITIALIZED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR\_ALREADYINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-110">L’objet a déjà été initialisé.</span><span class="sxs-lookup"><span data-stu-id="f52e6-110">The object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR \_ BLTFASTCANTCLIP**</span><span class="sxs-lookup"><span data-stu-id="f52e6-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR\_BLTFASTCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-112">Un objet DirectDrawClipper est attaché à une surface source qui a été passée dans un appel à la méthode [**IDirectDrawSurface7 :: BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) .</span><span class="sxs-lookup"><span data-stu-id="f52e6-112">A DirectDrawClipper object is attached to a source surface that has passed into a call to the [**IDirectDrawSurface7::BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR \_ CANNOTATTACHSURFACE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR\_CANNOTATTACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-114">Une surface ne peut pas être attachée à une autre surface demandée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-114">A surface cannot be attached to another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR \_ CANNOTDETACHSURFACE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR\_CANNOTDETACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-116">Une surface ne peut pas être détachée d’une autre surface demandée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-116">A surface cannot be detached from another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR \_ CANTCREATEDC**</span><span class="sxs-lookup"><span data-stu-id="f52e6-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR\_CANTCREATEDC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-118">Windows ne peut pas créer d’autres contextes de périphérique (DC), ou un contrôleur de périphérique a demandé une surface indexée lorsque l’aire n’a pas de palette et que le mode d’affichage n’a pas été indexé dans la palette (dans ce cas, DirectDraw ne peut pas sélectionner une palette appropriée dans le contrôleur de l’appareil).</span><span class="sxs-lookup"><span data-stu-id="f52e6-118">Windows cannot create any more device contexts (DCs), or a DC has requested a palette-indexed surface when the surface had no palette and the display mode was not palette-indexed (in this case, DirectDraw cannot select a proper palette into the DC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR \_ CANTDUPLICATE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR\_CANTDUPLICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-120">Les surfaces principales et 3D, ou les surfaces qui sont créées implicitement, ne peuvent pas être dupliquées.</span><span class="sxs-lookup"><span data-stu-id="f52e6-120">Primary and 3-D surfaces, or surfaces that are implicitly created, cannot be duplicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR \_ CANTLOCKSURFACE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR\_CANTLOCKSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-122">L’accès à cette surface est refusé, car une tentative a été effectuée pour verrouiller l’aire principale sans prise en charge de l’interface de contrôle d’affichage (DCI).</span><span class="sxs-lookup"><span data-stu-id="f52e6-122">Access to this surface is refused because an attempt was made to lock the primary surface without Display Control Interface (DCI) support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR \_ CANTPAGELOCK**</span><span class="sxs-lookup"><span data-stu-id="f52e6-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR\_CANTPAGELOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-124">Une tentative de verrouillage de la page d’une surface a échoué.</span><span class="sxs-lookup"><span data-stu-id="f52e6-124">An attempt to page-lock a surface failed.</span></span> <span data-ttu-id="f52e6-125">Le verrou de page ne fonctionne pas sur une surface d’affichage ou une surface primaire émulée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-125">Page lock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR \_ CANTPAGEUNLOCK**</span><span class="sxs-lookup"><span data-stu-id="f52e6-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR\_CANTPAGEUNLOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-127">Une tentative de déverrouillage d’une surface a échoué.</span><span class="sxs-lookup"><span data-stu-id="f52e6-127">An attempt to page-unlock a surface failed.</span></span> <span data-ttu-id="f52e6-128">Le déverrouillage de page ne fonctionne pas sur une surface d’affichage ou une surface primaire émulée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-128">Page unlock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR \_ CLIPPERISUSINGHWND**</span><span class="sxs-lookup"><span data-stu-id="f52e6-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR\_CLIPPERISUSINGHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-130">Une tentative a été effectuée pour définir une liste de clips pour un objet DirectDrawClipper qui analyse déjà un handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f52e6-130">An attempt was made to set a clip list for a DirectDrawClipper object that is already monitoring a window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR \_ COLORKEYNOTSET**</span><span class="sxs-lookup"><span data-stu-id="f52e6-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR\_COLORKEYNOTSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-132">Aucune clé de couleur source n’est spécifiée pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="f52e6-132">No source color key is specified for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR \_ CURRENTLYNOTAVAIL**</span><span class="sxs-lookup"><span data-stu-id="f52e6-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR\_CURRENTLYNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-134">Aucune prise en charge n’est actuellement disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-134">No support is currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR \_ DDSCAPSCOMPLEXREQUIRED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR\_DDSCAPSCOMPLEXREQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-136">Nouveauté de DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="f52e6-136">New for DirectX 7.0.</span></span> <span data-ttu-id="f52e6-137">L’aire de conception requiert l' \_ indicateur complexe DDSCAPS.</span><span class="sxs-lookup"><span data-stu-id="f52e6-137">The surface requires the DDSCAPS\_COMPLEX flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR \_ DCALREADYCREATED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR\_DCALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-139">Un contexte de périphérique (DC) a déjà été retourné pour cette surface.</span><span class="sxs-lookup"><span data-stu-id="f52e6-139">A device context (DC) has already been returned for this surface.</span></span> <span data-ttu-id="f52e6-140">Un seul contrôleur de périphérique peut être récupéré pour chaque surface.</span><span class="sxs-lookup"><span data-stu-id="f52e6-140">Only one DC can be retrieved for each surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR \_ DEVICEDOESNTOWNSURFACE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR\_DEVICEDOESNTOWNSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-142">Les surfaces créées par un appareil DirectDraw ne peuvent pas être utilisées directement par un autre appareil DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="f52e6-142">Surfaces created by one DirectDraw device cannot be used directly by another DirectDraw device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR \_ DIRECTDRAWALREADYCREATED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR\_DIRECTDRAWALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-144">Un objet DirectDraw représentant ce pilote a déjà été créé pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="f52e6-144">A DirectDraw object representing this driver has already been created for this process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**\_exception DDerr**</span><span class="sxs-lookup"><span data-stu-id="f52e6-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**DDERR\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-146">Une exception s’est produite lors de l’exécution de l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-146">An exception was encountered while performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR \_ EXCLUSIVEMODEALREADYSET**</span><span class="sxs-lookup"><span data-stu-id="f52e6-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR\_EXCLUSIVEMODEALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-148">Une tentative a été effectuée pour définir le niveau coopératif lorsqu’il a déjà été défini sur exclusif.</span><span class="sxs-lookup"><span data-stu-id="f52e6-148">An attempt was made to set the cooperative level when it was already set to exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR \_ expiré**</span><span class="sxs-lookup"><span data-stu-id="f52e6-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-150">Les données ont expiré et ne sont donc plus valides.</span><span class="sxs-lookup"><span data-stu-id="f52e6-150">The data has expired and is therefore no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR \_ générique**</span><span class="sxs-lookup"><span data-stu-id="f52e6-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-152">Il existe une condition d’erreur non définie.</span><span class="sxs-lookup"><span data-stu-id="f52e6-152">There is an undefined error condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR \_ HEIGHTALIGN**</span><span class="sxs-lookup"><span data-stu-id="f52e6-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR\_HEIGHTALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-154">La hauteur du rectangle fourni n’est pas un multiple de l’alignement requis.</span><span class="sxs-lookup"><span data-stu-id="f52e6-154">The height of the provided rectangle is not a multiple of the required alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR \_ HWNDALREADYSET**</span><span class="sxs-lookup"><span data-stu-id="f52e6-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR\_HWNDALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-156">Le descripteur de la fenêtre de niveau coopératif DirectDraw a déjà été défini.</span><span class="sxs-lookup"><span data-stu-id="f52e6-156">The DirectDraw cooperative-level window handle has already been set.</span></span> <span data-ttu-id="f52e6-157">Elle ne peut pas être réinitialisée lors de la création de surfaces ou de palettes dans le processus.</span><span class="sxs-lookup"><span data-stu-id="f52e6-157">It cannot be reset while the process has surfaces or palettes created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR \_ HWNDSUBCLASSED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR\_HWNDSUBCLASSED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-159">Impossible de restaurer l’état de DirectDraw car le handle de la fenêtre de niveau coopératif DirectDraw a été sous-classé.</span><span class="sxs-lookup"><span data-stu-id="f52e6-159">DirectDraw is prevented from restoring state because the DirectDraw cooperative-level window handle has been subclassed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR \_ IMPLICITLYCREATED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR\_IMPLICITLYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-161">Impossible de restaurer la surface, car il s’agit d’une surface créée implicitement.</span><span class="sxs-lookup"><span data-stu-id="f52e6-161">The surface cannot be restored because it is an implicitly created surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR \_ INCOMPATIBLEPRIMARY**</span><span class="sxs-lookup"><span data-stu-id="f52e6-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR\_INCOMPATIBLEPRIMARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-163">La demande de création d’aire principale ne correspond pas à la surface primaire existante.</span><span class="sxs-lookup"><span data-stu-id="f52e6-163">The primary surface creation request does not match the existing primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR \_ INVALIDCAPS**</span><span class="sxs-lookup"><span data-stu-id="f52e6-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR\_INVALIDCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-165">Un ou plusieurs des bits de fonctionnalité passés à la fonction de rappel sont incorrects.</span><span class="sxs-lookup"><span data-stu-id="f52e6-165">One or more of the capability bits passed to the callback function are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR \_ INVALIDCLIPLIST**</span><span class="sxs-lookup"><span data-stu-id="f52e6-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR\_INVALIDCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-167">DirectDraw ne prend pas en charge la liste de séquences fournie.</span><span class="sxs-lookup"><span data-stu-id="f52e6-167">DirectDraw does not support the provided clip list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR \_ INVALIDDIRECTDRAWGUID**</span><span class="sxs-lookup"><span data-stu-id="f52e6-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR\_INVALIDDIRECTDRAWGUID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-169">L’identificateur global unique (GUID) passé à la fonction [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) n’est pas un identificateur de pilote DirectDraw valide.</span><span class="sxs-lookup"><span data-stu-id="f52e6-169">The globally unique identifier (GUID) passed to the [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) function is not a valid DirectDraw driver identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR \_ INVALIDMODE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR\_INVALIDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-171">DirectDraw ne prend pas en charge le mode demandé.</span><span class="sxs-lookup"><span data-stu-id="f52e6-171">DirectDraw does not support the requested mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR \_ INVALIDOBJECT**</span><span class="sxs-lookup"><span data-stu-id="f52e6-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR\_INVALIDOBJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-173">DirectDraw a reçu un pointeur qui était un objet DirectDraw non valide.</span><span class="sxs-lookup"><span data-stu-id="f52e6-173">DirectDraw received a pointer that was an invalid DirectDraw object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR \_ INVALIDPARAMS**</span><span class="sxs-lookup"><span data-stu-id="f52e6-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR\_INVALIDPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-175">Un ou plusieurs des paramètres passés à la méthode sont incorrects.</span><span class="sxs-lookup"><span data-stu-id="f52e6-175">One or more of the parameters passed to the method are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR \_ INVALIDPIXELFORMAT**</span><span class="sxs-lookup"><span data-stu-id="f52e6-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR\_INVALIDPIXELFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-177">Le format de pixel n’était pas valide comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="f52e6-177">The pixel format was invalid as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR \_ INVALIDPOSITION**</span><span class="sxs-lookup"><span data-stu-id="f52e6-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR\_INVALIDPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-179">La position de la superposition sur la destination n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="f52e6-179">The position of the overlay on the destination is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR \_ INVALIDRECT**</span><span class="sxs-lookup"><span data-stu-id="f52e6-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR\_INVALIDRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-181">Le rectangle fourni n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="f52e6-181">The provided rectangle was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR \_ INVALIDSTREAM**</span><span class="sxs-lookup"><span data-stu-id="f52e6-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR\_INVALIDSTREAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-183">Le flux spécifié contient des données non valides.</span><span class="sxs-lookup"><span data-stu-id="f52e6-183">The specified stream contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR \_ INVALIDSURFACETYPE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR\_INVALIDSURFACETYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-185">Le type de surface est incorrect.</span><span class="sxs-lookup"><span data-stu-id="f52e6-185">The surface was of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR \_ LOCKEDSURFACES**</span><span class="sxs-lookup"><span data-stu-id="f52e6-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR\_LOCKEDSURFACES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-187">Une ou plusieurs surfaces sont verrouillées, provoquant ainsi l’échec de l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-187">One or more surfaces are locked, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR \_ MOREDATA**</span><span class="sxs-lookup"><span data-stu-id="f52e6-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR\_MOREDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-189">Il y a plus de données disponibles que la taille de la mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-189">There is more data available than the specified buffer size can hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR \_ NEWMODE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR\_NEWMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-191">Nouveauté de DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="f52e6-191">New for DirectX 7.0.</span></span> <span data-ttu-id="f52e6-192">Lorsque [**IDirectDraw7 :: StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) est appelé avec l' \_ indicateur DDSMT ISTESTREQUIRED, il peut retourner cette valeur pour indiquer qu’une partie ou la totalité des résolutions peut et doit être testée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-192">When [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) is called with the DDSMT\_ISTESTREQUIRED flag, it might return this value to denote that some or all of the resolutions can and should be tested.</span></span> <span data-ttu-id="f52e6-193">[**IDirectDraw7 :: EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) retourne cette valeur pour indiquer que le test a basculé vers un nouveau mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f52e6-193">[**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) returns this value to indicate that the test has switched to a new display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR \_ NO3D**</span><span class="sxs-lookup"><span data-stu-id="f52e6-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR\_NO3D**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-195">Aucun matériel ou émulation 3D n’est présent.</span><span class="sxs-lookup"><span data-stu-id="f52e6-195">No 3-D hardware or emulation is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR \_ NOALPHAHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR\_NOALPHAHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-197">Aucun matériel d’accélération alpha n’est présent ou disponible, ce qui entraîne l’échec de l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-197">No alpha-acceleration hardware is present or available, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR \_ NOBLTHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR\_NOBLTHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-199">Aucun bloc de bits de transfert de matériel n’est présent.</span><span class="sxs-lookup"><span data-stu-id="f52e6-199">No bit block transferring hardware is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR \_ NOCLIPLIST**</span><span class="sxs-lookup"><span data-stu-id="f52e6-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR\_NOCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-201">Aucune liste de clips n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-201">No clip list is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR \_ NOCLIPPERATTACHED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR\_NOCLIPPERATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-203">Aucun objet DirectDrawClipper n’est attaché à l’objet surface.</span><span class="sxs-lookup"><span data-stu-id="f52e6-203">No DirectDrawClipper object is attached to the surface object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR \_ NOCOLORCONVHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR\_NOCOLORCONVHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-205">Aucun matériel de conversion de couleurs n’est présent ou disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-205">No color-conversion hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR \_ NOCOLORKEY**</span><span class="sxs-lookup"><span data-stu-id="f52e6-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR\_NOCOLORKEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-207">La surface n’a actuellement pas de clé de couleur.</span><span class="sxs-lookup"><span data-stu-id="f52e6-207">The surface does not currently have a color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR \_ NOCOLORKEYHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR\_NOCOLORKEYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-209">Il n’existe aucune prise en charge matérielle pour la clé de couleur de destination.</span><span class="sxs-lookup"><span data-stu-id="f52e6-209">There is no hardware support for the destination color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR \_ NOCOOPERATIVELEVELSET**</span><span class="sxs-lookup"><span data-stu-id="f52e6-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR\_NOCOOPERATIVELEVELSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-211">Une fonction Create a été appelée sans la méthode [**IDirectDraw7 :: SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) .</span><span class="sxs-lookup"><span data-stu-id="f52e6-211">A create function was called without the [**IDirectDraw7::SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR \_ nodC**</span><span class="sxs-lookup"><span data-stu-id="f52e6-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR\_NODC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-213">Aucun contexte de périphérique (DC) n’a jamais été créé pour cette surface.</span><span class="sxs-lookup"><span data-stu-id="f52e6-213">No device context (DC) has ever been created for this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR \_ NODDROPSHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR\_NODDROPSHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-215">Aucun matériel de l’opération Raster (ROP) DirectDraw n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-215">No DirectDraw raster-operation (ROP) hardware is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR \_ NODIRECTDRAWHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR\_NODIRECTDRAWHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-217">La création d’objets DirectDraw uniquement sur le matériel est impossible ; le pilote ne prend en charge aucun matériel.</span><span class="sxs-lookup"><span data-stu-id="f52e6-217">Hardware-only DirectDraw object creation is not possible; the driver does not support any hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR \_ NODIRECTDRAWSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="f52e6-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR\_NODIRECTDRAWSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-219">La prise en charge de DirectDraw n’est pas possible avec le pilote d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="f52e6-219">DirectDraw support is not possible with the current display driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR \_ NODRIVERSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="f52e6-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR\_NODRIVERSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-221">Nouveauté de DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="f52e6-221">New for DirectX 7.0.</span></span> <span data-ttu-id="f52e6-222">Le test ne peut pas se poursuivre, car le pilote de carte d’affichage n’énumère pas les fréquences d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="f52e6-222">Testing cannot proceed because the display adapter driver does not enumerate refresh rates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR \_ NOémulation**</span><span class="sxs-lookup"><span data-stu-id="f52e6-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR\_NOEMULATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-224">L’émulation de logiciel n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-224">Software emulation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR \_ NOEXCLUSIVEMODE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR\_NOEXCLUSIVEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-226">L’opération nécessite que l’application soit en mode exclusif, mais l’application n’a pas le mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="f52e6-226">The operation requires the application to have exclusive mode, but the application does not have exclusive mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR \_ NOFLIPHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR\_NOFLIPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-228">Le renversement des surfaces visibles n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f52e6-228">Flipping visible surfaces is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR \_ NOFOCUSWINDOW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR\_NOFOCUSWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-230">Une tentative de création ou de définition d’une fenêtre d’appareil a été effectuée sans définir au préalable la fenêtre de focus.</span><span class="sxs-lookup"><span data-stu-id="f52e6-230">An attempt was made to create or set a device window without first setting the focus window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR \_ NOGDI**</span><span class="sxs-lookup"><span data-stu-id="f52e6-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR\_NOGDI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-232">Aucun GDI n’est présent.</span><span class="sxs-lookup"><span data-stu-id="f52e6-232">No GDI is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR \_ NOHWND**</span><span class="sxs-lookup"><span data-stu-id="f52e6-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR\_NOHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-234">La notification Clipper requiert un handle de fenêtre ou aucun handle de fenêtre n’a été défini précédemment comme handle de fenêtre de niveau coopératif.</span><span class="sxs-lookup"><span data-stu-id="f52e6-234">Clipper notification requires a window handle, or no window handle has been previously set as the cooperative level window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR \_ NOMIPMAPHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR\_NOMIPMAPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-236">Aucun matériel de mappage de texture qui prend en charge le mipmap n’est présent ou disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-236">No mipmap-capable texture mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR \_ NOMIRRORHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR\_NOMIRRORHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-238">Aucun matériel de mise en miroir n’est présent ou disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-238">No mirroring hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR \_ NOMONITORINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="f52e6-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR\_NOMONITORINFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-240">Nouveauté de DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="f52e6-240">New for DirectX 7.0.</span></span> <span data-ttu-id="f52e6-241">Le test ne peut pas se poursuivre, car l’analyse n’a pas de données EDID associées.</span><span class="sxs-lookup"><span data-stu-id="f52e6-241">Testing cannot proceed because the monitor has no associated EDID data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR \_ NONONLOCALVIDMEM**</span><span class="sxs-lookup"><span data-stu-id="f52e6-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR\_NONONLOCALVIDMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-243">Une tentative a été effectuée pour allouer de la mémoire vidéo non locale à partir d’un appareil qui ne prend pas en charge la mémoire vidéo non locale.</span><span class="sxs-lookup"><span data-stu-id="f52e6-243">An attempt was made to allocate nonlocal video memory from a device that does not support nonlocal video memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR \_ NOOPTIMIZEHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR\_NOOPTIMIZEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-245">L’appareil ne prend pas en charge les surfaces optimisées.</span><span class="sxs-lookup"><span data-stu-id="f52e6-245">The device does not support optimized surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR \_ NOOVERLAYDEST**</span><span class="sxs-lookup"><span data-stu-id="f52e6-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR\_NOOVERLAYDEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-247">La méthode [**IDirectDrawSurface7 :: GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) est appelée sur une superposition sur laquelle la méthode [**IDirectDrawSurface7 :: UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) n’a pas été appelée pour établir comme destination.</span><span class="sxs-lookup"><span data-stu-id="f52e6-247">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method is called on an overlay that the [**IDirectDrawSurface7::UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) method has not been called on to establish as a destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR \_ NOOVERLAYHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR\_NOOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-249">Aucun matériel de superposition n’est présent ou disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-249">No overlay hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR \_ NOPALETTEATTACHED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR\_NOPALETTEATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-251">Aucun objet palette n’est attaché à cette surface.</span><span class="sxs-lookup"><span data-stu-id="f52e6-251">No palette object is attached to this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR \_ NOPALETTEHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR\_NOPALETTEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-253">Il n’existe pas de prise en charge matérielle pour les palettes de 16 ou 256 couleurs.</span><span class="sxs-lookup"><span data-stu-id="f52e6-253">There is no hardware support for 16- or 256-color palettes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR \_ NORASTEROPHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR\_NORASTEROPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-255">Aucun matériel de l’opération Raster appropriée n’est présent ou disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-255">No appropriate raster-operation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR \_ NOROTATIONHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR\_NOROTATIONHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-257">Aucun matériel de rotation n’est présent ou disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-257">No rotation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR \_ NOSTEREOHARDWARE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR\_NOSTEREOHARDWARE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-259">Aucun matériel stéréo n’est présent ou disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-259">There is no stereo hardware present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR \_ NOSTRETCHHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR\_NOSTRETCHHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-261">Il n’existe pas de prise en charge matérielle pour l’étirement.</span><span class="sxs-lookup"><span data-stu-id="f52e6-261">There is no hardware support for stretching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR \_ NOSURFACELEFT**</span><span class="sxs-lookup"><span data-stu-id="f52e6-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR\_NOSURFACELEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-263">Aucun matériel ne prend en charge les surfaces stéréo.</span><span class="sxs-lookup"><span data-stu-id="f52e6-263">There is no hardware present that supports stereo surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR \_ NOT4BITCOLOR**</span><span class="sxs-lookup"><span data-stu-id="f52e6-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR\_NOT4BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-265">L’objet DirectDrawSurface n’utilise pas une palette de couleurs de 4 bits et l’opération demandée requiert une palette de couleurs de 4 bits.</span><span class="sxs-lookup"><span data-stu-id="f52e6-265">The DirectDrawSurface object is not using a 4-bit color palette, and the requested operation requires a 4-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR \_ NOT4BITCOLORINDEX**</span><span class="sxs-lookup"><span data-stu-id="f52e6-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR\_NOT4BITCOLORINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-267">L’objet DirectDrawSurface n’utilise pas de palette d’index de couleurs de 4 bits et l’opération demandée requiert une palette d’index de couleurs de 4 bits.</span><span class="sxs-lookup"><span data-stu-id="f52e6-267">The DirectDrawSurface object is not using a 4-bit color index palette, and the requested operation requires a 4-bit color index palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR \_ NOT8BITCOLOR**</span><span class="sxs-lookup"><span data-stu-id="f52e6-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR\_NOT8BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-269">L’objet DirectDrawSurface n’utilise pas une palette de couleurs de 8 bits et l’opération demandée requiert une palette de couleurs de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="f52e6-269">The DirectDrawSurface object is not using an 8-bit color palette, and the requested operation requires an 8-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR \_ NOTAOVERLAYSURFACE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR\_NOTAOVERLAYSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-271">Un composant de superposition est appelé pour une surface non superposée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-271">An overlay component is called for a nonoverlay surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR \_ NOTEXTUREHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR\_NOTEXTUREHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-273">Impossible d’effectuer l’opération, car aucun matériel de mappage de texture n’est présent ou disponible.</span><span class="sxs-lookup"><span data-stu-id="f52e6-273">The operation cannot be carried out because no texture-mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR \_ NOTFLIPPABLE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR\_NOTFLIPPABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-275">Une tentative a été effectuée pour retourner une surface qui ne peut pas être retournée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-275">An attempt was made to flip a surface that cannot be flipped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR \_ NotFound**</span><span class="sxs-lookup"><span data-stu-id="f52e6-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-277">L'élément demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="f52e6-277">The requested item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR \_ NOTINITIALIZED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR\_NOTINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-279">Une tentative d’appel d’une méthode d’interface d’un objet DirectDraw créé par [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) a été effectuée avant l’initialisation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f52e6-279">An attempt was made to call an interface method of a DirectDraw object created by [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) before the object was initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR \_ NOTLOADED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR\_NOTLOADED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-281">La surface est une surface optimisée, mais elle n’a pas encore été allouée à aucune mémoire.</span><span class="sxs-lookup"><span data-stu-id="f52e6-281">The surface is an optimized surface, but it has not yet been allocated any memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR \_ NOTLOCKED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR\_NOTLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-283">Une tentative de déverrouillage d’une surface qui n’a pas été verrouillée a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-283">An attempt was made to unlock a surface that was not locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR \_ NOTPAGELOCKED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR\_NOTPAGELOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-285">Une tentative a été effectuée pour déverrouiller une surface sans verrous de page en attente.</span><span class="sxs-lookup"><span data-stu-id="f52e6-285">An attempt was made to page-unlock a surface with no outstanding page locks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR \_ NOTPALETTIZED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR\_NOTPALETTIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-287">La surface utilisée n’est pas une surface basée sur la palette.</span><span class="sxs-lookup"><span data-stu-id="f52e6-287">The surface being used is not a palette-based surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR \_ NOVSYNCHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR\_NOVSYNCHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-289">Il n’existe pas de prise en charge matérielle des opérations synchronisées verticales vides.</span><span class="sxs-lookup"><span data-stu-id="f52e6-289">There is no hardware support for vertical blank synchronized operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR \_ NOZBUFFERHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR\_NOZBUFFERHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-291">L’opération de création d’une mémoire tampon z dans l’affichage de la mémoire ou d’un transfert de blocs binaires (BitBlt) à l’aide d’une mémoire tampon z ne peut pas être effectuée car il n’y a pas de prise en charge matérielle pour les mémoires tampons z.</span><span class="sxs-lookup"><span data-stu-id="f52e6-291">The operation to create a z-buffer in display memory or to perform a bit block transfer (bitblt), using a z-buffer cannot be carried out because there is no hardware support for z-buffers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR \_ NOZOVERLAYHW**</span><span class="sxs-lookup"><span data-stu-id="f52e6-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR\_NOZOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-293">Les surfaces de recouvrement ne peuvent pas être empilées en z, en fonction de l’ordre de plan car le matériel ne prend pas en charge l’ordre de plan des superpositions.</span><span class="sxs-lookup"><span data-stu-id="f52e6-293">The overlay surfaces cannot be z-layered, based on the z-order because the hardware does not support z-ordering of overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR \_ OUTOFCAPS**</span><span class="sxs-lookup"><span data-stu-id="f52e6-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR\_OUTOFCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-295">Le matériel nécessaire pour l’opération demandée a déjà été alloué.</span><span class="sxs-lookup"><span data-stu-id="f52e6-295">The hardware needed for the requested operation has already been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="f52e6-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-297">DirectDraw ne dispose pas de suffisamment de mémoire pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f52e6-297">DirectDraw does not have enough memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR \_ OUTOFVIDEOMEMORY**</span><span class="sxs-lookup"><span data-stu-id="f52e6-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR\_OUTOFVIDEOMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-299">DirectDraw n’a pas suffisamment de mémoire d’affichage pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f52e6-299">DirectDraw does not have enough display memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR \_ OVERLAPPINGRECTS**</span><span class="sxs-lookup"><span data-stu-id="f52e6-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR\_OVERLAPPINGRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-301">Les rectangles source et de destination se trouvent sur la même surface et se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="f52e6-301">The source and destination rectangles are on the same surface and overlap each other.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR \_ OVERLAYCANTCLIP**</span><span class="sxs-lookup"><span data-stu-id="f52e6-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR\_OVERLAYCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-303">Le matériel ne prend pas en charge les superpositions ajustées.</span><span class="sxs-lookup"><span data-stu-id="f52e6-303">The hardware does not support clipped overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR \_ OVERLAYCOLORKEYONLYONEACTIVE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR\_OVERLAYCOLORKEYONLYONEACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-305">Une tentative a été effectuée pour qu’une clé de couleur soit active sur une superposition.</span><span class="sxs-lookup"><span data-stu-id="f52e6-305">An attempt was made to have more than one color key active on an overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR \_ OVERLAYNOTVISIBLE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR\_OVERLAYNOTVISIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-307">La méthode [**IDirectDrawSurface7 :: GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) a été appelée sur une superposition masquée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-307">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method was called on a hidden overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR \_ PALETTEBUSY**</span><span class="sxs-lookup"><span data-stu-id="f52e6-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR\_PALETTEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-309">L’accès à cette palette est refusé car la palette est verrouillée par un autre thread.</span><span class="sxs-lookup"><span data-stu-id="f52e6-309">Access to this palette is refused because the palette is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR \_ PRIMARYSURFACEALREADYEXISTS**</span><span class="sxs-lookup"><span data-stu-id="f52e6-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR\_PRIMARYSURFACEALREADYEXISTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-311">Ce processus a déjà créé une surface principale.</span><span class="sxs-lookup"><span data-stu-id="f52e6-311">This process has already created a primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**DDERR \_ REGIONTOOSMALL**</span><span class="sxs-lookup"><span data-stu-id="f52e6-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**DDERR\_REGIONTOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-313">La région transmise à la méthode [**IDirectDrawClipper :: GetClipList**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) est trop petite.</span><span class="sxs-lookup"><span data-stu-id="f52e6-313">The region passed to the [**IDirectDrawClipper::GetClipList**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) method is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR \_ SURFACEALREADYATTACHED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR\_SURFACEALREADYATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-315">Une tentative a été effectuée pour attacher une surface à une autre surface à laquelle elle est déjà attachée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-315">An attempt was made to attach a surface to another surface to which it is already attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR \_ SURFACEALREADYDEPENDENT**</span><span class="sxs-lookup"><span data-stu-id="f52e6-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR\_SURFACEALREADYDEPENDENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-317">Une tentative a été effectuée pour faire d’une surface une dépendance d’une autre surface sur laquelle elle est déjà dépendante.</span><span class="sxs-lookup"><span data-stu-id="f52e6-317">An attempt was made to make a surface a dependency of another surface on which it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR \_ SURFACEBUSY**</span><span class="sxs-lookup"><span data-stu-id="f52e6-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR\_SURFACEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-319">L’accès à la surface est refusé, car la surface est verrouillée par un autre thread.</span><span class="sxs-lookup"><span data-stu-id="f52e6-319">Access to the surface is refused because the surface is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR \_ SURFACEISOBSCURED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR\_SURFACEISOBSCURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-321">L’accès à la surface est refusé, car la surface est obscurcie.</span><span class="sxs-lookup"><span data-stu-id="f52e6-321">Access to the surface is refused because the surface is obscured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR \_ SURFACELOST**</span><span class="sxs-lookup"><span data-stu-id="f52e6-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR\_SURFACELOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-323">L’accès à la surface est refusé car la mémoire de surface a disparu.</span><span class="sxs-lookup"><span data-stu-id="f52e6-323">Access to the surface is refused because the surface memory is gone.</span></span> <span data-ttu-id="f52e6-324">Appelez la méthode [**IDirectDrawSurface7 :: Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) sur cette surface pour restaurer la mémoire qui lui est associée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-324">Call the [**IDirectDrawSurface7::Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) method on this surface to restore the memory associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR \_ SURFACENOTATTACHED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR\_SURFACENOTATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-326">La surface demandée n’est pas attachée.</span><span class="sxs-lookup"><span data-stu-id="f52e6-326">The requested surface is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR \_ TESTFINISHED**</span><span class="sxs-lookup"><span data-stu-id="f52e6-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR\_TESTFINISHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-328">Nouveauté de DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="f52e6-328">New for DirectX 7.0.</span></span> <span data-ttu-id="f52e6-329">Lorsqu’elle est retournée par la méthode [**IDirectDraw7 :: StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) , cette valeur signifie qu’aucun test n’a pu être lancé, car toutes les résolutions choisies pour le test ont déjà des informations sur la fréquence d’actualisation dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f52e6-329">When returned by the [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) method, this value means that no test could be initiated because all the resolutions chosen for testing already have refresh rate information in the registry.</span></span> <span data-ttu-id="f52e6-330">Lorsqu’elle est retournée par [**IDirectDraw7 :: EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode), la valeur signifie que DirectDraw a terminé un test de fréquence d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="f52e6-330">When returned by [**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode), the value means that DirectDraw has completed a refresh rate test.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR \_ TOOBIGHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="f52e6-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR\_TOOBIGHEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-332">La hauteur demandée par DirectDraw est trop importante.</span><span class="sxs-lookup"><span data-stu-id="f52e6-332">The height requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR \_ TOOBIGSIZE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR\_TOOBIGSIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-334">La taille demandée par DirectDraw est trop importante.</span><span class="sxs-lookup"><span data-stu-id="f52e6-334">The size requested by DirectDraw is too large.</span></span> <span data-ttu-id="f52e6-335">Toutefois, la hauteur et la largeur individuelles sont des tailles valides.</span><span class="sxs-lookup"><span data-stu-id="f52e6-335">However, the individual height and width are valid sizes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR \_ TOOBIGWIDTH**</span><span class="sxs-lookup"><span data-stu-id="f52e6-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR\_TOOBIGWIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-337">La largeur demandée par DirectDraw est trop importante.</span><span class="sxs-lookup"><span data-stu-id="f52e6-337">The width requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR \_ non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="f52e6-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-339">L'opération n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f52e6-339">The operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR \_ UNSUPPORTEDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="f52e6-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR\_UNSUPPORTEDFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-341">Le format de pixel demandé n’est pas pris en charge par DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="f52e6-341">The pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR \_ UNSUPPORTEDMASK**</span><span class="sxs-lookup"><span data-stu-id="f52e6-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR\_UNSUPPORTEDMASK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-343">Le masque de masque de pixels dans le format de pixel demandé n’est pas pris en charge par DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="f52e6-343">The bitmask in the pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR \_ UNSUPPORTEDMODE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR\_UNSUPPORTEDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-345">L’affichage est actuellement dans un mode non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f52e6-345">The display is currently in an unsupported mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR \_ VERTICALBLANKINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="f52e6-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR\_VERTICALBLANKINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-347">Un espace vertical est en cours.</span><span class="sxs-lookup"><span data-stu-id="f52e6-347">A vertical blank is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**DDERR \_ VIDEONOTACTIVE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**DDERR\_VIDEONOTACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-349">Le port vidéo n’est pas actif.</span><span class="sxs-lookup"><span data-stu-id="f52e6-349">The video port is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR \_ WASSTILLDRAWING**</span><span class="sxs-lookup"><span data-stu-id="f52e6-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR\_WASSTILLDRAWING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-351">L’opération BitBlt précédente qui transfère des informations vers ou à partir de cette surface est incomplète.</span><span class="sxs-lookup"><span data-stu-id="f52e6-351">The previous bitblt operation that is transferring information to or from this surface is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR \_ WRONGMODE**</span><span class="sxs-lookup"><span data-stu-id="f52e6-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR\_WRONGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-353">Cette surface ne peut pas être restaurée, car elle a été créée dans un autre mode.</span><span class="sxs-lookup"><span data-stu-id="f52e6-353">This surface cannot be restored because it was created in a different mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f52e6-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR \_ XALIGN**</span><span class="sxs-lookup"><span data-stu-id="f52e6-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR\_XALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f52e6-355">Le rectangle fourni n’a pas été aligné horizontalement sur une limite requise.</span><span class="sxs-lookup"><span data-stu-id="f52e6-355">The provided rectangle was not horizontally aligned on a required boundary.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f52e6-356">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f52e6-356">Requirements</span></span>



| <span data-ttu-id="f52e6-357">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f52e6-357">Requirement</span></span> | <span data-ttu-id="f52e6-358">Valeur</span><span class="sxs-lookup"><span data-stu-id="f52e6-358">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f52e6-359">En-tête</span><span class="sxs-lookup"><span data-stu-id="f52e6-359">Header</span></span><br/> | <dl> <span data-ttu-id="f52e6-360"><dt>Ddraw. h</dt></span><span class="sxs-lookup"><span data-stu-id="f52e6-360"><dt>Ddraw.h</dt></span></span> </dl> |



 

