---
description: Les \_ constantes d’indicateur de bit LINEDEVCAPFLAGS sont une collection de valeurs booléennes qui décrivent différentes fonctionnalités de périphérique en ligne.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: Constantes LINEDEVCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530007"
---
# <a name="linedevcapflags_-constants"></a><span data-ttu-id="02a90-103">\_Constantes LINEDEVCAPFLAGS</span><span class="sxs-lookup"><span data-stu-id="02a90-103">LINEDEVCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="02a90-104">Les constantes d’indicateur de bit **LINEDEVCAPFLAGS \_** sont une collection de valeurs booléennes qui décrivent différentes fonctionnalités de périphérique en ligne.</span><span class="sxs-lookup"><span data-stu-id="02a90-104">The **LINEDEVCAPFLAGS\_** bit-flag constants are a collection of Booleans describing various line device capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="02a90-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**</span><span class="sxs-lookup"><span data-stu-id="02a90-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS\_CALLHUB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02a90-106">Indique si les hubs d’appel sont pris en charge sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="02a90-106">Indicates whether call hubs are supported on this line.</span></span> <span data-ttu-id="02a90-107">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="02a90-107">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**</span><span class="sxs-lookup"><span data-stu-id="02a90-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02a90-109">Indique si le suivi des concentrateurs d’appels est pris en charge sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="02a90-109">Indicates whether call hub tracking is supported on this line.</span></span> <span data-ttu-id="02a90-110">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="02a90-110">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**</span><span class="sxs-lookup"><span data-stu-id="02a90-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS\_CLOSEDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02a90-112">Spécifie ce qui se produit lorsqu’une ligne ouverte est fermée pendant que l’application appelle active sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="02a90-112">Specifies what happens when an open line is closed while the application has calls active on the line.</span></span> <span data-ttu-id="02a90-113">Si la **valeur est true**, le fournisseur de services supprime (efface) tous les appels actifs sur la ligne lorsque la dernière application qui a ouvert la ligne la ferme avec [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span><span class="sxs-lookup"><span data-stu-id="02a90-113">If **TRUE**, the service provider drops (clears) all active calls on the line when the last application that has opened the line closes it with [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span></span> <span data-ttu-id="02a90-114">Si la **valeur est false**, le fournisseur de services ne supprime pas les appels actifs dans de tels cas.</span><span class="sxs-lookup"><span data-stu-id="02a90-114">If **FALSE**, the service provider does not drop active calls in such cases.</span></span> <span data-ttu-id="02a90-115">Au lieu de cela, les appels restent actifs et sous le contrôle des périphériques externes.</span><span class="sxs-lookup"><span data-stu-id="02a90-115">Instead, the calls remain active and under control of external devices.</span></span> <span data-ttu-id="02a90-116">Un fournisseur de services définit généralement ce bit sur **false** s’il existe un autre périphérique qui peut garder l’appel actif. par exemple, si une ligne analogique a l’ordinateur et que l’ensemble de téléphones se connectent directement à ces derniers dans une configuration de ligne de partie, le téléphone offhook garde automatiquement l’appel actif même après la mise sous tension de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="02a90-116">A service provider typically sets this bit to **FALSE** if there is some other device that can keep the call alive, for example, if an analog line has the computer and phone set both connect directly to them in a party-line configuration, the offhook phone will automatically keep the call active even after the computer powers down.</span></span>

