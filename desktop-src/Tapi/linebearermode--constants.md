---
description: Les \_ constantes d’indicateur de bit LINEBEARERMODE décrivent les différents modes de support d’un appel.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: Constantes LINEBEARERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537884"
---
# <a name="linebearermode_-constants"></a><span data-ttu-id="18154-103">\_Constantes LINEBEARERMODE</span><span class="sxs-lookup"><span data-stu-id="18154-103">LINEBEARERMODE\_ Constants</span></span>

<span data-ttu-id="18154-104">Les constantes d’indicateur de bit **LINEBEARERMODE \_** décrivent les différents modes de support d’un appel.</span><span class="sxs-lookup"><span data-stu-id="18154-104">The **LINEBEARERMODE\_** bit-flag constants describe different bearer modes of a call.</span></span> <span data-ttu-id="18154-105">Lorsqu’une application effectue un appel, elle peut demander un mode de support spécifique.</span><span class="sxs-lookup"><span data-stu-id="18154-105">When an application makes a call, it can request a specific bearer mode.</span></span> <span data-ttu-id="18154-106">Ces modes permettent de sélectionner une certaine qualité de service pour la connexion demandée à partir du réseau téléphonique sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="18154-106">These modes are used to select a certain quality of service for the requested connection from the underlying telephone network.</span></span> <span data-ttu-id="18154-107">Les modes de support disponibles sur une ligne donnée sont une fonctionnalité de l’appareil de la ligne.</span><span class="sxs-lookup"><span data-stu-id="18154-107">Bearer modes available on a given line are a device capability of the line.</span></span>

<dl> <dt>

