---
title: Utiliser ordinateur pour diagnostiquer les erreurs GPU
description: Le ordinateur (Device removed Extended Data) est un ensemble évolutif de fonctionnalités de diagnostic conçues pour vous aider à identifier la cause des erreurs de suppression de périphérique inattendues.
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 795ecaf464728388c33f55655ff81d29068956ca
ms.sourcegitcommit: 9942a888f172981e276def0c6b84fb0266fcb02d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2021
ms.locfileid: "123399805"
---
# <a name="use-dred-to-diagnose-gpu-faults"></a>Utiliser ordinateur pour diagnostiquer les erreurs GPU
ORDINATEUR correspond aux données étendues supprimées de l’appareil. ORDINATEUR est un ensemble évolutif de fonctionnalités de diagnostic conçues pour vous aider à identifier la cause des erreurs de suppression de périphérique inattendues. Sur le matériel qui prend en charge les fonctionnalités nécessaires (comme indiqué ci-dessous), ordinateur fournit des plans de navigation automatiques et des rapports de défaillance de page GPU.

## <a name="auto-breadcrumbs"></a>Barres de navigation automatiques
Pour définir la scène des plans de navigation automatiques, commençons par mentionner la variété manuelle. En prévision de l’éventualité d’un délai d' [expiration de la détection et de la récupération (TDR)](/windows-hardware/drivers/display/timeout-detection-and-recovery), vous pouvez utiliser la [méthode ID3D12GraphicsCommandList2 :: WriteBufferImmediate](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate) pour placer le *Breadcrumb* dans le flux de commandes GPU, afin d’effectuer le suivi de la progression du GPU.

Il s’agit d’une approche raisonnable si vous souhaitez créer une implémentation personnalisée et à faible surcharge. toutefois, il peut manquer une certaine polyvalence d’une solution standardisée, telle que les extensions de débogueur ou la création de rapports via [Rapport d’erreurs Windows (WER)](/windows/desktop/wer/windows-error-reporting) (également appelée Watson).

Ainsi, les breadcrumbs automatiques de ordinateur appellent **WriteBufferImmediate** pour placer des compteurs de progression dans le flux de commandes GPU. ORDINATEUR insère un fil d’Ariane après chaque opération de *rendu*, &mdash; ce qui signifie que toutes les opérations qui entraînent le fonctionnement de GPU (par exemple, **dessin**, **Dispatch**, **copie**, **résolution** et autres). Si l’appareil est supprimé au milieu d’une charge de travail GPU, la valeur de Breadcrumb ordinateur est essentiellement une collection des opérations de rendu qui se sont terminées avant l’erreur.

La mémoire tampon en anneau de l’historique du plan de navigation conserve les opérations 64KiB dans une liste de commandes donnée. S’il y a plus de 65536 opérations dans une liste de commandes, seules les dernières opérations 64KiB sont stockées en &mdash; remplaçant d’abord les opérations les plus anciennes. Toutefois, la valeur du compteur de navigation continue à compter jusqu’à `UINT_MAX` . Par conséquent, LastOpIndex = (BreadcrumbCount-1) %65536.

ordinateur 1,0 était d’abord disponible en Windows 10, version 1809 (Mise à jour d’octobre 2018 de Windows 10) et il exposait des plans de navigation automatiques rudimentaires. Toutefois, il n’y avait pas d’API pour celle-ci, et la seule façon d’activer ordinateur 1,0 consistait à utiliser le **Hub de commentaires** pour capturer une reproduction TDR (repro) pour les **applications &** les \> **performances et la compatibilité du jeu** de jeux. L’objectif principal de ordinateur 1,0 était d’aider à analyser les défaillances de jeu à l’aide des commentaires des clients.
### <a name="caveats"></a>Mises en garde
- Comme un GPU est fortement canalisé, il n’est pas garanti que le compteur de navigation indique l’opération exacte qui a échoué. En fait, sur certains appareils de rendu différés basés sur des vignettes, il est possible que le compteur de navigation soit une ressource complète ou une barrière d’affichage d’accès non ordonné (UAV) derrière la progression réelle du GPU.
- Un pilote d’affichage peut réorganiser les commandes, prérécupérer à partir de la mémoire des ressources avant d’exécuter une commande ou vider la mémoire mise en cache correctement après l’achèvement d’une commande. L’une d’entre elles peut générer une erreur GPU. Dans ce cas, les compteurs de navigation automatique peuvent être moins utiles ou trompeurs.
### <a name="performance"></a>Performances
Bien que les barres de navigation automatiques soient conçues pour être à faible charge, elles ne sont pas gratuites. Les mesures empiriques montrent une baisse de 2-5% des performances sur un moteur de jeu graphique AAA Direct3D 12 classique. Pour cette raison, les barres de navigation automatiques sont désactivées par défaut.
### <a name="hardware-requirements"></a>Configuration matérielle requise
Étant donné que les valeurs de compteur de navigation doivent être conservées après la suppression de l’appareil, la ressource qui contient des plans de navigation doit exister dans la mémoire système et doit être conservée en cas de suppression de l’appareil. Cela signifie que le pilote d’affichage doit prendre en charge [**D3D12_FEATURE_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature). heureusement, c’est le cas pour la plupart des pilotes d’affichage Direct3D 12 sur Windows 10, version 1903.
## <a name="gpu-page-fault-reporting"></a>Rapport d’erreurs de page GPU
Une fonctionnalité qui est nouvelle pour ordinateur 1,1 est la création de rapports d’erreurs de pages GPU ordinateur. Une erreur de page GPU se produit généralement dans l’une de ces conditions.

