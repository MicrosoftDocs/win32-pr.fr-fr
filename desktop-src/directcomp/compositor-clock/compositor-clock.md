---
title: Horloge du compositeur
description: L’API d’horloge du compositeur offre des statistiques et un contrôle de la fréquence d’images pour la présentation fluide du contenu à l’écran, à la cadence la plus rapide possible et sur diverses configurations matérielles.
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 211684d8e199c61ec76fad6dbad168088056473a
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128523852"
---
# <a name="compositor-clock"></a>Horloge du compositeur

> [!NOTE]
> **Certaines informations portent sur la préversion du produit, qui est susceptible d’être en grande partie modifié avant sa commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.**

## <a name="overview"></a>Vue d’ensemble

L’API d’horloge du compositeur offre des statistiques et un contrôle de la fréquence d’images pour la présentation fluide du contenu à l’écran, à la cadence la plus rapide possible et sur diverses configurations matérielles. Traditionnellement, cela a été géré par les API DirectX. Mais ceux-ci ont des liens forts vers des configurations à taux d’actualisation fixe et à affichage unique. Par exemple, voici une partie simplifiée du pseudo-code illustrant la façon dont les applications sont généralement créées pour dessiner au taux de rafraîchissement de l’affichage.

```cpp
void GameLoop()
{
    CreateRenderingObjects();
    auto pSwapChain = CreateSwapChain();

    while (pSwapChain->WaitForVerticalBlank())
    {
        ProcessInput();
        RenderFrame(pSwapChain);
        pSwapChain->Present();
    }
}
```

Dans ce type de boucle, l’hypothèse est qu’il n’y a qu’une cadence verticale unique (vblank). Il n’est pas évident de savoir ce que l’application doit faire si sa fenêtre chevauche deux analyses dont l’analyse est hors phase ou qui ont des fréquences différentes. En fait, l’API DXGI utilise permutation utilise toujours la cadence de l’analyse principale, quelle que soit la fenêtre sur laquelle l’application s’affiche. Cela pose des problèmes pour les applications qui souhaitent une présentation sans heurts de tous les moniteurs. Un exemple réel est la lecture vidéo sur un moniteur secondaire qui a une actualisation différente de la base de données primaire. un scénario qui existait depuis le lancement de plusieurs moniteurs ; de plus, il affecte de manière disproportionnée les joueurs, qui ont tendance à avoir un moniteur 60 Hz pour l’interface utilisateur secondaire et une fréquence plus élevée (144 + Hz) pour les jeux.

Le deuxième problème courant est celui qui consiste à régler la fréquence d’images en fonction des performances de l’ordinateur. C’est généralement le cas pour les applications de lecture vidéo, qui souhaitent savoir si les trames vidéo sont visibles par l’utilisateur au moment prévu, ou si les problèmes compliquent la présentation, dans l’espoir d’ajuster la présentation pour obtenir de meilleures performances. Par exemple, un service de streaming vidéo peut basculer vers un flux de qualité inférieure si l’ordinateur ne peut pas supporter la fréquence d’images souhaitée à la qualité la plus élevée. Cela est également géré par les API DXGI et est donc affecté par la même limitation d’exposition de l’architecture et de l’API.

Enfin, l’API offre aux applications la possibilité de participer à une nouvelle fonctionnalité d’amélioration de la fréquence d’images appelée fréquence d’actualisation dynamique, dans laquelle le système s’exécute à un taux d’actualisation relativement faible pour les opérations normales, &mdash; par exemple 60 Hz, &mdash; mais elle accélère jusqu’à une fréquence plus élevée, &mdash; par exemple, 120Hz &mdash; quand une application effectue certaines opérations sensibles à la latence, telles que l’encrage  ou le panoramique tactile. La fonctionnalité boosting existe car l’exécution à la fréquence élevée 100% du temps est prohibitif du point de vue de la consommation énergétique. En même temps, en raison des mêmes limitations de l’API DXGI, le basculement de la fréquence d’actualisation de l’affichage à des moments arbitraires est généralement onéreux, impliquant des notifications de changement de mode de diffusion à toutes les applications, ainsi que les coûts de toutes ces applications qui exécutent du code pour répondre à la modification. Par conséquent, la fonctionnalité augmenter la fréquence d’actualisation effectue une modification de configuration légère qui n’émet pas de notifications, mais qui, par conséquent, doit être extraite de la plupart des applications, ce qui continue à croire que le système s’exécute à la fréquence inférieure. Cette virtualisation fonctionne en émettant des applications uniquement pour chaque vblank, ou tous les trois vblanks, ou tout autre intervalle entier, afin que l’application puisse voir un taux de rafraîchissement effectif qui est une fraction entière de la fréquence réelle. Cela permet d’utiliser le mécanisme vblank existant sans coût supplémentaire pour générer une fréquence inférieure parfaite. Le vblank aligné est représenté par un mode de fréquence d’actualisation dynamique dans le système d’exploitation (se), par exemple 60 Hz/120Hz. Notez que, par conséquent, la fonctionnalité Booster ne fonctionne que pour augmenter la fréquence jusqu’à une fréquence plus élevée, jamais plus faible, car elle n’est pas aussi coûteuse à insérer des vblanks artificiels que d’ignorer les vblanks réels.

