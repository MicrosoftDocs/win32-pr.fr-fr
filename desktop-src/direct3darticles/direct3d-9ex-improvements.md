---
title: Améliorations de Direct3D 9Ex
description: cette rubrique décrit la prise en charge ajoutée de Windows 7 pour le Mode de basculement présent et les statistiques actuelles associées dans Direct3D 9ex et Gestionnaire de fenêtrage.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3221b805f07408b27e19a00a42ca0c4733ea725bd32a51b5b3e340b48d2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796991"
---
# <a name="direct3d-9ex-improvements"></a>Améliorations de Direct3D 9Ex

cette rubrique décrit la prise en charge ajoutée de Windows 7 pour le Mode de basculement présent et les statistiques actuelles associées dans Direct3D 9ex et Gestionnaire de fenêtrage. Les applications cibles incluent des vidéos ou des applications de présentation basées sur la fréquence des images. Les applications qui utilisent le mode de basculement Direct3D 9Ex présentent réduisent la charge des ressources système lorsque DWM est activé. La présentation des améliorations des statistiques associées au mode de basculement présente permet aux applications Direct3D 9Ex de mieux contrôler le taux de présentation en fournissant des mécanismes de commentaires et de correction en temps réel. Des explications détaillées et des pointeurs vers des exemples de ressources sont inclus.

Cette rubrique contient les sections suivantes.

