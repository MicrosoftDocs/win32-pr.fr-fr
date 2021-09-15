---
title: Paramètre d’animation de la zone client
description: L’indicateur d’animation de la zone cliente indique si l’utilisateur souhaite désactiver les animations dans les éléments d’interface utilisateur.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520916"
---
# <a name="client-area-animation-parameter"></a>Paramètre d’animation de la zone client

Le paramètre d’animation de la zone cliente indique si l’utilisateur souhaite désactiver les animations dans les éléments d’interface utilisateur. Les fonctionnalités d’affichage telles que le clignotement, le clignotement, le scintillement et le déplacement de contenu peuvent entraîner des crises chez les utilisateurs avec une épilepsie photosensible. Ce paramètre vous permet d’activer ou de désactiver toutes les animations de ce type.

Les applications utilisent les indicateurs **SPI \_ GETCLIENTAREAANIMATION** et **SPI \_ SETCLIENTAREAANIMATION** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour activer ou désactiver les animations de la zone cliente.

 

 