L’API de l’horloge du compositeur permet à votre application non seulement de demander à ce que le système entre en mode Boost, mais également d’observer la véritable fréquence d’actualisation dans ce mode, afin que vous puissiez présenter le contenu à la fréquence supérieure.

## <a name="the-api"></a>L'API

L’API comporte trois parties. La première offre une pulsation indépendante de l’affichage pour les applications qui souhaitent présenter une fréquence d’images sur plusieurs moniteurs. Le deuxième permet aux applications de demander une augmentation de fréquence avec une fréquence d’actualisation dynamique. La troisième offre des statistiques sur le comportement du moteur de composition système, séparées pour chaque affichage individuel.

Chaque partie de l’API influence ou observe le cycle de travail du compositeur système. Ce cycle de travail est une cadence régulière qui produit un seul frame de compositeur par cycle. Ce cycle peut ou non être aligné pour afficher vblanks, en fonction de la charge de travail du système, du nombre d’affichages et d’autres facteurs.

## <a name="wait-for-the-compositor-clock"></a>Attendre l’horloge du compositeur

L’objectif de ce signal est de remplacer l’utilisation de la méthode [**IDXGIOutput :: WaitForVBlank**](/windows/win32/api/dxgi/nf-dxgi-idxgioutput-waitforvblank) , tout en offrant une plus grande flexibilité dans différents taux de rafraîchissement et en simplifiant les modèles d’utilisation pour les développeurs. Comme avec **WaitForVBlank**, le système doit savoir si une application attend ce signal, de sorte qu’en l’absence d’application, le système peut diriger la carte vidéo pour désactiver l’interruption verticale vide. 

Cela est essentiel pour la gestion de l’alimentation, ce qui limite l’architecture de l’API à un appel de fonction d’attente, au lieu d’accepter ou de retourner un événement (le système graphique ne peut pas déterminer si elle est attendue ou non). À ce niveau bas, les applications sont censées utiliser cette API pour contrôler les threads de rendu, séparées des threads de l’interface utilisateur à usage général, de la même façon que **IDXGIOutput :: WaitForVBlank** est traditionnellement utilisé.

Comme mentionné dans la vue d’ensemble, l’horloge du compositeur peut prendre en charge plusieurs aspects pour ce **WaitForVBlank** .

* Zone verticale suivante vide lorsque l’horloge du compositeur n’est pas nécessairement source de l’affichage principal.
* Éveil des applications à des taux variables sur les affichages qui prennent en charge la fréquence d’actualisation dynamique.
* Éveil des applications pour les événements définis par l’application.

En général, il est prévu que de nombreuses applications veulent rester synchronisées avec l’horloge du compositeur pour le meilleur moment. Toutefois, certaines exceptions peuvent inclure des frameworks multimédia et des jeux qui doivent sortir de veille sur la barre verticale d’un affichage spécifique.

### <a name="handle-usage-with-compositor-clock"></a>Gérer l’utilisation avec l’horloge du compositeur

Les applications se réveillent actuellement à chaque zone verticale par le biais du mécanisme de DXGI, mais ont souvent d’autres événements dont ils ont besoin pour sortir de veille également. Plutôt que de gérer ces événements séparément, l’horloge du compositeur peut prendre des handles pour plusieurs événements et signaler le frame suivant et chaque fois que les événements se déclenchent. L’application peut ensuite sortir d’un signal, en connaissant l’événement qui l’a déclenchée.

### <a name="cycle-for-compositor-clock-events"></a>Cycle pour les événements d’horloge du compositeur