1. Une application exécute par erreur le travail sur le GPU qui fait référence à un objet supprimé. C’est l’une des principales raisons de la suppression d’un appareil inattendu.
2. Une application exécute par erreur un travail sur le GPU qui accède à une ressource expulsée ou une vignette non résidente.
3. Un nuanceur fait référence à un descripteur non initialisé ou périmé.
3. Index de nuanceur au-delà de la fin d’une liaison racine.

ORDINATEUR tente de traiter certains de ces scénarios en signalant les noms et les types des objets API existants ou récemment libérés qui correspondent à l’adresse virtuelle (VA) de l’erreur de page signalée par le GPU.

### <a name="caveat"></a>Mise en garde
Tous les processeurs graphiques ne prennent pas en charge les défauts de page (bien que de nombreuses tâches). Certains GPU répondent aux erreurs de mémoire par : les écritures de compartiment binaire ; lecture des données simulées (par exemple, des zéros); ou simplement en suspens. Malheureusement, dans les cas où le GPU ne se bloque pas immédiatement, une [détection et une récupération du délai d’attente (TDR)](/windows-hardware/drivers/display/timeout-detection-and-recovery) peuvent se produire plus tard dans le canal, ce qui rend encore plus difficile la localisation de la cause racine.

### <a name="performance"></a>Performances
Le runtime Direct3D 12 doit activement organiser une collection d’objets API existants et récemment supprimés indexables par adresse virtuelle (VA). Cela augmente la surcharge de mémoire système et introduit un faible impact sur les performances de la création et de la destruction d’objets. Pour cette raison, ce comportement est désactivé par défaut.

### <a name="hardware-requirements"></a>Configuration matérielle requise
Un GPU qui ne prend pas en charge la défaillance de page peut toujours tirer parti de la fonctionnalité de plans de navigation automatique.

## <a name="setting-up-dred-in-code"></a>Configuration de ordinateur dans le code
Les paramètres ordinateur sont globaux pour le processus et vous devez les configurer avant de créer un appareil Direct3D 12. Pour ce faire, appelez la fonction [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) pour récupérer un [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings).

```cpp
CComPtr<ID3D12DeviceRemovedExtendedDataSettings> pDredSettings;
VERIFY_SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&pDredSettings)));

// Turn on auto-breadcrumbs and page fault reporting.
pDredSettings->SetAutoBreadcrumbsEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
pDredSettings->SetPageFaultEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
```

> [!NOTE]
> Les modifications apportées aux paramètres de ordinateur n’ont aucun effet sur les appareils déjà créés. Toutefois, les appels suivants à [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) utilisent les paramètres ordinateur les plus récents.

## <a name="accessing-dred-data-in-code"></a>Accès aux données ordinateur dans le code
Une fois la suppression de l’appareil détectée (par exemple, la **présence** de retourne [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/com/com-error-codes-10)), utilisez les méthodes de l’interface [**ID3D12DEVICEREMOVEDEXTENDEDDATA**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) pour accéder aux données ordinateur pour l’appareil supprimé.

Pour récupérer l’interface **ID3D12DeviceRemovedExtendedData** , appelez [QueryInterface](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) sur une interface [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) (ou dérivée), en passant l’identificateur d’interface (IID) de **ID3D12DeviceRemovedExtendedData**.

```cpp
void MyDeviceRemovedHandler(ID3D12Device * pDevice)
{
    CComPtr<ID3D12DeviceRemovedExtendedData> pDred;
    VERIFY_SUCCEEDED(pDevice->QueryInterface(IID_PPV_ARGS(&pDred)));
    D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT DredAutoBreadcrumbsOutput;
    D3D12_DRED_PAGE_FAULT_OUTPUT DredPageFaultOutput;
    VERIFY_SUCCEEDED(pDred->GetAutoBreadcrumbsOutput(&DredAutoBreadcrumbsOutput));
    VERIFY_SUCCEEDED(pDred->GetPageFaultAllocationOutput(&DredPageFaultOutput));
    // Custom processing of DRED data can be done here.
    // Produce telemetry...
    // Log information to console...
    // break into a debugger...
}
```

## <a name="debugger-access-to-dred"></a>Accès au débogueur à ordinateur
Les débogueurs ont accès aux données ordinateur via **d3d12 !** Exportation de données D3D12DeviceRemovedExtendedData.

## <a name="dred-telemetry"></a>Télémétrie ordinateur
Votre application peut utiliser les API ordinateur pour contrôler les fonctionnalités de ordinateur et collecter les données de télémétrie pour faciliter l’analyse des problèmes. Cela vous donne un net bien plus large pour détecter les TDRs difficiles à reproduire.

à partir de Windows 10, la version 1903, tous les événements de retrait de périphérique en mode utilisateur sont signalés à [Rapport d’erreurs Windows (WER)](/windows/desktop/wer/windows-error-reporting), également appelé Watson. Si une combinaison particulière de l’application, du GPU et du pilote d’affichage génère un nombre suffisant d’événements supprimés par l’appareil, il est possible que ordinateur soit temporairement activé pour les clients lançant la même application sur une configuration similaire.
