---
title: Codes de retour Direct3D 12
description: Voici les codes de retour des fonctions API.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba58a72fa3cbb22b69cf4a31fb3ac88ce2b6b47cac3f0e334db4ec86dfd8e0f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098331"
---
# <a name="direct3d-12-return-codes"></a>Codes de retour Direct3D 12

Voici les codes de retour des fonctions API. Pour plus d’informations sur les codes de retour, consultez [ \_ erreur dxgi](/windows/desktop/direct3ddxgi/dxgi-error).



| HRESULT                                                                  | Description                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| \_Adaptateur d’erreur D3D12 \_ \_ \_ introuvable                                        | Le PSO mis en cache spécifié a été créé sur un autre adaptateur et ne peut pas être réutilisé sur l’adaptateur actuel.          |
| Incompatibilité de version de pilote d' \_ erreur D3D12 \_ \_ \_                                  | Le PSO mis en cache spécifié a été créé sur une version de pilote différente et ne peut pas être réutilisé sur l’adaptateur actuel.  |
| D3DERR \_ INVALIDCALL (remplacé par une \_ erreur \_ dxgi \_ appel non valide)           | L’appel de la méthode n’est pas valide. Par exemple, le paramètre d’une méthode peut ne pas être un pointeur valide.                             |
| D3DERR \_ WASSTILLDRAWING (remplacé par l' \_ erreur \_ dxgi \_ \_ dessinait encore) | L’opération blit précédente qui transfère des informations vers ou à partir de cette surface est incomplète.                   |
| E \_ échec                                                                  | Tentative de création d’un appareil avec la couche de débogage activée et la couche n’est pas installée.                             |
| E \_ INVALIDARG                                                            | Un paramètre non valide a été passé à la fonction retournée.                                                             |
| \_OUTOFMEMORY E                                                           | Direct3D n’a pas pu allouer suffisamment de mémoire pour terminer l’appel.                                                   |
| \_NOTIMPL E                                                               | L’appel de méthode n’est pas implémenté avec la combinaison de paramètres passée.                                               |
| S \_ false                                                                 | Autre valeur de réussite, indiquant une saisie semi-automatique réussie mais non standard (la signification précise dépend du contexte). |
| \_OK                                                                    | Aucune erreur ne s'est produite.                                                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 