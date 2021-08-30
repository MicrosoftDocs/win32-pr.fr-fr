---
title: Fourniture de mises à jour d’État
description: Fourniture de mises à jour d’État
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- MCIWndSetActiveTimer macro)
- MCIWndSetInactiveTimer macro)
- MCIWndGetActiveTimer macro)
- MCIWndGetInactiveTimer macro)
- MCIWndSetTimers macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71ad60ce3970c21adec75af04f3c896eef4c933816002bc8b4c8c3acabcd5a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037579"
---
# <a name="providing-status-updates"></a>Fourniture de mises à jour d’État

MCIWnd utilise des minuteries pour mettre régulièrement à jour les informations dans la barre de titre et la barre de défilement de la fenêtre, et pour envoyer des messages de notification à la fenêtre parente. Une minuterie contrôle la période de mise à jour de la fenêtre active MCIWnd et une deuxième minuterie contrôle la période de mise à jour pour les fenêtres MCIWnd qui sont inactives. Votre application peut utiliser les macros du minuteur MCIWnd pour récupérer les paramètres du minuteur en cours et ajuster les périodes de mise à jour.

Vous pouvez définir la période de mise à jour utilisée par le minuteur de fenêtre active à l’aide de la macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) . Cette macro définit la période utilisée par MCIWnd pour mettre à jour la barre de suivi, pour mettre à jour la position de lecture indiquée dans la barre de titre de la fenêtre et pour informer la fenêtre parente que le média a changé. Vous pouvez récupérer la période de mise à jour actuelle utilisée par le minuteur de fenêtre active à l’aide de la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) . La période de mise à jour par défaut du minuteur de fenêtre active est de 500 millisecondes.

Vous pouvez définir la période de mise à jour utilisée par le minuteur de fenêtre inactive à l’aide de la macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) . Cette macro définit la période utilisée par MCIWnd pour mettre à jour la barre de suivi, pour mettre à jour la position de lecture signalée dans le titre de la fenêtre et pour informer la fenêtre parent que le média a changé. Vous pouvez récupérer la période de mise à jour actuelle utilisée par le minuteur de fenêtre inactive à l’aide de la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) . La période de mise à jour par défaut du minuteur de fenêtre inactive est de 2000 millisecondes.

Votre application peut définir simultanément la période de mise à jour pour les deux minuteurs à l’aide de la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) . Le stockage de la valeur de la période de mise à jour est limité à 16 bits. Si vous avez besoin d’une quantité plus importante pour une période de mise à jour, définissez les minuteries individuellement.

 

 




