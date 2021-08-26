---
title: Interfaces de la couche de débogage
description: Les interfaces suivantes sont déclarées dans d3d12sdklayers. h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d7e16d6c593f2dcfcc46266102ac15a61386ef
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812880"
---
# <a name="debug-layer-interfaces"></a>Interfaces de couche de débogage

Les interfaces suivantes sont définies dans `d3d12sdklayers.h` .

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**ID3D12Debug**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Une interface de débogage contrôle les paramètres de débogage et valide l’état du pipeline. Elle ne peut être utilisée que si la couche de débogage est activée. |
| [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | Ajoute la validation basée sur GPU et la synchronisation de la file d’attente de commandes dépendante à la couche de débogage. |
| [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | Ajoute des niveaux configurables de GPU-Based validation. |
| [**ID3D12Debug3**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | Ajoute à la couche de débogage la validation basée sur GPU, à la synchronisation de la file d’attente des commandes dépendante et aux niveaux configurables de validation basée sur GPU. |
| [**ID3D12Debug4**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug4) | Ajoute la possibilité de désactiver la couche de débogage. |
| [**ID3D12Debug5**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug5) | Ajoute à la couche de débogage la possibilité de configurer le nommage automatique des objets. |
| [**ID3D12DebugCommandList**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | Fournit des méthodes pour surveiller et déboguer une liste de commandes. |
| [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | Cette interface permet de modifier les paramètres de couche de débogage de la liste de commandes supplémentaires. |
| [**ID3D12DebugCommandQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | Fournit des méthodes pour surveiller et déboguer une file d’attente de commandes. |
| [**ID3D12DebugDevice**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | Cette interface représente un périphérique graphique pour le débogage. |
| [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | Spécifie les paramètres de la couche de débogage au niveau de l’appareil. |
| [**ID3D12InfoQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | Une interface d’informations de file d’attente stocke, récupère et filtre les messages de débogage. La file d’attente se compose d’une file d’attente de messages, d’une pile de filtres de stockage facultative et d’une pile de filtres de récupération facultative. |
| [**ID3D12SharingContract**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | Partie d’un contrat entre les couches de diagnostic D3D11On12 et les outils de diagnostic graphique. |

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’environnement de programmation Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Référence de la couche de débogage](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Référence de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>