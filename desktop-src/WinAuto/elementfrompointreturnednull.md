---
title: ElementFromPointReturnedNull
description: ElementFromPointReturnedNull
ms.assetid: DBCA6705-BDFD-4024-A505-4539F72A9421
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde128b0865d24ea41270665a7b9592355a68d5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511647"
---
# <a name="elementfrompointreturnednull"></a>ElementFromPointReturnedNull

## <a name="text"></a>Texte

IUIAutomation. ElementFromPoint ( {0} , {1} ) a retourné la valeur null

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

L’adresse de l’objet [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de l’élément d’interface utilisateur obtenu pour les coordonnées données a la valeur null.

## <a name="possible-causes"></a>Causes possibles

-   L’interaction de l’utilisateur pendant la vérification, telle que le déplacement du focus vers un HWND non cible, interfère avec le processus de vérification.
-   Implémentation d’UI Automation incorrecte ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