L’horloge du compositeur se met toujours en éveil à l’emplacement vertical d’une analyse ou d’une autre minuterie. Lorsque le compositeur est en veille, mais que l’affichage est toujours en cours de mise à jour, ce signal est toujours déclenché à l’vblank de l’affichage principal.

### <a name="c-example"></a>Exemple C++

```cpp
void GameLoop(HANDLE hQuitGameEvent)
{
    DWORD waitResult;

    CreateRenderingObjects();
    auto pSwapChain = CreateSwapChain();

    do
    {
        // Do all of the work for a single frame
        ProcessInput();
        RenderFrame(pSwapChain);
        pSwapChain->Present();

        // Wait for the compositor heartbeat before starting a new frame
        waitResult = DCompositionWaitForCompositorClock(1, &hQuitGameEvent, INFINITE);

        // If we get WAIT_RESULT_0+count it means the compositor clock ticked,
        // and we should render another frame. Our count is one, as we're
        // passing only one extra handle. Otherwise, either we got a failure or
        // another thread signaled our "quit" event, and in either case we want
        // to exit the loop
    } while (waitResult == WAIT_OBJECT_0 + 1);
}
```

## <a name="boost-compositor-clock"></a>Augmenter l’horloge du compositeur

Lorsque la source de l’horloge du compositeur prend en charge la fréquence d’actualisation dynamique (cette fonctionnalité est activée dans les paramètres d’affichage avancés ; uniquement utilisable sur la fréquence d’actualisation des variables s’affiche avec les pilotes de support) le système est en mesure de basculer dynamiquement entre deux taux. Il y a un mode non renforcé, qui est généralement 60 Hz, et un taux optimisé qui est généralement 2x plus élevé sur 120Hz. Ce taux d’actualisation plus élevé doit être utilisé pour améliorer le contenu sensible à la latence, tel que l’encrage numérique. Le diagramme ci-dessous montre comment le système passe de l’exécution à une vitesse de base de 60 Hz (Flip 1), puis à 6 images (2-7) avec une encre numérique dépassée à 120Hz. Enfin, une fois que l’encre numérique n’est plus mise à jour, le système bascule en mode 60Hz.

Voici une illustration de la fréquence d’images dynamique pour l’amélioration.

![taux d’actualisation renforcé sur flip2 ; l’encrage se termine par flip8 et le taux revient à 60 Hz](images/dyn-refresh-rate.png)

Et voici comment DWM gère les demandes Boost.

![Organigramme illustrant comment DWM gère les demandes d’amélioration](images/dwm-boosting.png)

Si une application nécessitant une augmentation est terminée, les demandes Boost de l’application sont également arrêtées. Les applications qui sont toujours actives avec plusieurs demandes de boosting peuvent vérifier le nombre de références pour déterminer le nombre de fois qu’elles peuvent être désactivées. L’optimisation des appels est entièrement compatible, même si le système n’est pas en mode de fréquence d’actualisation dynamique, où le multiplicateur Booster est 1x.

### <a name="c-example"></a>Exemple C++

Cet exemple traite **WM_TOUCH** pour augmenter la fréquence d’actualisation chaque fois que cette application reçoit des entrées tactiles, dans le but de fournir une expérience de panoramique tactile de haute fréquence et lisse. Une application plus sophistiquée peut exécuter la reconnaissance de mouvement en premier, et augmenter uniquement si un panoramique est détecté.

```cpp
int g_activeTouchPoints = 0;

LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;
    UINT inputCount = LOWORD(wParam);
    auto hTouchInput = reinterpret_cast<HTOUCHINPUT>(lParam);

    // Allocate room for touch data (assume throwing new)
    auto pInputs = new TOUCHINPUT[inputCount];

    if (GetTouchInputInfo(hTouchInput, inputCount, pInputs, sizeof(TOUCHINPUT)))
    {
        for (int index = 0; index < inputCount; index++)
        {
            auto& touchInput = pInputs[index];

            // The first time we receive a touch down, boost the compositor
            // clock so we do our stuff at high frequency. Once the last touch
            // up happens, return to the base frequency
            if (touchInput.dwFlags & TOUCHEVENTF_DOWN)
            {
                if (!g_activeTouchPoints)
                {
                    // We're going from zero to one active points -- boost 
                    DCompositionBoostCompositorClock(true);
                }

                g_activeTouchPoints++;
            }
            else if (touchInput.dwFlags && TOUCHEVENTWF_UP)
            {
                g_activeTouchPoints--;

                if (g_activeTouchPoints == 0)
                {
                    DCompositionBoostCompositorClock(false);
                }
            }

            // Perform other normal touch processing here...
        }

        // We handled the window message; close the handle
        CloseTouchInputHandle(hTouchInput);
    }
    else
    {
        // We couldn't handle the message; forward it to the system
        result = DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
    }

    delete[] pInputs;
    return result;
}
```

