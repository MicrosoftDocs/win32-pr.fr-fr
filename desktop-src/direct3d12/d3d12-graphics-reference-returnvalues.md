---
title: Codes de retour Direct3D 12
description: Voici les codes de retour des fonctions API.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513544"
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

 

 