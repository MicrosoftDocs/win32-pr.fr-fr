---
description: Les applications peuvent interroger le matériel pour détecter les types de périphériques Direct3D pris en charge. Cette section contient des informations sur les tâches principales impliquées dans l’énumération des adaptateurs d’affichage et la sélection des périphériques Direct3D.
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: Sélection d’un appareil (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63428e15948e15790364f310d55989a9bbc7339846f7db5d301e316bee4d872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044247"
---
# <a name="selecting-a-device-direct3d-9"></a>Sélection d’un appareil (Direct3D 9)

Les applications peuvent interroger le matériel pour détecter les types de périphériques Direct3D pris en charge. Cette section contient des informations sur les tâches principales impliquées dans l’énumération des adaptateurs d’affichage et la sélection des périphériques Direct3D.

Une application doit effectuer une série de tâches pour sélectionner un appareil Direct3D approprié. Notez que les étapes suivantes sont destinées à une application en plein écran et que, dans la plupart des cas, une application avec fenêtres peut ignorer la plupart de ces étapes.

1.  Au départ, l’application doit énumérer les adaptateurs d’affichage sur le système. Un adaptateur est un élément physique du matériel. Notez que la carte graphique peut contenir plusieurs adaptateurs, comme c’est le cas avec un affichage à deux pointes. Les applications qui ne sont pas concernées par la prise en charge de plusieurs moniteurs peuvent ignorer cette étape et passer D3DADAPTER \_ par défaut à la méthode [**IDirect3D9 :: EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) à l’étape 2.
2.  Pour chaque adaptateur, l’application énumère les modes d’affichage pris en charge en appelant [**IDirect3D9 :: EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).
3.  Si nécessaire, l’application vérifie la présence de l’accélération matérielle dans chaque mode d’affichage énuméré en appelant [**IDirect3D9 :: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), comme indiqué dans l’exemple de code suivant. Notez qu’il ne s’agit que d’une des utilisations possibles de **IDirect3D9 :: CheckDeviceType**; Pour plus d’informations, consultez Détermination de la [prise en charge matérielle (Direct3D 9)](determining-hardware-support.md).
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    Params.BackBufferFormat = D3DFMT_X1R5G5B5; 

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, 
                      Device.m_DevType, 
                      Params.BackBufferFormat, Params.BackBufferFormat, 
                      FALSE))) 
        return E_FAIL;
    ```

    

4.  L’application vérifie le niveau de fonctionnalité souhaité pour l’appareil sur cet adaptateur en appelant la méthode [**IDirect3D9 :: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) . La fonctionnalité retournée par cette méthode est toujours constante pour un appareil dans tous les modes d’affichage, vérifiée par [**IDirect3D9 :: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).
5.  Les appareils peuvent toujours effectuer un rendu sur des surfaces du format d’un mode d’affichage énuméré qui est pris en charge par l’appareil. Si l’application doit effectuer un rendu sur une surface d’un autre format, elle peut appeler [**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat). Si l’appareil peut effectuer un rendu au format, il est garanti que toutes les fonctionnalités retournées par [**IDirect3D9 :: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) sont applicables.
6.  Enfin, l’application peut déterminer si les techniques d’échantillonnage multiple, telles que l’anticrénelage de scène complète, sont prises en charge pour un format de rendu à l’aide de la méthode [**IDirect3D9 :: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) .

Une fois les étapes précédentes terminées, l’application doit disposer d’une liste de modes d’affichage dans laquelle elle peut fonctionner. La dernière étape consiste à vérifier que suffisamment de mémoire accessible par l’appareil est disponible pour prendre en charge le nombre requis de mémoires tampons et l’anticrénelage. Ce test est nécessaire car la consommation de mémoire pour le mode et la combinaison d’exemples est impossible à prédire sans le vérifier. De plus, certaines architectures d’adaptateur d’affichage peuvent ne pas disposer d’une quantité constante de mémoire accessible à l’appareil. Cela signifie qu’une application doit être en mesure de signaler des échecs de mémoire non vidéo lors du passage en mode plein écran. En règle générale, une application doit supprimer le mode plein écran de la liste des modes qu’elle offre à un utilisateur, ou elle doit tenter de consommer moins de mémoire en réduisant le nombre de mémoires tampons d’arrière-plan ou en utilisant une technique d’échantillonnage multiple moins complexe.

Une application avec fenêtres exécute un ensemble de tâches similaire.

1.  Elle détermine le rectangle du bureau couvert par la zone cliente de la fenêtre.
2.  Il énumère les adaptateurs, en recherchant l’adaptateur dont le moniteur couvre la zone cliente. Si la zone cliente appartient à plusieurs adaptateurs, l’application peut choisir de piloter chaque carte indépendamment, ou de piloter une seule carte et de transférer Direct3D des pixels d’un appareil à l’autre lors de la présentation. L’application peut également ignorer deux étapes précédentes et utiliser l' \_ adaptateur par défaut D3DADAPTER. Notez que cela peut entraîner une opération plus lente lorsque la fenêtre est placée sur un moniteur secondaire.
3.  L’application doit appeler [**IDirect3D9 :: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) pour déterminer si l’appareil peut prendre en charge le rendu d’une mémoire tampon d’arrière-plan au format spécifié en mode Bureau. [**IDirect3D9 :: GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) peut être utilisé pour déterminer le format d’affichage du bureau, comme indiqué dans l’exemple de code suivant.
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    // Use the current display mode.
    D3DDISPLAYMODE mode;

    if(FAILED(m_pD3D->GetAdapterDisplayMode(Device.m_uAdapter , &mode)))
        return E_FAIL;

    Params.BackBufferFormat = mode.Format;

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, Device.m_DevType, 
    Params.BackBufferFormat, Params.BackBufferFormat, FALSE)))
        return E_FAIL;
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
