---
description: Les \_ \_ constantes AUDCLNT SESSIONFLAGS xxx indiquent les caractéristiques d’une session audio associée au flux.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: Constantes AUDCLNT_SESSIONFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483921"
---
# <a name="audclnt_sessionflags_xxx-constants"></a><span data-ttu-id="70491-103">AUDCLNT \_ SESSIONFLAGS \_ xxx, constantes</span><span class="sxs-lookup"><span data-stu-id="70491-103">AUDCLNT\_SESSIONFLAGS\_XXX Constants</span></span>

<span data-ttu-id="70491-104">Les \_ \_ constantes AUDCLNT SESSIONFLAGS xxx indiquent les caractéristiques d’une session audio associée au flux.</span><span class="sxs-lookup"><span data-stu-id="70491-104">The AUDCLNT\_SESSIONFLAGS\_XXX constants indicate characteristics of an audio session associated with the stream.</span></span> <span data-ttu-id="70491-105">Un client peut spécifier ces options lors de l’initialisation du flux par le biais du paramètre *StreamFlags* de la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="70491-105">A client can specify these options during the initialization of the stream by through the *StreamFlags* parameter of the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span>



| <span data-ttu-id="70491-106">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="70491-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="70491-107">Description</span><span class="sxs-lookup"><span data-stu-id="70491-107">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <span data-ttu-id="70491-108"><dt>**AUDCLNT \_ SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="70491-108"><dt>**AUDCLNT\_SESSIONFLAGS\_EXPIREWHENUNOWNED**</dt> <dt>0x10000000 </dt></span></span> </dl>                       | <span data-ttu-id="70491-109">La session expire lorsqu’il n’y a aucun flux associé et que les objets de contrôle de session propriétaire contiennent des références.</span><span class="sxs-lookup"><span data-stu-id="70491-109">The session expires when there are no associated streams and owning session control objects holding references.</span></span><br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <span data-ttu-id="70491-110"><dt>**AUDCLNT \_ \_Affichage SESSIONFLAGS \_ Masquer**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="70491-110"><dt>**AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDE**</dt> <dt>0x20000000 </dt></span></span> </dl>                                     | <span data-ttu-id="70491-111">Le contrôle du volume est masqué dans l’interface utilisateur du mélangeur de volume lors de la création de la session audio.</span><span class="sxs-lookup"><span data-stu-id="70491-111">The volume control is hidden in the volume mixer user interface when the audio session is created.</span></span> <span data-ttu-id="70491-112">Si la session associée au flux existe déjà avant que [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) ouvre le flux, le contrôle du volume est affiché dans le mélangeur de volume.</span><span class="sxs-lookup"><span data-stu-id="70491-112">If the session associated with the stream already exists before [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) opens the stream, the volume control is displayed in the volume mixer.</span></span><br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <span data-ttu-id="70491-113"><dt> **AUDCLNT \_ SESSIONFLAGS \_ Display \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="70491-113"><dt> **AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDEWHENEXPIRED**</dt> <dt>0x40000000 </dt></span></span> </dl> | <span data-ttu-id="70491-114">Le contrôle du volume est masqué dans l’interface utilisateur du mélangeur de volume après l’expiration de la session.</span><span class="sxs-lookup"><span data-stu-id="70491-114">The volume control is hidden in the volume mixer user interface after the session expires.</span></span> <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="70491-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70491-115">Requirements</span></span>



| <span data-ttu-id="70491-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70491-116">Requirement</span></span> | <span data-ttu-id="70491-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="70491-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70491-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70491-118">Minimum supported client</span></span><br/> | <span data-ttu-id="70491-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70491-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="70491-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70491-120">Minimum supported server</span></span><br/> | <span data-ttu-id="70491-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70491-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="70491-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="70491-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="70491-123"><dt>Audiosessiontypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="70491-123"><dt>Audiosessiontypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70491-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70491-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70491-125">Constantes audio principales</span><span class="sxs-lookup"><span data-stu-id="70491-125">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="70491-126">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="70491-126">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




