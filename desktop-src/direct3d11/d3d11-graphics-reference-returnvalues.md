---
title: Codes de retour Direct3D 11
description: Codes de retour des fonctions API.
ms.assetid: c0856a58-b760-44e5-8acf-145720b403d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d932c3ce3828f375e90bf322af6c42dc112b845f44dfe22f0d0988930129efea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990039"
---
# <a name="direct3d-11-return-codes"></a>Codes de retour Direct3D 11

Codes de retour des fonctions API.

| HRESULT | Description |
|-|-|
| D3D11_ERROR_FILE_NOT_FOUND (0x887C0002) | Ce fichier est introuvable. |
| D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS (0x887C0001) | Le nombre d’instances uniques d’un type particulier d’objet d’État est trop important. |
| D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS (0x887C0003) | Le nombre d’instances uniques d’un type particulier d’objet d’affichage est trop important. |
| D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD (0x887C0004) | Le premier appel à [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) après [**ID3D11Device :: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext) ou [**ID3D11DeviceContext :: FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) par ressource n’a pas été D3D11_MAP_WRITE_DISCARD. |
| D3DERR_INVALIDCALL (remplacé par DXGI_ERROR_INVALID_CALL) (0x887A0001) | L’appel de la méthode n’est pas valide. Par exemple, le paramètre d’une méthode peut ne pas être un pointeur valide. |
| D3DERR_WASSTILLDRAWING (remplacé par DXGI_ERROR_WAS_STILL_DRAWING) (0x887A000A) | L’opération blit précédente qui transfère des informations vers ou à partir de cette surface est incomplète. |
| E_FAIL (0x80004005) | Tentative de création d’un appareil avec la couche de débogage activée et la couche n’est pas installée. |
| E_INVALIDARG (0x80070057) | Un paramètre non valide a été passé à la fonction retournée. |
| E_OUTOFMEMORY (0x8007000E) | Direct3D n’a pas pu allouer suffisamment de mémoire pour terminer l’appel. |
| E_NOTIMPL (0x80004001) | L’appel de méthode n’est pas implémenté avec la combinaison de paramètres passée. |
| S_FALSE (HRESULT) 1L) | Autre valeur de réussite, indiquant une saisie semi-automatique réussie mais non standard (la signification précise dépend du contexte). |
| S_OK (HRESULT) 0L) | Aucune erreur ne s'est produite. |

Pour plus d’informations sur les codes de retour, consultez [DXGI_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).

## <a name="related-topics"></a>Rubriques connexes

* [Référence de Direct3D 11](d3d11-graphics-reference.md)