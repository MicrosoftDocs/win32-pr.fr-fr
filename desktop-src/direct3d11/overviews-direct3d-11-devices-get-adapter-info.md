---
title: Obtention des modes d’affichage de l’adaptateur
description: Cette rubrique montre comment utiliser Microsoft DirectX Graphics infrastructure (DXGI) pour obtenir les modes d’affichage valides associés à un adaptateur.
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921d373a9ff0f79baaf848a55cbab0d08fd4e119d30a0a0cb917832830589dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119569"
---
# <a name="how-to-get-adapter-display-modes"></a>Comment : obtenir les modes d’affichage de l’adaptateur

Cette rubrique montre comment utiliser Microsoft DirectX Graphics infrastructure (DXGI) pour obtenir les modes d’affichage valides associés à un adaptateur. DirectX 10 et 11 peuvent utiliser DXGI pour obtenir les modes d’affichage valides. Le fait de connaître les modes d’affichage valides garantit que votre application peut choisir correctement un mode plein écran valide.

**Pour obtenir les modes d’affichage de l’adaptateur**

1.  Créez un objet [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) et utilisez-le pour énumérer les adaptateurs disponibles. Pour plus d’informations, consultez [Comment : énumérer des adaptateurs](overviews-direct3d-11-devices-enum.md).
2.  Appelez IDXGIAdapter :: EnumOutputs pour énumérer les sorties de chaque adaptateur.
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  Appelez IDXGIOutput :: GetDisplayModeList pour récupérer un tableau de [**structures \_ \_ desc en mode dxgi**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) et le nombre d’éléments dans le tableau. Chaque **structure \_ \_ desc mode dxgi** représente un mode d’affichage valide pour la sortie.
    ```
    UINT numModes = 0;
    DXGI_MODE_DESC* displayModes = NULL;
    DXGI_FORMAT format = DXGI_FORMAT_R32G32B32A32_FLOAT;

        // Get the number of elements
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, NULL);

        displayModes = new DXGI_MODE_DESC[numModes]; 

        // Get the list
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, displayModes);
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appareils](overviews-direct3d-11-devices.md)
</dt> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 