## <a name="frame-statistics"></a>Statistiques de frame

> [!NOTE]
> Nous pensons que les applications utilisent la fonctionnalité des statistiques de frame principalement pour la télémétrie, et non pour l’ajustement du contenu.

Windows applications envoient souvent du contenu au compositeur qui est affiché dans différents emplacements sur les adaptateurs et écrans d’affichage. Nous n’effectuons pas toujours le rendu sur un écran, c’est pourquoi dans cette API, nous utilisons des [*cibles*](#glossary). Plutôt que de compter sur une seule statistique pour représenter quand un frame atteint l’écran, [**DCompositionGetTargetStatistics**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongettargetstatistics) propose des statistiques de frame pour chaque frame de compositeur lorsqu’il atteint chaque cible. Le compositeur travaille régulièrement, ce qui peut se produire sur un vblank ou non. Cela signifie que si un affichage est dupliqué ou qu’un contenu est affiché à plusieurs endroits, l’application, l’infrastructure ou la télémétrie peut en tenir compte. Toutefois, ces frames de compositeur fournissent des informations incomplètes sur les trames qui ne sont pas composées, par exemple dans *iflip* (retournement indépendant) sur un utilise permutation.

À titre d’exemple d’utilisation, la nouvelle infrastructure de Media Foundation basée sur la composition utilise permutation s’appuie sur [**DCompositionGetStatistics**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongetstatistics) et [**DCompositionGetTargetStatistics**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongettargetstatistics) pour déterminer la qualité de présentation composée par télémétrie. En plus de cette API, ils appellent une API distincte lorsque leurs frames se trouvent dans iflip et ne sont pas dirigés vers le compositeur.

Pour certaines utilisations, les applications doivent utiliser [**IDCompositionDevice :: GetFrameStatistics**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-getframestatistics) pour recevoir une estimation de la prochaine trame de compositeur en vérifiant [**DCOMPOSITION_FRAME_STATISTICS :: nextEstimatedFrameTime**](/windows/win32/api/dcomptypes/ns-dcomptypes-dcomposition_frame_statistics).

Tout d’abord, l’application interroge la dernière image relative à l’état de la présentation du cadre par le biais de différentes expressions. L’application aura soit un *frameId* existant fourni par le utilise permutation de composition, soit des interfaces futures auxquelles il souhaite obtenir des informations, ou il peut appeler [**DCompositionGetFrameId**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongetframeid) pour récupérer les **COMPOSITION_FRAME_ID** les plus récentes du [**COMPOSITION_FRAME_ID_TYPE**](/windows/win32/api/dcomptypes/ne-dcomptypes-composition_frame_id_type)spécifié.

* **COMPOSITION_FRAME_ID_CREATED**. Le compositeur a commencé à travailler sur le frame.
* **COMPOSITION_FRAME_ID_CONFIRMED**. ID de frame dans lequel le travail de l’UC est terminé et tous les cadeaux ont eu lieu.
* **COMPOSITION_FRAME_ID_COMPLETED**. Le travail GPU est effectué pour toutes les cibles associées à un frame.

> [!NOTE]
> La **COMPOSITION_Frame_ID** est de plus en plus complexe. ainsi, les frames de compositeur précédents peuvent être déduites de celui-ci.

Ensuite, l’application recherche des informations de base sur le cadre de la composition et une liste des *targetID* qui font partie du cadre, en appelant [**DCompositionGetStatistics**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongetstatistics). Enfin, si l’application requiert des informations par cible, elle utilise [**DCompositionGetTargetStatistics**](/windows/win32/api/dcomp/nf-dcomp-dcompositiongettargetstatistics) pour récupérer des informations pour les FrameId et targetID spécifiés.

### <a name="c-example"></a>Exemple C++

L’exemple suivant montre une collection dynamique de statistiques de frame de l’API, qui est ensuite résumée dans la fonction **TargetFrameRate** pour déduire ce que la cadence était sur un ensemble de frames. Là encore, ce type de code est attendu dans les données de télémétrie ou dans les infrastructures, plutôt que dans une application.

```cpp
class FrameStatisticsCollector
{
private:
    // Collect at most 4 target monitors
    static constexpr UINT sc_maxTargetCount = 4;

    struct CompositionTargetStats
    {
        COMPOSITION_FRAME_ID frameId;
        COMPOSITION_FRAME_STATS frameStats;

        COMPOSITION_TARGET_ID targetId;
        COMPOSITION_TARGET_STATS targetStats;
    };

    UINT64 m_qpcFrequency;
    COMPOSITION_FRAME_ID m_lastCollectedFrameId = 0;
    std::vector<CompositionTargetStats> m_targetStats;

public:
    FrameStatisticsCollector()
    {
        QueryPerformanceFrequency(&m_qpcFrequency);
        m_lastCollectedFrameId = CurrentFrameId();
    }

    // Queries the compositor clock statistics API to determine the last frame
    // completed by the composition engine
    COMPOSITION_FRAME_ID CurrentFrameId() const
    {
        COMPOSITION_FRAME_ID frameId;
        if (FAILED(_DCompositionGetFrameId(frameIdType, &frameId)))
        {
            frameId = 0;
        }

        return frameId;
    }

    // Queries the system to get information about the latest composition frames
    void CollectStats()
    {
        COMPOSITION_FRAME_ID currentFrameId = CurrentFrameId(COMPOSITION_FRAME_ID_COMPLETED);

        while (m_active && (currentFrameId > m_endFrameId))
        {
            auto newEndFrameId = m_endFrameId + 1;

            COMPOSITION_FRAME_STATS frameStats = {};
            COMPOSITION_TARGET_ID targetIds[sc_maxTargetCount] = {};
            UINT targetCount;

            hr = _DCompositionGetStatistics(newEndFrameId,
                &frameStats,
                _countof(targetIds),
                targetIds,
                &targetCount);
            if (SUCCEEDED(hr))
            {
                // We track up to sc_maxTargetCount targets per frame
                targetCount = min<UINT>(targetCount, _countof(targetIds));

                for (UINT uIndex = 0; uIndex < targetCount; uIndex++)
                {
                    COMPOSITION_TARGET_STATS targetStats = {};
                    hr = DCompositionGetTargetStatistics(newEndFrameId,
                        &targetIds[uIndex],
                        &targetStats);
                    if (SUCCEEDED(hr))
                    {
                        CompositionTargetStats compTargetStats = { newEndFrameId,
                                                                  frameStats,
                                                                  targetIds[uIndex],
                                                                  targetStats };

                        m_compTargetStats.push_back(compTargetStats);
                    }
                    else
                    {
                        m_active = false;
                    }
                }

                m_endFrameId = newEndFrameId;
            }
            else
            {
                m_active = false;
            }
        }
    }

    // Compute the frame rate for the given composition target in frames per
    // second, over the specified frame interval based on historical statistics
    // data
    float TargetFrameRate(
        _const COMPOSITION_TARGET_ID& targetId,
        COMPOSITION_FRAME_ID beginFrameId,
        COMPOSITION_FRAME_ID endFrameId)  const
    {
        UINT frameCount = 0;
        UINT64 beginTime = 0;
        UINT64 endTime = 0;

        for (const auto& stats : m_compTargetStats)
        {
            if ((stats.frameId >= beginFrameId) && (stats.frameId <= endFrameId))
            {
                if (stats.frameId == beginFrameId)
                {
                    beginTime = stats.frameStats.startTime;
                }

                if (stats.frameId == endFrameId)
                {
                    endTime = stats.frameStats.startTime +
                        stats.frameStats.framePeriod;
                }

                if ((stats.targetId == targetId) &&
                    (stats.targetStats.presentTime != 0))
                {
                    frameCount++;
                }
            }
        }

        if ((beginTime != 0) &&
            (endTime != 0) &&
            (endTime > beginTime) &&
            (frameCount != 0))
        {
            auto seconds = static_cast<float>(endTime - beginTime) /
                static_cast<float>(m_qpcFrequency);

            return static_cast<float>(frameCount) / seconds;
        }
        else
        {
            return 0.0f;
        }
    }
};
```

## <a name="glossary"></a>Glossaire

* **Cible**. Bitmap dans laquelle le moteur de composition pixellise l’arborescence d’éléments visuels. Cette image bitmap est généralement un affichage.
* **Cadre de compositeur**. Un cycle de travail de compository &mdash; n’est pas nécessairement un vblank.