-   [améliorations de Direct3D 9ex pour Windows 7](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [Présentation du mode de basculement de Direct3D 9EX](#direct3d-9ex-flip-mode-presentation)
-   [Modèle de programmation et API](#programming-model-and-apis)
    -   [Comment s’abonner au modèle de basculement Direct3D 9Ex](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [Instructions de conception pour les applications de basculement Direct3D 9Ex](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [Synchronisation des frames des applications Direct3D 9Ex Flip Model](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [Synchronisation des frames pour les applications Windows lorsque DWM est désactivé](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [Guide pas à pas d’un modèle de basculement Direct3D 9Ex et présentation de l’exemple de statistiques](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [résumé des Recommandations de programmation pour la synchronisation de frames](#summary-of-programming-recommendations-for-frame-synchronization)
-   [Conclusion sur les améliorations Direct3D 9Ex](#conclusion-about-direct3d-9ex-improvements)
-   [Appel à l’action](#call-to-action)
-   [Rubriques connexes](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a>améliorations de Direct3D 9ex pour Windows 7

la présentation en mode Flip de direct3d 9ex est un mode amélioré de présentation d’images dans direct3d 9ex qui transmet efficacement les images rendues à Windows 7 Gestionnaire de fenêtrage (DWM) pour la composition. à compter de Windows Vista, DWM compose la totalité du bureau. Lorsque DWM est activé, les applications en mode fenêtre présentent leur contenu sur le Bureau à l’aide d’une méthode appelée mode BLT présente dans DWM (ou le modèle BLT). Avec le modèle BLT, DWM conserve une copie de la surface de rendu Direct3D 9Ex pour la composition du bureau. Lorsque l’application est mise à jour, le nouveau contenu est copié vers la surface DWM via un BLT. Pour les applications qui contiennent du contenu Direct3D et GDI, les données GDI sont également copiées sur la surface DWM.

disponible dans Windows 7, le Mode Flip présent dans DWM (ou Flip Model) est une nouvelle méthode de présentation qui permet essentiellement de passer les descripteurs des surfaces d’application entre les applications en Mode fenêtre et le DWM. Outre l’enregistrement des ressources, l’inversion du modèle prend en charge les statistiques actuelles améliorées.

Les statistiques présentent les informations de minutage des trames que les applications peuvent utiliser pour synchroniser les flux vidéo et audio et récupérer des problèmes de lecture vidéo. Les informations de minutage de trame dans les statistiques actuelles permettent aux applications d’ajuster la vitesse de présentation de leurs images vidéo pour une présentation plus lisse. dans Windows Vista, où dwm gère une copie correspondante de la surface de frame pour la composition du bureau, les applications peuvent utiliser les statistiques fournies par DWM. cette méthode d’obtention des statistiques actuelles sera toujours disponible dans Windows 7 pour les applications existantes.

dans Windows 7, les applications Direct3D 9ex qui adoptent la fonction Flip Model doivent utiliser des api D3D9Ex pour obtenir les statistiques actuelles. Lorsque DWM est activé, les applications en mode fenêtre et en mode exclusif Direct3D 9Ex peuvent attendre les mêmes informations sur les statistiques lors de l’utilisation de Flip Model. Direct3D 9Ex Flip Model sent Statistics permet aux applications d’interroger les statistiques actuelles en temps réel, plutôt qu’une fois que le frame a été affiché à l’écran. les mêmes informations statistiques sont disponibles pour les applications en mode fenêtre Flip-Model activées en tant qu’applications plein écran. un indicateur ajouté dans les API D3D9Ex permet aux applications de retournement de supprimer efficacement les trames tardives au moment de la présentation.

le modèle de retournement de Direct3D 9ex doit être utilisé par les nouvelles applications vidéo ou de présentation basées sur la fréquence des images qui ciblent Windows 7. En raison de la synchronisation entre le DWM et le runtime Direct3D 9Ex, les applications qui utilisent Flip Model doivent spécifier entre 2 et 4 mémoires tampons pour garantir une présentation fluide. Les applications qui utilisent les informations de statistiques actuelles tireront parti de l’amélioration des statistiques de retournement activé.

## <a name="direct3d-9ex-flip-mode-presentation"></a>Présentation du mode de basculement de Direct3D 9EX

Les améliorations des performances du mode de basculement de Direct3D 9Ex sont importantes sur le système lorsque DWM est activé et lorsque l’application est en mode fenêtre, plutôt qu’en mode exclusif plein écran. Le tableau et l’illustration suivantes présentent une comparaison simplifiée des utilisations de la bande passante de la mémoire et des lectures et écritures système des applications Windows qui choisissent le modèle Flip Model et le modèle BLT d’utilisation par défaut.



| Mode BLT présent dans DWM                                                                                                 | Mode de basculement de D3D9Ex présent dans DWM                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1. l’application met à jour son Frame (écriture)<br/>                                                                 | 1. l’application met à jour son Frame (écriture)<br/>                     |
| 2. le runtime Direct3D copie le contenu de la surface dans une surface de redirection DWM (lecture, écriture)<br/>                       | 2. le runtime Direct3D passe l’aire de l’application à DWM<br/>        |
| 3. une fois la copie de la surface partagée terminée, DWM restitue l’aire de l’application sur l’écran (lecture, écriture)<br/> | 3. DWM affiche l’aire de l’application sur l’écran (lecture, écriture)<br/> |



 

![illustration d’une comparaison entre le modèle BLT et le modèle Flip](images/blt-flip-mode-present.png)

Le mode de basculement présent réduit l’utilisation de la mémoire système en réduisant le nombre de lectures et d’écritures par le runtime Direct3D pour la composition de frame avec fenêtres par DWM. Cela réduit la consommation d’énergie du système et l’utilisation de la mémoire globale.

Les applications peuvent tirer parti du mode de basculement Direct3D 9Ex présentent des améliorations des statistiques lorsque DWM est activé, que l’application soit en mode fenêtre ou en mode exclusif plein écran.

## <a name="programming-model-and-apis"></a>Modèle de programmation et API

les nouvelles applications vidéo ou de fréquence d’images qui utilisent des api Direct3D 9ex sur Windows 7 peuvent tirer parti de la mémoire et des économies d’énergie, ainsi que de la présentation améliorée proposée par le Mode Flip sur Windows 7. (en cas d’exécution sur les versions antérieures de Windows, le runtime Direct3D utilise le Mode Blt de l’application.)

Le mode de basculement présente que l’application peut tirer parti des mécanismes de commentaires et de correction des statistiques en temps réel lorsque DWM est activé. Toutefois, les applications qui utilisent le mode Flip doivent être conscientes des limitations lorsqu’elles utilisent le rendu simultané de l’API GDI.

Vous pouvez modifier les applications existantes pour tirer parti du mode de basculement, avec les mêmes avantages et les mêmes avertissements que les applications récemment développées.

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a>Comment s’abonner au modèle de basculement Direct3D 9Ex

les applications Direct3D 9ex qui ciblent Windows 7 peuvent s’abonner au modèle de basculement en créant la chaîne de permutation avec la valeur d’énumération [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) . Pour s’abonner au modèle Flip, les applications spécifient la structure de [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) , puis passent un pointeur vers cette structure lorsqu’ils appellent l’API [**IDirect3D9Ex :: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) . cette section décrit comment les applications qui ciblent Windows 7 utilisent **IDirect3D9Ex :: CreateDeviceEx** pour s’abonner au modèle de retournement. Pour plus d’informations sur l’API **IDirect3D9Ex :: CreateDeviceEx** , consultez **IDirect3D9Ex :: CreateDeviceEx sur MSDN**.

Pour plus de commodité, la syntaxe des [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) et [**IDirect3D9Ex :: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) sont répétées ici.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

lorsque vous modifiez des applications Direct3D 9ex pour Windows 7 afin d’accepter le modèle de basculement, vous devez prendre en compte les éléments suivants concernant les membres spécifiés des [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters):

<dl> <dt>

**BackBufferCount**
</dt> <dd>

(Windows 7 uniquement)

Quand **SwapEffect** est défini sur le nouveau \_ type d’effet de chaîne d’échange FLIPEX D3DSWAPEFFECT, le nombre de mémoires tampons d’arrière-plan doit être égal ou supérieur à 2, pour empêcher une baisse des performances de l’application en raison de l’attente de la libération de la mémoire tampon précédente précédente par DWM.

Lorsque l’application utilise également les statistiques actuelles associées à D3DSWAPEFFECT \_ FLIPEX, nous vous recommandons de définir le nombre de mémoires tampons d’arrière-plan sur une valeur comprise entre 2 et 4.

l’utilisation de D3DSWAPEFFECT \_ FLIPEX sur Windows Vista ou des versions antérieures du système d’exploitation échoue à partir de [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

**SwapEffect**
</dt> <dd>

(Windows 7 uniquement)

Le nouveau \_ type d’effet de chaîne de permutation D3DSWAPEFFECT FLIPEX désigne le moment où une application adopte le mode Flip présent dans DWM. Il permet à l’application d’utiliser plus efficacement la mémoire et la puissance, et permet également à l’application de tirer parti des statistiques de présentation en plein écran en mode fenêtre. Le comportement de l’application en plein écran n’est pas affecté. Si Windowed a la valeur **true** et que **SwapEffect** a la valeur D3DSWAPEFFECT \_ FLIPEX, le runtime crée une mémoire tampon d’arrière-plan supplémentaire et fait pivoter le handle qui appartient à la mémoire tampon qui devient la mémoire tampon d’arrière-plan au moment de la présentation.

</dd> <dt>

**Indicateurs**
</dt> <dd>

(Windows 7 uniquement)

L’indicateur de [ \_ \_ mémoire tampon D3DPRESENTFLAG verrouillable](/windows/desktop/direct3d9/d3dpresentflag) ne peut pas être défini si **SwapEffect** est défini sur le nouveau type d’effet de chaîne de permutation [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) .

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a>Instructions de conception pour les applications de basculement Direct3D 9Ex

Utilisez les instructions des sections suivantes pour concevoir vos applications Direct3D 9Ex Flip Model.

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a>Utiliser le mode Flip présent dans un HWND distinct du mode BLT présent

Les applications doivent utiliser le mode de basculement de Direct3D 9Ex présent dans un HWND qui n’est pas également ciblé par d’autres API, y compris le mode BLT présente Direct3D 9Ex, d’autres versions de Direct3D ou GDI. Le mode de basculement présent peut être utilisé pour présenter des fenêtres enfants. autrement dit, les applications peuvent utiliser Flip Model lorsqu’elles ne sont pas mélangées avec le modèle BLT dans le même HWND, comme indiqué dans les illustrations suivantes.

![illustration de la fenêtre parente Direct3D et d’une fenêtre enfant GDI, chacune avec son propre HWND](images/parent-d3d.png)

![illustration de la fenêtre parente GDI et d’une fenêtre enfant Direct3D, chacune avec son propre HWND](images/parent-gdi.png)

Étant donné que le modèle BLT gère une copie supplémentaire de la surface, GDI et d’autres contenus Direct3D peuvent être ajoutés au même HWND par le biais de mises à jour fragmentées de Direct3D et GDI. À l’aide du modèle de retournement, seul le contenu Direct3D 9Ex dans les chaînes de permutation [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) transmises à DWM sera visible. Toutes les autres mises à jour de contenu Direct3D ou GDI du modèle BLT seront ignorées, comme indiqué dans les illustrations suivantes.

![illustration du texte GDI qui peut ne pas s’afficher si l’utilisation de l’opération Flip Model est utilisée et que le contenu Direct3D et GDI se trouvent dans le même HWND](images/d3d-gdi-same-hwnd.png)

![illustration du contenu Direct3D et GDI dans lequel DWM est activé et l’application est en mode fenêtre](images/d3d-gdinotext-same-hwnd.png)

Par conséquent, le modèle de retournement doit être activé pour les surfaces de tampon de chaîne de permutation où le modèle de basculement Direct3D 9Ex est rendu seul au HWND entier.

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a>N’utilisez pas Flip Model avec ScrollWindow ou ScrollWindowEx de GDI

Certaines applications Direct3D 9Ex utilisent les fonctions ScrollWindow ou ScrollWindowEx de GDI pour mettre à jour le contenu de la fenêtre lorsqu’un événement de défilement utilisateur est déclenché. ScrollWindow et ScrollWindowEx effectuent la blts du contenu des fenêtres à l’écran lors du défilement d’une fenêtre. Ces fonctions nécessitent également des mises à jour du modèle BLT pour le contenu GDI et Direct3D 9Ex. Les applications qui utilisent l’une ou l’autre des fonctions n’affichent pas nécessairement l’affichage du contenu de la fenêtre visible à l’écran quand l’application est en mode fenêtre et que DWM est activé. Nous vous recommandons de ne pas utiliser les API ScrollWindow et ScrollWindowEx de GDI dans vos applications, et de redessiner à la place leur contenu à l’écran en réponse au défilement.

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a>Utiliser une \_ chaîne de permutation D3DSWAPEFFECT FLIPEX par HWND

Les applications qui utilisent Flip Model ne doivent pas utiliser plusieurs chaînes de permutation de modèle ciblant le même HWND.

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a>Synchronisation des frames des applications Direct3D 9Ex Flip Model

Les statistiques présentent les informations de minutage des frames utilisées par les applications multimédias pour synchroniser les flux vidéo et audio et récupérer des défauts de lecture vidéo. Pour activer la disponibilité des statistiques, l’application Direct3D 9Ex doit s’assurer que le paramètre *BehaviorFlags* transmis par l’application à [**IDirect3D9Ex :: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contient l’indicateur de comportement de l’appareil [D3DCREATE \_ Enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).

Pour plus de commodité, la syntaxe de [**IDirect3D9Ex :: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) est répétée ici.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

Le modèle de basculement Direct3D 9Ex ajoute l’indicateur de présentation [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) qui applique le comportement de l’indicateur de présentation [ \_ \_ immédiate intervalle D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) . L’application Direct3D 9Ex spécifie ces indicateurs de présentation dans le paramètre *dwFlags* que l’application transmet à [**IDirect3DDevice9Ex ::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), comme illustré ici.

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

lorsque vous modifiez votre application Direct3D 9ex pour Windows 7, vous devez tenir compte des informations suivantes sur les indicateurs de présentation [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) spécifiés :

<dl> <dt>

[D3DPRESENT \_ DONOTFLIP](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

Cet indicateur est disponible uniquement en mode plein écran ou

(Windows 7 uniquement)

Lorsque l’application définit le membre **SwapEffect** des [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) sur [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) dans un appel à [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

[D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

(Windows 7 uniquement)

Cet indicateur peut être spécifié uniquement si l’application définit le membre **SwapEffect** des [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) sur [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) dans un appel à [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex). L’application peut utiliser cet indicateur pour mettre immédiatement à jour une surface avec plusieurs frames plus loin dans la file d’attente de DWM présente, en ignorant essentiellement les frames intermédiaires.

Les applications FlipEx avec fenêtres peuvent utiliser cet indicateur pour mettre immédiatement à jour une surface avec un frame qui est plus tard dans la file d’attente présente dans le DWM, en ignorant les frames intermédiaires. Cela s’avère particulièrement utile pour les applications multimédias qui souhaitent ignorer les trames qui ont été détectées en retard et présentent les trames suivantes au moment de la composition. [**IDirect3DDevice9Ex ::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) retourne une erreur de paramètre non valide si cet indicateur n’est pas correctement spécifié.

</dd> </dl>

Pour obtenir les informations de statistiques actuelles, l’application obtient la structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) en appelant l’API [**IDirect3DSwapChain9Ex :: GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .

La structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) contient des statistiques sur [**IDirect3DDevice9Ex ::P**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) les appels resentex. L’appareil doit être créé à l’aide d’un appel de [**IDirect3D9Ex :: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) avec l’indicateur [D3DCREATE \_ Enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) . Sinon, les données retournées par [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ne sont pas définies. Une chaîne de permutation Direct3D 9Ex avec basculement de modèle fournit les informations de statistiques en mode fenêtre et en mode plein écran.

Pour les chaînes de permutation Direct3D 9Ex compatibles avec le modèle BLT en mode fenêtre, toutes les valeurs de la structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) sont des zéros.

Pour FlipEx présente les statistiques, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) retourne \_ D3DERR \_ présente \_ des statistiques disjointes dans les situations suivantes :

-   Premier appel à [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) jamais, qui indique le début d’une séquence
-   Conversion DWM de on à OFF
-   Changement de mode : mode avec fenêtre, en mode plein écran ou plein écran pour les transitions en plein écran

Pour plus de commodité, la syntaxe de [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) est répétée ici.

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

La méthode [**IDirect3DSwapChain9Ex :: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) retourne le dernier PresentCount, autrement dit, l’ID actuel du dernier appel présent réussi qui a été effectué par un périphérique d’affichage associé à la chaîne de permutation. Cet ID est la valeur du membre **PresentCount** de la structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) . Pour les chaînes de permutation Direct3D 9Ex compatibles avec le modèle BLT, en mode fenêtre, toutes les valeurs de la structure **D3DPRESENTSTATS** sont des zéros.

Pour plus de commodité, la syntaxe de [**IDirect3DSwapChain9Ex :: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) est répétée ici.

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

lorsque vous modifiez votre application Direct3D 9ex pour Windows 7, vous devez prendre en compte les informations suivantes sur la structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) :

-   La valeur PresentCount renvoyée par [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) n’est pas mise à jour lorsqu’un appel [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) avec D3DPRESENT \_ DONOTWAIT spécifié dans le paramètre *dwFlags* retourne un échec.
-   Quand [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) est appelé avec D3DPRESENT \_ DONOTFLIP, un appel [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) se déroule correctement, mais ne retourne pas de structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) mise à jour lorsque l’application est en mode fenêtre.
-   **PresentRefreshCount** et **SyncRefreshCount** dans [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):
    -   **PresentRefreshCount** est égal à **SyncRefreshCount** lorsque l’application s’affiche sur chaque Vsync.
    -   **SyncRefreshCount** est obtenu à l’intervalle Vsync lorsque le présent a été envoyé, **SyncQPCTime** est approximativement l’heure associée à l’intervalle de Vsync.

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a>Synchronisation des frames pour les applications Windows lorsque DWM est désactivé

Lorsque DWM est désactivé, les applications en fenêtre s’affichent directement sur l’écran du moniteur sans passer par une chaîne de basculement. dans Windows Vista, il n’existe pas de prise en charge pour l’obtention d’informations de statistiques de frame pour les applications windows lorsque DWM est désactivé. pour gérer une API dans laquelle les applications n’ont pas besoin de prendre en charge le dwm, Windows 7 retourne les informations de statistiques de frame pour les applications windows lorsque DWM est désactivé. Les statistiques de frame retournées lorsque DWM est désactivé sont des estimations uniquement.

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a>Walk-Through d’un modèle de basculement et de présentation des statistiques Direct3D 9Ex

**Pour choisir FlipEx Presentation pour Direct3D 9Ex, exemple**

1.  vérifiez que l’exemple d’application s’exécute sur la version du système d’exploitation Windows 7 ou version ultérieure.
2.  Définissez le membre **SwapEffect** des [**\_ paramètres D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) sur [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) dans un appel à [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



**Pour s’abonner également aux statistiques de présentation de FlipEx associées à Direct3D 9Ex, exemple**

-   Définissez [D3DCREATE \_ Enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) dans le paramètre *BehaviorFlags* de [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



**Pour éviter, détecter et récupérer des problèmes**

1.  Appels présents dans la file d’attente : le nombre de tampons en mémoire recommandée est compris entre 2 et 4.
2.  L’exemple Direct3D 9Ex ajoute une mémoire tampon de base implicite, la longueur réelle de la file d’attente est le nombre de tampons de la mémoire \ + 1.
3.  Créer une structure d’application d’assistance présente la structure de file d’attente pour stocker tous les ID présents de présent de la présente (PresentCount) et les PresentRefreshCount associés, calculés/attendus.
4.  Pour détecter une occurrence de problème :

    -   Appelez [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).
    -   Obtenez l’ID actuel (PresentCount) et le nombre de Vsync où le frame est affiché (PresentRefreshCount) du frame dont les statistiques actuelles sont obtenues.
    -   Récupérez le PresentRefreshCount attendu (TargetRefresh dans l’exemple de code) associé à l’ID présent.
    -   Si le PresentRefreshCount réel est plus tard que prévu, un problème s’est produit.

5.  Pour effectuer une récupération suite à un problème :

    -   Calculez le nombre de frames à ignorer ( \_ variable g iImmediates dans l’exemple de code).
    -   Présentez les frames ignorés avec l’intervalle D3DPRESENT \_ FORCEIMMEDIATE.

**Considérations relatives à la détection et à la récupération des problèmes**

1.  La récupération de problème prend la variable N (g \_ iQueueDelay dans l’exemple de code) nombre d’appels présents où N (g \_ iQueueDelay) est égal à g \_ iImmediates plus la longueur de la file d’attente actuelle, c’est-à-dire :

    -   Frames ignorés avec l’intervalle présent D3DPRESENT \_ FORCEIMMEDIATE, plus
    -   Mises en file d’attente qui doivent être traitées

2.  Définissez une limite sur la longueur du problème ( \_ \_ limite de récupération des problèmes dans l’exemple). Si l’exemple d’application ne peut pas récupérer à partir d’un problème trop long (par exemple, 1 seconde, ou 60 vsyncs sur 60 Hz), passez l’animation intermittente et réinitialisez la file d’attente d’assistance actuelle.


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



**Exemple de scénario**

-   L’illustration suivante montre une application avec un nombre de tampons de mémoire tampon de 4. La longueur réelle de la file d’attente actuelle est donc 5.

    ![illustration d’une mise en file d’attente d’appliances et de la file d’attente actuelle](images/sample-scenario.png)

    Le frame A est destiné à être affiché à l’écran sur le nombre d’intervalles de synchronisation de 1, mais a détecté qu’il a été affiché sur le nombre d’intervalles de synchronisation de 4. Par conséquent, un problème s’est produit. Les 3 images suivantes sont présentées avec D3DPRESENT \_ Interval \_ FORCEIMMEDIATE. Le problème doit prendre un total de 8 appels présents avant de pouvoir être récupéré : le frame suivant sera affiché en fonction du nombre d’intervalles de synchronisation ciblés.

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a>résumé des Recommandations de programmation pour la synchronisation de frames

-   Créez une liste de sauvegarde de tous les ID LastPresentCount (obtenus via [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) et des PresentRefreshCount estimés associés de tous les cadeaux soumis.
    > [!Note]  
    > Lorsque l’application appelle [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) avec D3DPRESENT \_ DONOTFLIP, l’appel [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) a échoué mais ne retourne pas de structure [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) mise à jour lorsque l’application est en mode fenêtre.

     

-   Appelez [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) pour obtenir le PresentRefreshCount réel associé à chaque ID actuel des frames affichés, pour vous assurer que l’application gère les retours d’échec de l’appel.
-   Si le PresentRefreshCount réel est postérieur au PresentRefreshCount estimé, un problème est détecté. Compenser en envoyant des frames de retard» présent avec D3DPRESENT \_ FORCEIMMEDIATE.
-   Quand un frame est présenté en retard dans la file d’attente actuelle, tous les frames mis en file d’attente suivants sont présentés en retard. D3DPRESENT \_ FORCEIMMEDIATE corrigera uniquement le frame suivant qui sera présenté après tous les frames mis en file d’attente. Par conséquent, le nombre de files d’attente ou de mises en mémoire tampon actuelles ne doit pas être trop long. il y a donc moins de problèmes de trames à intercepter. Le nombre optimal de mémoires tampons est de 2 à 4.
-   Si le PresentRefreshCount estimé est postérieur au PresentRefreshCount réel, la limitation DWM peut s’être produite. Les solutions suivantes sont possibles :

    -   réduction de la longueur actuelle de la file d’attente
    -   réduction des besoins en mémoire du GPU avec d’autres moyens, en plus de réduire la longueur de la file d’attente actuelle (autrement dit, la réduction de la qualité, la suppression des effets, etc.)
    -   spécification de [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) pour empêcher la limitation DWM en général

-   Vérifiez la fonctionnalité d’affichage de l’application et les performances des statistiques de frame dans les scénarios suivants :

    -   avec DWM activé et désactivé
    -   modes exclusif et avec fenêtre plein écran
    -   matériel de capacité inférieure

-   Lorsque les applications ne peuvent pas récupérer à partir d’un grand nombre de trames avec D3DPRESENT \_ FORCEIMMEDIATE présentes, elles peuvent potentiellement effectuer les opérations suivantes :

    -   Réduisez l’utilisation du processeur et du GPU en rendant moins de charge de travail.
    -   en cas de décodage vidéo, décodez plus rapidement en réduisant la qualité et, par conséquent, l’utilisation du processeur et du GPU.

## <a name="conclusion-about-direct3d-9ex-improvements"></a>Conclusion sur les améliorations Direct3D 9Ex

sur Windows 7, les applications qui affichent la fréquence d’images vidéo ou de jauge pendant la présentation peuvent choisir de retourner le modèle. Les améliorations actuelles des statistiques associées à la fonction Flip Model Direct3D 9Ex peuvent tirer parti des applications qui synchronisent la présentation par fréquence d’images, avec des commentaires en temps réel sur la détection et la récupération des problèmes. Les développeurs qui adoptent le modèle de basculement Direct3D 9Ex doivent prendre en compte un HWND distinct du contenu GDI et de la synchronisation de la fréquence d’images. Reportez-vous aux détails de cette rubrique et à la documentation MSDN. Pour obtenir une documentation supplémentaire, consultez [le centre de développement DirectX sur MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).

## <a name="call-to-action"></a>À vous d’agir !

nous vous encourageons à utiliser le modèle de basculement Direct3D 9ex et ses statistiques sur Windows 7 lorsque vous créez des applications qui tentent de synchroniser la fréquence des images de présentation ou de récupérer à partir de défauts d’affichage.

## <a name="related-topics"></a>Rubriques connexes

[Centre de développement DirectX sur MSDN](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> </dl>