<span data-ttu-id="18154-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**</span><span class="sxs-lookup"><span data-stu-id="18154-108"><span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE\_ALTSPEECHDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18154-109">Autre transfert de données vocales ou non restreintes sur le même appel (RNIS).</span><span class="sxs-lookup"><span data-stu-id="18154-109">The alternate transfer of speech or unrestricted data on the same call (ISDN).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18154-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**\_données LINEBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="18154-110"><span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**LINEBEARERMODE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18154-111">Transfert de données non restreintes sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="18154-111">The unrestricted data transfer on the call.</span></span> <span data-ttu-id="18154-112">Le débit de données est spécifié séparément.</span><span class="sxs-lookup"><span data-stu-id="18154-112">The data rate is specified separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18154-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ Multiuse**</span><span class="sxs-lookup"><span data-stu-id="18154-113"><span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE\_MULTIUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18154-114">Mode multi-multiple défini par RNIS.</span><span class="sxs-lookup"><span data-stu-id="18154-114">The multiuse mode defined by ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18154-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**</span><span class="sxs-lookup"><span data-stu-id="18154-115"><span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE\_NONCALLSIGNALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18154-116">Cela correspond à une connexion de signal non associée à un appel entre l’application et le fournisseur de services ou le commutateur (traitée comme un flux de média par TAPI).</span><span class="sxs-lookup"><span data-stu-id="18154-116">This corresponds to a non-call-associated signaling connection from the application to the service provider or switch (treated as a media stream by TAPI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18154-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE \_ passthrough**</span><span class="sxs-lookup"><span data-stu-id="18154-117"><span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE\_PASSTHROUGH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18154-118">Lorsqu’un appel est actif dans LINEBEARERMODE \_ passthrough, le fournisseur de services offre un accès direct au matériel attaché pour le contrôle par l’application.</span><span class="sxs-lookup"><span data-stu-id="18154-118">When a call is active in LINEBEARERMODE\_PASSTHROUGH, the service provider gives direct access to the attached hardware for control by the application.</span></span> <span data-ttu-id="18154-119">Ce mode est principalement utilisé par les applications qui souhaitent disposer d’un contrôle direct temporaire sur les modems asynchrones, accessibles via les [fonctions de communication](/windows/desktop/DevIO/communications-functions), afin de configurer ou d’utiliser des fonctionnalités spéciales non prises en charge par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="18154-119">This mode is used primarily by applications desiring temporary direct control over asynchronous modems, accessed through the [communications functions](/windows/desktop/DevIO/communications-functions), for the purpose of configuring or using special features not otherwise supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18154-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**</span><span class="sxs-lookup"><span data-stu-id="18154-120"><span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE\_RESTRICTEDDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18154-121">Service porteur pour les données numériques dans laquelle seuls les sept bits de poids faible de chaque octet peuvent contenir des données utilisateur (par exemple, pour un service 56Kbit/s commuté).</span><span class="sxs-lookup"><span data-stu-id="18154-121">Bearer service for digital data in which only the low-order seven bits of each octet may contain user data (for example, for Switched 56kbit/s service).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18154-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**\_parole LINEBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="18154-122"><span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE\_SPEECH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18154-123">Cela correspond à la transmission de la parole G. 711 sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="18154-123">This corresponds to G.711 speech transmission on the call.</span></span> <span data-ttu-id="18154-124">Le réseau peut utiliser des techniques de traitement telles que la transmission analogique, l’annulation de l’écho et la compression/décompression.</span><span class="sxs-lookup"><span data-stu-id="18154-124">The network can use processing techniques such as analog transmission, echo cancellation, and compression/decompression.</span></span> <span data-ttu-id="18154-125">L’intégrité des bits n’est pas assurée.</span><span class="sxs-lookup"><span data-stu-id="18154-125">Bit integrity is not assured.</span></span> <span data-ttu-id="18154-126">La reconnaissance vocale n’est pas destinée à prendre en charge les types de média Fax et modem.</span><span class="sxs-lookup"><span data-stu-id="18154-126">Speech is not intended to support fax and modem media types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18154-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**\_voix LINEBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="18154-127"><span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="18154-128">Il s’agit d’un service de support analogique de niveau vocal 3,1 kHz standard.</span><span class="sxs-lookup"><span data-stu-id="18154-128">This is a regular 3.1 kHz analog voice-grade bearer service.</span></span> <span data-ttu-id="18154-129">L’intégrité des bits n’est pas assurée.</span><span class="sxs-lookup"><span data-stu-id="18154-129">Bit integrity is not assured.</span></span> <span data-ttu-id="18154-130">Voice peut prendre en charge les types de média Fax et modem.</span><span class="sxs-lookup"><span data-stu-id="18154-130">Voice can support fax and modem media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18154-131">Notes</span><span class="sxs-lookup"><span data-stu-id="18154-131">Remarks</span></span>

<span data-ttu-id="18154-132">Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18154-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="18154-133">Les 16 bits de poids faible sont réservés.</span><span class="sxs-lookup"><span data-stu-id="18154-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="18154-134">Notez que le mode porteur et le type de média sont des notions différentes.</span><span class="sxs-lookup"><span data-stu-id="18154-134">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="18154-135">Le mode de support d’un appel est une indication de la qualité de la connexion téléphonique, comme fourni principalement par le réseau.</span><span class="sxs-lookup"><span data-stu-id="18154-135">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="18154-136">Le type de média d’un appel est une indication du type de flux d’informations échangé sur cet appel.</span><span class="sxs-lookup"><span data-stu-id="18154-136">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="18154-137">Le modem de télécopie ou de données de groupe 3 est un type de support qui utilise un appel avec un mode de support vocal 3,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="18154-137">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="18154-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18154-138">Requirements</span></span>



| <span data-ttu-id="18154-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18154-139">Requirement</span></span> | <span data-ttu-id="18154-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="18154-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="18154-141">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="18154-141">TAPI version</span></span><br/> | <span data-ttu-id="18154-142">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="18154-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="18154-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="18154-143">Header</span></span><br/>       | <dl> <span data-ttu-id="18154-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="18154-144"><dt>Tapi.h</dt></span></span> </dl> |



 

