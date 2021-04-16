---
title: Enregistrement multimédia
description: Enregistrement multimédia
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- MCIWndCreate fonction)
- MCIWndNew macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379909"
---
# <a name="multimedia-recording"></a>Enregistrement multimédia

Vous pouvez implémenter des fonctionnalités d’enregistrement dans votre application à l’aide de l’interface utilisateur intégrée à MCIWnd. Vous pouvez utiliser la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) et la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) pour fournir des contrôles permettant de démarrer et d’arrêter l’enregistrement et d’enregistrer les informations enregistrées. À l’aide de **MCIWndCreate**, vous pouvez spécifier des styles de fenêtre pour afficher une fenêtre MCIWnd et inclure le bouton **Enregistrer** dans la barre d’outils. À l’aide de **MCIWndNew**, vous pouvez spécifier le type d’appareil en cours d’enregistrement et spécifier que les informations doivent être capturées dans un nouveau fichier.

Si votre application nécessite une plus grande sophistication, vous pouvez automatiser et personnaliser l’enregistrement à l’aide de la macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) . Pour plus d’informations, consultez [Personnalisation du processus d’enregistrement](customizing-the-recording-process.md).

> [!Note]  
> Certains périphériques, tels que les CD audio et MCIAVI, sont utilisés uniquement pour la lecture. D’autres périphériques, tels que les périphériques audio Waveform, peuvent être utilisés pour l’enregistrement. Si vous spécifiez un appareil qui ne peut pas être enregistré, MCIWnd omet le bouton **Enregistrer** dans la barre d’outils.

 

 

 




