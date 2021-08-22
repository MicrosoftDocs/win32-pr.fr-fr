---
description: Les \_ constantes dxgi présentes spécifient des options pour la présentation des frames à la sortie.
ms.assetid: 1ddf8643-ea3e-4c9f-8439-c245942f7333
title: DXGI_PRESENT (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84ce79d686aebd77e24a5be6facccd6fa4abd48e10bf15c07729a8ff6a0397bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796603"
---
# <a name="dxgi_present"></a>DXGI \_ présente

Les constantes **dxgi \_ présentes** spécifient des options pour la présentation des frames à la sortie.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valeur</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span></span><dl> <dt><strong></strong></dt><dt>0</dt> </dl></td>
<td style="text-align: left;">Présente un frame à partir de chaque mémoire tampon (à partir de la mémoire tampon actuelle) vers la sortie.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_SEQUENCE"></span><span id="dxgi_present_do_not_sequence"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt> <dt>0x00000002UL</dt> </dl></td>
<td style="text-align: left;">Présente un frame de la mémoire tampon actuelle à la sortie. Utilisez cet indicateur pour que la présentation puisse utiliser la synchronisation à blanc vertical au lieu de séquencer des mémoires tampons dans la chaîne de manière habituelle.<br/>
<blockquote>
[!Note]<br />
Si l’application appelante définit la constante DXGI_PRESENT_DO_NOT_SEQUENCE sur la première opération présente (autrement dit, en l’absence de mémoire tampon actuelle), le runtime ignore cette opération présente et n’appelle pas le pilote.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_TEST"></span><span id="dxgi_present_test"></span><dl> <dt><strong>DXGI_PRESENT_TEST</strong></dt> <dt>0x00000001UL</dt> </dl></td>
<td style="text-align: left;">Ne présentez pas le frame à la sortie. L’état de la chaîne de permutation sera testé et les erreurs appropriées seront retournées. DXGI_PRESENT_TEST est destiné à être utilisé uniquement lors du passage à l’état inactif ; ne l’utilisez pas pour déterminer quand basculer vers l’état inactif, car cela peut permettre à la chaîne de permutation de quitter le mode plein écran.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTART"></span><span id="dxgi_present_restart"></span><dl> <dt><strong>DXGI_PRESENT_RESTART</strong></dt> <dt>0x00000004UL</dt> </dl></td>
<td style="text-align: left;">Spécifie que le runtime ignorera les cadeaux en attente en attente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_WAIT"></span><span id="dxgi_present_do_not_wait"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt> <dt>0x00000008UL</dt> </dl></td>
<td style="text-align: left;">Spécifie que le runtime ne fera pas échouer la présentation (autrement dit, un appel à <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1 ::P resent1</strong></a>) avec le code d’erreur <a href="dxgi-error.md">DXGI_ERROR_WAS_STILL_DRAWING</a> si le thread appelant est bloqué ; le runtime retourne DXGI_ERROR_WAS_STILL_DRAWING au lieu de se mettre en veille jusqu’à ce que la dépendance soit résolue.<br/> <strong>Direct3D 11 :</strong> Cette valeur d’énumération est prise en charge à partir de Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTRICT_TO_OUTPUT"></span><span id="dxgi_present_restrict_to_output"></span><dl> <dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt> <dt>0x00000010UL</dt> </dl></td>
<td style="text-align: left;">Indique que le contenu de la présentation s’affichera uniquement sur la sortie particulière. Le contenu n’est pas visible sur les autres sorties. Par exemple, si l’utilisateur tente de déplacer le contenu vidéo sur une autre sortie, le contenu vidéo n’est pas visible. <br/> <strong>Direct3D 11 :</strong> Cette valeur d’énumération est prise en charge à partir de Windows 8. <br/>
<blockquote>
[!Note]<br />
Cet indicateur doit être utilisé uniquement avec l’effet d’échange <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> ou DXGI_SWAP_EFFECT_FLIP_DISCARD. L’utilisation de cet indicateur avec d' <em>autres</em> effets d’échange est dépréciée et risque de ne pas fonctionner dans les futures versions de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_PREFER_RIGHT"></span><span id="dxgi_present_stereo_prefer_right"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt> <dt>0x00000020UL</dt> </dl></td>
<td style="text-align: left;">Indique que si la stéréo présente doit être réduite en mono, l’affichage à droite est utilisé au lieu de l’affichage de l’œil gauche.<br/> <strong>Direct3D 11 :</strong> Cette valeur d’énumération est prise en charge à partir de Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_TEMPORARY_MONO"></span><span id="dxgi_present_stereo_temporary_mono"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt> <dt>0x00000040UL</dt> </dl></td>
<td style="text-align: left;">Indique que la présentation doit utiliser la mémoire tampon de gauche comme une mémoire tampon mono. Une application appelle la méthode <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>IDXGISwapChain1 :: IsTemporaryMonoSupported</strong></a> pour déterminer si une chaîne de permutation prend en charge les &quot; mono temporaires &quot; .<br/> <strong>Direct3D 11 :</strong> Cette valeur d’énumération est prise en charge à partir de Windows 8.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_USE_DURATION"></span><span id="dxgi_present_use_duration"></span><dl> <dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt> <dt>0x00000100UL</dt> </dl></td>
<td style="text-align: left;">Cet indicateur doit être défini par les applications multimédias qui utilisent actuellement une durée actuelle personnalisée (fréquence de rafraîchissement personnalisée). Consultez <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>IDXGISwapChainMedia</strong></a>.<br/>
<blockquote>
[!Note]<br />
Cette valeur est prise en charge à partir de Windows 8.1.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_ALLOW_TEARING"></span><span id="dxgi_present_allow_tearing"></span><dl> <dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt> <dt>0x00000200UL</dt> </dl></td>
<td style="text-align: left;">L’autorisation du déchirement est une exigence de la fréquence d’actualisation des variables.<br/> Les conditions d’utilisation de DXGI_PRESENT_ALLOW_TEARINGs sont les suivantes :<br/>
<ul>
<li>La chaîne de permutation doit être créée avec l’indicateur <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</strong></a> .</li>
<li>L’intervalle de synchronisation passé à <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>présent</strong></a> (ou <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) doit être égal à 0.</li>
<li>L’indicateur DXGI_PRESENT_ALLOW_TEARING ne peut pas être utilisé dans une application actuellement en mode exclusif plein écran (définie par l’appel de <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>SetFullscreenState (true)</strong></a>). Il ne peut être utilisé qu’en mode fenêtre. Pour utiliser cet indicateur dans les applications Win32 en mode plein écran, l’application doit être présente dans une fenêtre sans bordure plein écran et désactiver le basculement automatique ALT + entrée à l’aide de <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>IDXGIFactory :: MakeWindowAssociation</strong></a>. Les applications UWP qui entrent en mode plein écran en appelant <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> sont des fenêtres sans bordure plein écran et peuvent utiliser l’indicateur.</li>
</ul>
L’appel de <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>present</strong></a> (ou <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) avec cet indicateur et ne répondant pas aux conditions ci-dessus entraîne le renvoi d’une erreur DXGI_ERROR_INVALID_CALL à l’application appelante.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Remarques

Les options de présentation sont fournies lors de l’appel de [**IDXGISwapChain ::P renvoyé**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) ou [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . Les mémoires tampons sont spécifiées dans la description de la chaîne de permutation (consultez la chaîne de permutation [**dxgi \_ \_ \_ desc**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) ou [**dxgi \_ swap \_ chain \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)).

Le \_ \_ redémarrage de la dxgi présente est valide uniquement pour les chaînes de permutation du modèle et en mode plein écran. Les applications peuvent utiliser \_ le \_ redémarrage de DXGI pour récupérer des erreurs en cours de lecture, ainsi que pour ignorer les présentations précédemment mises en file d’attente. L’abandon des présentations précédemment mises en file d’attente est utile si ces présentations en file d’attente sont des scénarios de fenêtrage. En particulier, la présentation précédemment mise en file d’attente peut supposer que la fenêtre est d’une ancienne taille (autrement dit, une opération de redimensionnement s’est produite après l’envoi).

DXGI \_ présente \_ \_ la restriction à \_ la sortie est valide uniquement pour les chaînes de permutation qui ont spécifié une sortie particulière pour restreindre le contenu quand ces chaînes de permutation ont été créées ([**IDXGIFactory2 :: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)). S’il n’existe aucune sortie à limiter, l’indicateur n’est pas valide.

DXGI \_ présent \_ stéréo \_ préférer \_ à droite indique que si la stéréo présente doit être réduite en mono, l’œil droit doit être utilisé à la place de l’oeil gauche (par défaut). Vous pouvez utiliser cet indicateur si la qualité d’un côté est supérieure (par exemple, si la paire stéréo est synthétisée à partir d’une image standard).

DXGI \_ présent \_ mono stéréo stéréo \_ \_ indique que le présent doit utiliser la mémoire tampon gauche comme mémoire tampon mono. Vous pouvez utiliser cet indicateur pour éviter de mettre à jour la mémoire tampon appropriée lorsqu’une application n’a pas de contenu stéréo de manière temporaire. Vous devez utiliser cet indicateur chaque fois que cela est possible, car il permet une optimisation significative par le système d’exploitation et, dans certains cas, il peut éviter les artefacts de modification du mode visible.

Pour la plupart des applications, vous devez utiliser l' \_ \_ \_ indicateur mono stéréo temporaire dxgi présent \_ de préférence pour basculer vers une chaîne de permutation mono pour la plupart des applications que vous prévoyez de réutiliser le stéréo. Vous devez équilibrer l’utilisation de cet indicateur dans les applications qui sont extrêmement longues ou qui affichent rarement de la stéréo contre l’inconvénient de la mémoire inutilisée.

> [!Note]  
> Les applications plein écran qui basculent vers une chaîne d’échange mono provoquent une modification du mode qui a généralement des artefacts visibles (par exemple, « clignotant »). Toutefois, les chaînes mono temporaires peuvent ne pas être prises en charge pour les chaînes d’échange plein écran.

 

La DXGI \_ présente une \_ stéréo \_ préférée \_ et dxgi \_ présente \_ les \_ indicateurs mono stéréo stéréo \_ s’applique uniquement aux chaînes de permutation stéréo. Si vous les utilisez lorsque vous présentez des chaînes d’échange mono, une opération non valide se produit.

Si vous utilisez l' \_ \_ \_ indicateur mono stéréo temporaire dxgi présent \_ lorsque vous présentez une chaîne de permutation stéréo qui ne prend pas en charge les mono temporaires, une erreur se produit, la chaîne de permutation ne s’affiche pas et la présentation retourne l' [ \_ \_ \_ appel non valide de l’erreur dxgi](dxgi-error.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