<span data-ttu-id="02a90-117">Les applications doivent vérifier cet indicateur pour déterminer s’il faut avertir l’utilisateur (avec une boîte de dialogue OK/Annuler) que les appels actifs seront perdus.</span><span class="sxs-lookup"><span data-stu-id="02a90-117">Applications should check this flag to determine whether to warn the user (with an OK/Cancel dialog box) that active calls will be lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**</span><span class="sxs-lookup"><span data-stu-id="02a90-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS\_CROSSADDRCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02a90-119">Spécifie si les appels effectués sur des adresses différentes sur cette ligne peuvent être Conférence.</span><span class="sxs-lookup"><span data-stu-id="02a90-119">Specifies whether calls on different addresses on this line can be conferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**</span><span class="sxs-lookup"><span data-stu-id="02a90-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**</span><span class="sxs-lookup"><span data-stu-id="02a90-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**</span><span class="sxs-lookup"><span data-stu-id="02a90-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02a90-123">Ces indicateurs indiquent si le modificateur de chaîne de numérotation « $ », « @ » ou « W » est pris en charge pour un périphérique de ligne donné.</span><span class="sxs-lookup"><span data-stu-id="02a90-123">These flags indicate whether the "$", "@", or "W" dialable string modifier is supported for a given line device.</span></span> <span data-ttu-id="02a90-124">Elle a la **valeur true** si le modificateur est pris en charge ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="02a90-124">It is **TRUE** if the modifier is supported; otherwise, **FALSE**.</span></span> <span data-ttu-id="02a90-125">Le «  ? » (inviter l’utilisateur à continuer la numérotation) n’est jamais pris en charge par un périphérique en ligne.</span><span class="sxs-lookup"><span data-stu-id="02a90-125">The "?" (prompt user to continue dialing) is never supported by a line device.</span></span> <span data-ttu-id="02a90-126">Ces indicateurs permettent à une application de déterminer à l’avance quels modificateurs entraîneraient la génération d’un LINEERR.</span><span class="sxs-lookup"><span data-stu-id="02a90-126">These flags allow an application to determine up front which modifiers would result in the generation of a LINEERR.</span></span> <span data-ttu-id="02a90-127">L’application a le choix de préanalyser des chaînes de numérotation pour les caractères non pris en charge ou de passer directement la chaîne « brute » de [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) au fournisseur dans le cadre de fonctions telles que [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) ou [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) et laisser la fonction générer une erreur pour lui indiquer quel modificateur non pris en charge se produit en premier dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="02a90-127">The application has the choice of pre-scanning dialable strings for unsupported characters or of passing the "raw" string from [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) directly to the provider as part of functions such as [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) or [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) and let the function generate an error to tell it which unsupported modifier occurs first in the string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHLEVCOMP**</span><span class="sxs-lookup"><span data-stu-id="02a90-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS\_HIGHLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02a90-129">Spécifie si les éléments d’informations de compatibilité de haut niveau sont pris en charge sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="02a90-129">Specifies whether high-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWLEVCOMP**</span><span class="sxs-lookup"><span data-stu-id="02a90-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS\_LOWLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02a90-131">Spécifie si les éléments d’informations de compatibilité de bas niveau sont pris en charge sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="02a90-131">Specifies whether low-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="02a90-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS\_MEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02a90-133">Spécifie si les opérations de contrôle de média sont disponibles pour les appels à cette ligne.</span><span class="sxs-lookup"><span data-stu-id="02a90-133">Specifies whether media-control operations are available for calls at this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**\_MSP LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="02a90-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS\_MSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02a90-135">Indique si un fournisseur de services de média (MSP) est associé à la ligne.</span><span class="sxs-lookup"><span data-stu-id="02a90-135">Indicates whether a Media Service Provider (MSP) is associated with the line.</span></span> <span data-ttu-id="02a90-136">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="02a90-136">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**</span><span class="sxs-lookup"><span data-stu-id="02a90-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS\_MULTIPLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02a90-138">Spécifie si [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)ou [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) est en mesure de traiter plusieurs adresses à la fois (comme pour le multiplexage inverse).</span><span class="sxs-lookup"><span data-stu-id="02a90-138">Specifies whether [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI\_lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), or [**TSPI\_lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) is able to deal with multiple addresses at once (as for inverse multiplexing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="02a90-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS \_ PRIVATEOBJECTS**</span><span class="sxs-lookup"><span data-stu-id="02a90-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS\_PRIVATEOBJECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="02a90-140">Indique si [les interfaces spécifiques au fournisseur](./provider-specific-interfaces.md) ont été implémentées.</span><span class="sxs-lookup"><span data-stu-id="02a90-140">Indicates whether [provider-specific Interfaces](./provider-specific-interfaces.md) have been implemented.</span></span> <span data-ttu-id="02a90-141">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="02a90-141">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02a90-142">Notes</span><span class="sxs-lookup"><span data-stu-id="02a90-142">Remarks</span></span>

<span data-ttu-id="02a90-143">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="02a90-143">No extensibility.</span></span> <span data-ttu-id="02a90-144">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="02a90-144">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a90-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02a90-145">Requirements</span></span>



| <span data-ttu-id="02a90-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02a90-146">Requirement</span></span> | <span data-ttu-id="02a90-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="02a90-147">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="02a90-148">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="02a90-148">TAPI version</span></span><br/> | <span data-ttu-id="02a90-149">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="02a90-149">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="02a90-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="02a90-150">Header</span></span><br/>       | <dl> <span data-ttu-id="02a90-151"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="02a90-151"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02a90-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02a90-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a90-153">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="02a90-153">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="02a90-154">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="02a90-154">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="02a90-155">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="02a90-155">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="02a90-156">**lineTranslateAddress**</span><span class="sxs-lookup"><span data-stu-id="02a90-156">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

