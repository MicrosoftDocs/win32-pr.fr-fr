---
title: Valeurs de retour de test de positionnement
description: Cette section répertorie les valeurs de code de test de positionnement qui sont retournées dans le paramètre pwHitTestCode de la fonction HitTestThemeBackground.
ms.assetid: 95b4fc1a-2f9b-4464-b672-552d36b60c42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219cb59115bae56ac6cc3ba7f05384c331969b34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029050"
---
# <a name="hit-test-return-values"></a>Valeurs de retour de test de positionnement

Cette section répertorie les valeurs de code de test de positionnement qui sont retournées dans le paramètre *pwHitTestCode* de la fonction [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) . Les valeurs de code retournées dépendent des options de test de positionnement spécifiées dans le paramètre *dwOptions* de la fonction **HitTestThemeBackground** . Pour obtenir la liste des options, consultez [options de test de positionnement](theme-hit-test-options.md).

## <a name="return-values"></a>Valeurs de retour

Le tableau suivant répertorie les options de test de positionnement et les codes de retour correspondants.



| Option                       | Codes de retour  | Description                                                                                                        |
|------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | HTBOTTOM      | Le test d’atteinte a réussi dans le segment de bordure inférieur.                                                                   |
|                              | HTBOTTOMLEFT  | Le test d’atteinte a réussi dans l’intersection des bordures inférieure et gauche.                                                     |
|                              | HTBOTTOMRIGHT | Le test d’atteinte a réussi dans l’intersection des bordures inférieure et droite.                                                    |
|                              | HTCLIENT      | Le test d’atteinte a réussi dans le segment d’arrière-plan central.                                                               |
|                              | HTLEFT        | Le test d’atteinte a réussi dans le segment de bordure gauche.                                                                     |
|                              | HTNOWHERE     | Le test d’atteinte a réussi en dehors du contrôle ou sur une zone transparente.                                                   |
|                              | HTRIGHT       | Le test d’atteinte a réussi dans le segment de bordure droit.                                                                    |
|                              | HTTOP         | Le test d’atteinte a réussi dans le segment de bordure supérieur.                                                                      |
|                              | HTTOPLEFT     | Le test d’atteinte a réussi dans l’intersection des bordures supérieure et gauche.                                                            |
|                              | HTTOPRIGHT    | Le test d’atteinte a réussi dans l’intersection des bordures supérieure et droite.                                                       |
| \_légende HTTB                | HTCAPTION     | Le test d’atteinte a réussi dans les segments d’arrière-plan supérieur, supérieur gauche ou supérieur droit.                                         |
|                              | HTNOWHERE     | Le test d’atteinte a réussi en dehors du contrôle ou sur une zone transparente.                                                   |
| HTTB \_ FIXEDBORDER            | HTBORDER      | Test d’atteinte réussi dans un segment d’arrière-plan, à l’exception du segment d’arrière-plan central.                                 |
|                              | HTCLIENT      | Le test d’atteinte a réussi dans le segment d’arrière-plan central.                                                               |
| HTTB \_ RESIZINGBORDER         | HTBORDER      | Le test d’atteinte a échoué dans le segment d’arrière-plan central et les zones de redimensionnement, mais réussissent dans un segment de bordure d’arrière-plan. |
| HTTB \_ RESIZINGBORDER \_ bas | HTBOTTOM      | Le test d’atteinte a réussi dans le segment de bordure inférieur.                                                                   |
| HTTB \_ RESIZINGBORDER \_ gauche   | HTLEFT        | Le test d’atteinte a réussi dans le segment de bordure gauche.                                                                     |
| HTTB \_ RESIZINGBORDER \_ Right  | HTRIGHT       | Le test d’atteinte a réussi dans le segment de bordure droit.                                                                    |
| HTTB \_ RESIZINGBORDER \_ Top    | HTTOP         | Le test d’atteinte a réussi dans le segment de bordure supérieur.                                                                      |



 

 

 




