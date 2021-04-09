---
description: Crée un objet de contexte qui décrit le périphérique tablette spécifié.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: 'ITablet :: CreateContext, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868285"
---
# <a name="itabletcreatecontext-method"></a><span data-ttu-id="7a80f-103">ITablet :: CreateContext, méthode</span><span class="sxs-lookup"><span data-stu-id="7a80f-103">ITablet::CreateContext method</span></span>

<span data-ttu-id="7a80f-104">Crée un objet de contexte qui décrit le périphérique tablette spécifié.</span><span class="sxs-lookup"><span data-stu-id="7a80f-104">Creates a context object that describes the specified tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a80f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a80f-105">Syntax</span></span>


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="7a80f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a80f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a80f-107">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a80f-108">Fenêtre à laquelle le contexte de tablette sera attaché.</span><span class="sxs-lookup"><span data-stu-id="7a80f-108">The window to which the tablet context will be attached.</span></span>

</dd> <dt>

<span data-ttu-id="7a80f-109">*prcInput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-109">*prcInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a80f-110">\[dans, unique\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-110">\[in, unique\]</span></span>

<span data-ttu-id="7a80f-111">Rectangle de saisie d’encre.</span><span class="sxs-lookup"><span data-stu-id="7a80f-111">The ink input rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="7a80f-112">*dwOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-112">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a80f-113">Indicateurs qui définissent des options de contexte de tablette.</span><span class="sxs-lookup"><span data-stu-id="7a80f-113">Flags that set tablet context options.</span></span>

</dd> <dt>

<span data-ttu-id="7a80f-114">*pTCS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-114">*pTCS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a80f-115">\[dans, unique\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-115">\[in, unique\]</span></span>

<span data-ttu-id="7a80f-116">Informations détaillées sur le contexte de tablette à créer.</span><span class="sxs-lookup"><span data-stu-id="7a80f-116">Detailed information about the tablet context to create.</span></span>

</dd> <dt>

<span data-ttu-id="7a80f-117">*cet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-117">*cet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a80f-118">Valeur qui active ou désactive les messages de contexte envoyés à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7a80f-118">Value that enables or disables context messages being sent to the window.</span></span>

</dd> <dt>

<span data-ttu-id="7a80f-119">*ppCtx* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-119">*ppCtx* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a80f-120">Pointeur vers le contexte de tablette nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="7a80f-120">A pointer to the newly create tablet context.</span></span>

</dd> <dt>

<span data-ttu-id="7a80f-121">*pTcid* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-121">*pTcid* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a80f-122">Valeur qui identifie de façon unique la tablette.</span><span class="sxs-lookup"><span data-stu-id="7a80f-122">Value that uniquely identifies the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="7a80f-123">*ppPD* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-123">*ppPD* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a80f-124">Pointeur vers des informations sur les données contenues dans chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="7a80f-124">Pointer to information about what data is contained in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="7a80f-125">*pSink* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-125">*pSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a80f-126">Objet [**ITabletEventSink**](itableteventsink.md) dans lequel les messages de notification seront envoyés.</span><span class="sxs-lookup"><span data-stu-id="7a80f-126">The [**ITabletEventSink**](itableteventsink.md) object where notification messages will be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a80f-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a80f-127">Return value</span></span>

<span data-ttu-id="7a80f-128">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="7a80f-128">This method can return one of these values.</span></span>



| <span data-ttu-id="7a80f-129">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7a80f-129">Return code</span></span>                                                                            | <span data-ttu-id="7a80f-130">Description</span><span class="sxs-lookup"><span data-stu-id="7a80f-130">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="7a80f-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a80f-131"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7a80f-132">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="7a80f-132">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="7a80f-133"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="7a80f-133"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7a80f-134">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="7a80f-134">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a80f-135">Notes</span><span class="sxs-lookup"><span data-stu-id="7a80f-135">Remarks</span></span>

<span data-ttu-id="7a80f-136">En règle générale, une application obtient les valeurs par défaut à partir de la [**méthode ITablet :: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifie les valeurs en fonction de leurs besoins, puis passe la structure des paramètres modifiés à la **méthode ITablet :: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="7a80f-136">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the **ITablet::CreateContext Method**.</span></span>

> [!Note]  
> <span data-ttu-id="7a80f-137">Vous devez implémenter l' [**interface ITabletEventSink**](itableteventsink.md) lors de l’appel de la **méthode ITablet :: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="7a80f-137">You must implement the [**ITabletEventSink Interface**](itableteventsink.md) when calling the **ITablet::CreateContext Method**.</span></span>

 

<span data-ttu-id="7a80f-138">Le paramètre *dwOptions* est un jeu d’indicateurs binaires qui décrivent les options de contexte.</span><span class="sxs-lookup"><span data-stu-id="7a80f-138">The *dwOptions* parameter is a set of bit flags that describe context options.</span></span> <span data-ttu-id="7a80f-139">Le tableau suivant décrit ces indicateurs.</span><span class="sxs-lookup"><span data-stu-id="7a80f-139">The following table describes these flags.</span></span>



| <span data-ttu-id="7a80f-140">Nom de l’indicateur</span><span class="sxs-lookup"><span data-stu-id="7a80f-140">Flag Name</span></span>                                | <span data-ttu-id="7a80f-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a80f-141">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="7a80f-142">Description</span><span class="sxs-lookup"><span data-stu-id="7a80f-142">Description</span></span>                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a80f-143">\_marge TCXO</span><span class="sxs-lookup"><span data-stu-id="7a80f-143">TCXO\_MARGIN</span></span><br/>                  | <span data-ttu-id="7a80f-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7a80f-144">0x00000001</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="7a80f-145">Spécifie que le contexte d’entrée sur la tablette aura une marge.</span><span class="sxs-lookup"><span data-stu-id="7a80f-145">Specifies that the input context on the tablet will have a margin.</span></span> <span data-ttu-id="7a80f-146">La marge est une zone située en dehors de la zone d’entrée spécifiée où les événements sont mappés sur le bord de la zone d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7a80f-146">The margin is an area outside the specified input area where events will be mapped to the edge of the input area.</span></span> <span data-ttu-id="7a80f-147">Cette fonctionnalité facilite l’entrée des points à la périphérie du contexte.</span><span class="sxs-lookup"><span data-stu-id="7a80f-147">This feature makes it easier to input points at the edge of the context.</span></span><br/> |
| <span data-ttu-id="7a80f-148">préhook TCXO \_</span><span class="sxs-lookup"><span data-stu-id="7a80f-148">TCXO\_PREHOOK</span></span><br/>                 | <span data-ttu-id="7a80f-149">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7a80f-149">0x00000002</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="7a80f-150">Le préhook obtient les paquets avant les contextes standard et les posthooks.</span><span class="sxs-lookup"><span data-stu-id="7a80f-150">Prehook gets packets before regular contexts and posthooks.</span></span> <span data-ttu-id="7a80f-151">Ils obtiennent des paquets dans l’ordre de leur création.</span><span class="sxs-lookup"><span data-stu-id="7a80f-151">They get packets in the order of their creation.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="7a80f-152">\_État du curseur TCXO \_</span><span class="sxs-lookup"><span data-stu-id="7a80f-152">TCXO\_CURSOR\_STATE</span></span><br/>           | <span data-ttu-id="7a80f-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7a80f-153">0x00000004</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="7a80f-154">Le TC renverra des paquets même si le curseur est en place.</span><span class="sxs-lookup"><span data-stu-id="7a80f-154">The TC will return packets even if the cursor is up.</span></span> <span data-ttu-id="7a80f-155">Par défaut, TC retourne des paquets uniquement lorsque le curseur est en aval.</span><span class="sxs-lookup"><span data-stu-id="7a80f-155">By default, a TC will only return packets when the cursor is down.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="7a80f-156">TCXO \_ aucun \_ curseur en \_ dessous</span><span class="sxs-lookup"><span data-stu-id="7a80f-156">TCXO\_NO\_CURSOR\_DOWN</span></span><br/>        | <span data-ttu-id="7a80f-157">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7a80f-157">0x00000008</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="7a80f-158">Le TC ne retourne pas de paquets lorsque le curseur est en aval.</span><span class="sxs-lookup"><span data-stu-id="7a80f-158">The TC will not return packets when the cursor is down.</span></span><br/>                                                                                                                                                                                                       |
| <span data-ttu-id="7a80f-159">TCXO \_ non \_ intégré</span><span class="sxs-lookup"><span data-stu-id="7a80f-159">TCXO\_NON\_INTEGRATED</span></span><br/>         | <span data-ttu-id="7a80f-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a80f-160">0x00000010</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="7a80f-161">Le contexte ne sera pas intégré.</span><span class="sxs-lookup"><span data-stu-id="7a80f-161">The context will be non-integrated.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="7a80f-162">TCXO \_ POSTHOOK</span><span class="sxs-lookup"><span data-stu-id="7a80f-162">TCXO\_POSTHOOK</span></span><br/>                | <span data-ttu-id="7a80f-163">0x00000020</span><span class="sxs-lookup"><span data-stu-id="7a80f-163">0x00000020</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="7a80f-164">Posthooks obtient des paquets après des contextes de tablette normaux mais avant le contexte système.</span><span class="sxs-lookup"><span data-stu-id="7a80f-164">Posthooks get packets after regular tablet contexts but before the system context.</span></span> <span data-ttu-id="7a80f-165">Ils obtiennent des paquets dans l’ordre inverse de leur création.</span><span class="sxs-lookup"><span data-stu-id="7a80f-165">They get packets in the reverse order of their creation.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="7a80f-166">TCXO ne pas \_ \_ afficher le \_ curseur</span><span class="sxs-lookup"><span data-stu-id="7a80f-166">TCXO\_DONT\_SHOW\_CURSOR</span></span><br/>      | <span data-ttu-id="7a80f-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="7a80f-167">0x00000080</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="7a80f-168">Le TC ne définit pas la position du curseur.</span><span class="sxs-lookup"><span data-stu-id="7a80f-168">The TC will not set the cursor position.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="7a80f-169">TCXO ne pas \_ \_ valider les \_ TCS</span><span class="sxs-lookup"><span data-stu-id="7a80f-169">TCXO\_DONT\_VALIDATE\_TCS</span></span><br/>     | <span data-ttu-id="7a80f-170">0x00000100</span><span class="sxs-lookup"><span data-stu-id="7a80f-170">0x00000100</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="7a80f-171">TC ne valide pas les GUID transmis dans les paramètres de contexte de tablette par rapport aux propriétés prises en charge de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7a80f-171">The TC will not validate the GUIDS passed in the tablet context settings against the supported properties of the device.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="7a80f-172">TCXO \_ autoriser les \_ raccourcis</span><span class="sxs-lookup"><span data-stu-id="7a80f-172">TCXO\_ALLOW\_FLICKS</span></span><br/>           | <span data-ttu-id="7a80f-173">0x00000400</span><span class="sxs-lookup"><span data-stu-id="7a80f-173">0x00000400</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="7a80f-174">Le TC autorisera la détection de mouvement (par défaut, cette opération est autorisée uniquement dans les contextes système) et le client obtiendra les \_ événements de scintillement se.</span><span class="sxs-lookup"><span data-stu-id="7a80f-174">The TC will allow flick detection to take place (by default this is only allowed on system contexts), and the client will get SE\_FLICK events.</span></span><br/>                                                                                                               |
| <span data-ttu-id="7a80f-175">TCXO \_ autoriser \_ les \_ clics de commentaires</span><span class="sxs-lookup"><span data-stu-id="7a80f-175">TCXO\_ALLOW\_FEEDBACK\_TAPS</span></span><br/>   | <span data-ttu-id="7a80f-176">0x00000800</span><span class="sxs-lookup"><span data-stu-id="7a80f-176">0x00000800</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="7a80f-177">Le TC permettra d’afficher les commentaires du stylet.</span><span class="sxs-lookup"><span data-stu-id="7a80f-177">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="7a80f-178">Par défaut, cette valeur est autorisée uniquement dans les contextes système.</span><span class="sxs-lookup"><span data-stu-id="7a80f-178">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="7a80f-179">TCXO \_ autoriser les \_ Commentaires \_ Barrel</span><span class="sxs-lookup"><span data-stu-id="7a80f-179">TCXO\_ALLOW\_FEEDBACK\_BARREL</span></span><br/> | <span data-ttu-id="7a80f-180">0x00001000</span><span class="sxs-lookup"><span data-stu-id="7a80f-180">0x00001000</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="7a80f-181">Le TC permettra d’afficher les commentaires du stylet.</span><span class="sxs-lookup"><span data-stu-id="7a80f-181">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="7a80f-182">Par défaut, cette valeur est autorisée uniquement dans les contextes système.</span><span class="sxs-lookup"><span data-stu-id="7a80f-182">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="7a80f-183">TCXO \_ tout</span><span class="sxs-lookup"><span data-stu-id="7a80f-183">TCXO\_ALL</span></span><br/>                     | <span data-ttu-id="7a80f-184">TCXO \_ Margin \| TCXO \_ préhook \| TCXO \_ État du curseur \_ \| TCXO \_ aucun \_ curseur vers le faible TCXO non intégré TCXO POSTHOOK TCXO ne pas \_ \| \_ afficher le \_ \| \_ \| \_ \_ \_ curseur \| TCXO \_ \_ \_ ne pas valider les TCS</span><span class="sxs-lookup"><span data-stu-id="7a80f-184">TCXO\_MARGIN \| TCXO\_PREHOOK \| TCXO\_CURSOR\_STATE \| TCXO\_NO\_CURSOR\_DOWN \| TCXO\_NON\_INTEGRATED \| TCXO\_POSTHOOK \| TCXO\_DONT\_SHOW\_CURSOR \| TCXO\_DONT\_VALIDATE\_TCS</span></span><br/> | <span data-ttu-id="7a80f-185">Toutes les options de contexte de tablette définies.</span><span class="sxs-lookup"><span data-stu-id="7a80f-185">All defined tablet context options.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="7a80f-186">\_Hook TCXO</span><span class="sxs-lookup"><span data-stu-id="7a80f-186">TCXO\_HOOK</span></span><br/>                    | <span data-ttu-id="7a80f-187">TCXO \_ prehook \| TCXO \_ POSTHOOK</span><span class="sxs-lookup"><span data-stu-id="7a80f-187">TCXO\_PREHOOK \| TCXO\_POSTHOOK</span></span><br/>                                                                                                                                                    | <span data-ttu-id="7a80f-188">Combine les fonctionnalités de pré-Hook et de postconnexion.</span><span class="sxs-lookup"><span data-stu-id="7a80f-188">Combines pre-hook and post-hook functionality.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="7a80f-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a80f-189">Requirements</span></span>



| <span data-ttu-id="7a80f-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a80f-190">Requirement</span></span> | <span data-ttu-id="7a80f-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a80f-191">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a80f-192">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a80f-192">Minimum supported client</span></span><br/> | <span data-ttu-id="7a80f-193">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a80f-193">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7a80f-194">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a80f-194">Minimum supported server</span></span><br/> | <span data-ttu-id="7a80f-195">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a80f-195">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7a80f-196">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7a80f-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a80f-197"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7a80f-197"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a80f-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a80f-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a80f-199">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="7a80f-199">**ITablet Interface**</span></span>](itablet.md)
</dt> <dt>

[<span data-ttu-id="7a80f-200">**\_Énumération des types d’activation de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="7a80f-200">**CONTEXT\_ENABLE\_TYPE Enumeration**</span></span>](context-enable-type.md)
</dt> <dt>

[<span data-ttu-id="7a80f-201">**Structure des paramètres de \_ contexte de tablette \_**</span><span class="sxs-lookup"><span data-stu-id="7a80f-201">**TABLET\_CONTEXT\_SETTINGS Structure**</span></span>](tablet-context-settings.md)
</dt> <dt>

[<span data-ttu-id="7a80f-202">**Structure de la description du paquet \_**</span><span class="sxs-lookup"><span data-stu-id="7a80f-202">**PACKET\_DESCRIPTION Structure**</span></span>](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[<span data-ttu-id="7a80f-203">**Interface ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="7a80f-203">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="7a80f-204">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="7a80f-204">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




