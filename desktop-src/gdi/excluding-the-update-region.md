---
description: La fonction ExcludeUpdateRgn exclut la région de mise à jour de la zone de découpage pour le contexte de périphérique d’affichage.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Exclusion de la région de mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531340"
---
# <a name="excluding-the-update-region"></a>Exclusion de la région de mise à jour

La fonction [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) exclut la région de mise à jour de la zone de découpage pour le contexte de périphérique d’affichage. Cette fonction est utile lors du dessin dans une fenêtre autre que lors du \_ traitement d’un message de peinture WM. Il empêche le dessin dans les zones qui seront mises à jour pendant le prochain \_ message de peinture WM.

 

 



