---
description: Codes d’erreur spécifiques à XAudio2 retournés par les méthodes XAudio2.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: Codes d’erreur XAudio2 (Xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7011786c3db7f660dee7a3323861abd88c57835
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528978"
---
# <a name="xaudio2-error-codes"></a><span data-ttu-id="e2b04-103">Codes d’erreur XAudio2</span><span class="sxs-lookup"><span data-stu-id="e2b04-103">XAudio2 Error Codes</span></span>

<span data-ttu-id="e2b04-104">Codes d’erreur spécifiques à XAudio2 retournés par les méthodes XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e2b04-104">XAudio2 specific error codes returned by XAudio2 methods.</span></span>



| <span data-ttu-id="e2b04-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="e2b04-105">Constant/value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="e2b04-106">Description</span><span class="sxs-lookup"><span data-stu-id="e2b04-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <span data-ttu-id="e2b04-107"><dt>**XAUDIO2 \_ E 0x88960001 d' \_ \_ appel non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e2b04-107"><dt>**XAUDIO2\_E\_INVALID\_CALL**</dt> <dt>0x88960001</dt></span></span> </dl>                          | <span data-ttu-id="e2b04-108">Retourné par XAudio2 pour certaines erreurs d’utilisation de l’API (appels non valides, etc.) qui sont difficiles à éviter complètement et doivent être gérées par un titre au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e2b04-108">Returned by XAudio2 for certain API usage errors (invalid calls and so on) that are hard to avoid completely and should be handled by a title at runtime.</span></span> <span data-ttu-id="e2b04-109">(Les erreurs d’utilisation d’API qui sont entièrement évitables, telles que les paramètres non valides, provoquent une assertion dans les versions Debug et le comportement non défini dans les versions commerciales, de sorte qu’aucun code d’erreur n’est défini pour eux.)</span><span class="sxs-lookup"><span data-stu-id="e2b04-109">(API usage errors that are completely avoidable, such as invalid parameters, cause an ASSERT in debug builds and undefined behavior in retail builds, so no error code is defined for them.)</span></span><br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <span data-ttu-id="e2b04-110"><dt>**XAUDIO2 \_ \_Erreur du \_ décodeur \_ E XMA**</dt> <dt>0x88960002</dt></span><span class="sxs-lookup"><span data-stu-id="e2b04-110"><dt>**XAUDIO2\_E\_XMA\_DECODER\_ERROR**</dt> <dt>0x88960002</dt></span></span> </dl>          | <span data-ttu-id="e2b04-111">Le matériel Xbox 360 XMA a subi une erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="e2b04-111">The Xbox 360 XMA hardware suffered an unrecoverable error.</span></span><br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <span data-ttu-id="e2b04-112"><dt>**XAUDIO2 \_ \_ \_ \_ Échec**</dt> de la création de XAPO <dt>0x88960003</dt></span><span class="sxs-lookup"><span data-stu-id="e2b04-112"><dt>**XAUDIO2\_E\_XAPO\_CREATION\_FAILED**</dt> <dt>0x88960003</dt></span></span> </dl> | <span data-ttu-id="e2b04-113">Échec de l’instanciation d’un effet.</span><span class="sxs-lookup"><span data-stu-id="e2b04-113">An effect failed to instantiate.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <span data-ttu-id="e2b04-114"><dt>**XAUDIO2 \_ 0x88960004 de l' \_ appareil \_ invalidée**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e2b04-114"><dt>**XAUDIO2\_E\_DEVICE\_INVALIDATED**</dt> <dt>0x88960004</dt></span></span> </dl>        | <span data-ttu-id="e2b04-115">Un périphérique audio est devenu inutilisable par le biais d’un débranchement ou d’un autre événement.</span><span class="sxs-lookup"><span data-stu-id="e2b04-115">An audio device became unusable through being unplugged or some other event.</span></span><br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="e2b04-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e2b04-116">Remarks</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="e2b04-117">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="e2b04-117">Platform Requirements</span></span>

<span data-ttu-id="e2b04-118">Windows 10 (XAudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); SDK DirectX (XAudio 2,7)</span><span class="sxs-lookup"><span data-stu-id="e2b04-118">Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b04-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2b04-119">Requirements</span></span>



| <span data-ttu-id="e2b04-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2b04-120">Requirement</span></span> | <span data-ttu-id="e2b04-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2b04-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b04-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2b04-122">Header</span></span><br/> | <dl> <span data-ttu-id="e2b04-123"><dt>Xaudio2. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2b04-123"><dt>Xaudio2.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b04-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2b04-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b04-125">XAudio2 :: constants</span><span class="sxs-lookup"><span data-stu-id="e2b04-125">XAudio2::Constants</span></span>](constants.md)
</dt> </dl>

 

 




