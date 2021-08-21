---
title: UiaElementIsOrphaned
description: UiaElementIsOrphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940e1242be2b0393023bc83b31cc662a52677c59307dff01fed30d8319604d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118827395"
---
# <a name="uiaelementisorphaned"></a>UiaElementIsOrphaned

## <a name="text"></a>Texte

L’élément est un AutomationElement orphelin dans l’arborescence

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

L’adresse de l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de l’objet obtenue pour les coordonnées données est une référence à un élément orphelin dans l’arborescence d’éléments.

Ce problème est un problème pour les personnes qui s’appuient sur un lecteur d’écran et un clavier pour la navigation, car les éléments sont traités comme invisibles et ne sont pas annoncés à l’utilisateur.

## <a name="possible-causes"></a>Causes possibles

-   L’interaction de l’utilisateur pendant la vérification, telle que le déplacement du focus vers un HWND non cible, interfère avec le processus de vérification.
-   Implémentation d’UI Automation incorrecte ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IUIAutomationElement.ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




