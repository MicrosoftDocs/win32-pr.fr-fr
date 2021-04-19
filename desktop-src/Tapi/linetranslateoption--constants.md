---
description: La \_ constante d’indicateur de bit LINETRANSLATEOPTION décrit une option utilisée par la traduction d’adresses.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: Constantes LINETRANSLATEOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537482"
---
# <a name="linetranslateoption_-constants"></a><span data-ttu-id="3287c-103">\_Constantes LINETRANSLATEOPTION</span><span class="sxs-lookup"><span data-stu-id="3287c-103">LINETRANSLATEOPTION\_ Constants</span></span>

<span data-ttu-id="3287c-104">La constante d’indicateur de bit **LINETRANSLATEOPTION \_** décrit une option utilisée par la traduction d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3287c-104">The **LINETRANSLATEOPTION\_** bit-flag constant describes an option used by address translation.</span></span>

<dl> <dt>

<span data-ttu-id="3287c-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION \_ CANCELCALLWAITING**</span><span class="sxs-lookup"><span data-stu-id="3287c-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION\_CANCELCALLWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3287c-106">Si une chaîne d’appel d’annulation est définie pour l’emplacement, la définition de ce bit entraînera l’insertion de cette chaîne au début de la chaîne de numérotation.</span><span class="sxs-lookup"><span data-stu-id="3287c-106">If a Cancel Call Waiting string is defined for the location, setting this bit will cause that string to be inserted at the beginning of the dialable string.</span></span> <span data-ttu-id="3287c-107">Ce mode est couramment utilisé par les applications de télécopie et de modems de données pour empêcher l’interruption des appels en signalant des signaux d’attente.</span><span class="sxs-lookup"><span data-stu-id="3287c-107">This is commonly used by data modem and fax applications to prevent interruption of calls by call waiting beeps.</span></span> <span data-ttu-id="3287c-108">Si aucune chaîne d’appel d’annulation n’est définie pour l’emplacement, ce bit n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="3287c-108">If no Cancel Call Waiting string is defined for the location, this bit has no affect.</span></span> <span data-ttu-id="3287c-109">Notez que les applications qui utilisent ce bit sont recommandées pour définir également le \_ bit sécurisé LINECALLPARAMFLAGS dans le membre **dwCallParamFlags** de la structure [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passée à [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) via le paramètre *lpCallParams* , de sorte que si le périphérique de ligne utilise un mécanisme autre que des chiffres à composer pour supprimer les interruptions d’appel, ce mécanisme sera appelé.</span><span class="sxs-lookup"><span data-stu-id="3287c-109">Note that applications using this bit are advised to also set the LINECALLPARAMFLAGS\_SECURE bit in the **dwCallParamFlags** member of the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in to [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) through the *lpCallParams* parameter, so that if the line device uses a mechanism other than dialable digits to suppress call interrupts then that mechanism will be invoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3287c-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION \_ CARDOVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="3287c-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION\_CARDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3287c-111">La carte d’appel par défaut doit être remplacée par une carte spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3287c-111">The default calling card is to be overridden with a specified one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3287c-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION \_ FORCELD**</span><span class="sxs-lookup"><span data-stu-id="3287c-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION\_FORCELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3287c-113">Cette option force la traduction de l’adresse (nombre) en longue distance.</span><span class="sxs-lookup"><span data-stu-id="3287c-113">This option forces the address (number) to be translated as long distance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3287c-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION \_ FORCELOCAL**</span><span class="sxs-lookup"><span data-stu-id="3287c-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION\_FORCELOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3287c-115">Cette option force la conversion du nombre (adresse) en local.</span><span class="sxs-lookup"><span data-stu-id="3287c-115">This option forces the number (address) to be translated as local.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3287c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3287c-116">Remarks</span></span>

<span data-ttu-id="3287c-117">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="3287c-117">No extensibility.</span></span> <span data-ttu-id="3287c-118">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="3287c-118">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="3287c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3287c-119">Requirements</span></span>



| <span data-ttu-id="3287c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3287c-120">Requirement</span></span> | <span data-ttu-id="3287c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3287c-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3287c-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="3287c-122">TAPI version</span></span><br/> | <span data-ttu-id="3287c-123">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3287c-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3287c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3287c-124">Header</span></span><br/>       | <dl> <span data-ttu-id="3287c-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3287c-125"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3287c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3287c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3287c-127">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="3287c-127">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="3287c-128">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="3287c-128">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="3287c-129">**LINETRANSLATEOUTPUT**</span><span class="sxs-lookup"><span data-stu-id="3287c-129">**LINETRANSLATEOUTPUT**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




