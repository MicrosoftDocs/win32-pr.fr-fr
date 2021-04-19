---
description: Le tableau suivant contient les codes de retour des fonctions API.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Codes de retour Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2fcdc4db5bd2d295b7cd3078ed80d401ce52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514929"
---
# <a name="direct3d-10-return-codes"></a>Codes de retour Direct3D 10

Le tableau suivant contient les codes de retour des fonctions API.



| HRESULT                                         | Description                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Fichier d’erreur D3D10 \_ \_ \_ introuvable                  | Ce fichier est introuvable.                                                                                                                               |
| \_Erreur D3D10 \_ \_ un trop grand nombre d’objets d' \_ \_ État uniques \_ | Le nombre d’instances uniques d’un type particulier d' [objet d’État](d3d10-graphics-programming-guide-api-features-state-objects.md)est trop important.          |
| D3DERR \_ INVALIDCALL                             | L’appel de la méthode n’est pas valide. Par exemple, le paramètre d’une méthode peut ne pas être un pointeur valide.                                                             |
| D3DERR \_ WASSTILLDRAWING                         | L’opération blit précédente qui transfère des informations vers ou à partir de cette surface est incomplète.                                                   |
| E \_ échec                                         | Tentative de création d’un appareil avec la [couche de débogage](d3d10-graphics-programming-guide-api-features-layers.md) activée et la couche n’est pas installée. |
| E \_ INVALIDARG                                   | Un paramètre non valide a été passé à la fonction retournée.                                                                                            |
| \_OUTOFMEMORY E                                  | Direct3D n’a pas pu allouer suffisamment de mémoire pour terminer l’appel.                                                                                   |
| \_NOTIMPL E                                      | L’appel de méthode n’est pas implémenté avec la combinaison de paramètres passée.                                                                              |
| S \_ false                                        | Autre valeur de réussite, indiquant une saisie semi-automatique réussie mais non standard (la signification précise dépend du contexte).                                 |
| \_OK                                           | Aucune erreur ne s'est produite.                                                                                                                                    |



 

Pour écrire du code qui gère les [valeurs HRESULT](../winprog/windows-data-types.md) de façon fiable, utilisez les macros SUCCEEDED (HR) et failed (HR).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[Référence pour Direct3D 10](d3d10-graphics-reference.md)
</dt> </dl>

 

 
