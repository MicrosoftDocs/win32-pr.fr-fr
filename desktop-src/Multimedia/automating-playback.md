---
title: Automatisation de la lecture
description: Automatisation de la lecture
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- MCIWndCreate macro)
- MCIWndPlay macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007250"
---
# <a name="automating-playback"></a>Automatisation de la lecture

Vous pouvez automatiser la lecture dans votre application à l’aide de [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) et de la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , ainsi que de la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) ou [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) . Pour automatiser la lecture, spécifiez les \_ styles MCIWNDF NOPLAYBAR et MCIWNDF \_ NOTIFYMODE dans le paramètre MCIWndCreate _dwStyle_ . Spécifiez le \_ style MCIWNDF NOPLAYBAR pour masquer la barre d’outils, et le \_ style MCIWNDF NOTIFYMODE pour émettre un message de notification approprié lorsque l’appareil s’arrête.

Vous pouvez lire l’appareil ou le fichier spécifié dans **MCIWndCreate** à l’aide de **MCIWndPlay**. La macro MCIWndPlay commence à lire le contenu à partir de sa position de lecture actuelle et continue jusqu’à sa fin.

Vous pouvez détruire ou fermer une fenêtre MCIWnd à l’aide de la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) ou [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) . La macro **MCIWndDestroy** ferme l’appareil ou le fichier et détruit la fenêtre MCIWnd en invalidant son handle. Si votre application peut réutiliser la fenêtre MCIWnd, utilisez **MCIWndClose** pour fermer l’appareil sans détruire la fenêtre.

Votre application peut détecter quand l’appareil s’arrête de fonctionner et fermer automatiquement la fenêtre. Pour ce faire, spécifiez le \_ style MCIWNDF NOTIFYMODE pour le paramètre *DwStyle* de [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea). L’appareil envoie alors un message [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md) à chaque fois qu’il change de mode. Votre application peut intercepter ce message pour déterminer si l’appareil a cessé de fonctionner. Lorsque l’appareil s’arrête, l’application ferme la fenêtre.

 

 




