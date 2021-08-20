---
title: Capture de fin de clé
description: Capture de fin de clé
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- CAPTUREPARMS, structure
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5764f6b1853e1b161501f3c8df22ff0b7387649c517a28e7e36e7a094f35b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140049"
---
# <a name="keys-ending-capture"></a>Capture de fin de clé

Vous pouvez autoriser l’utilisateur à abandonner une session de capture en appuyant sur une touche ou une combinaison de touches du clavier, ou en appuyant sur le bouton droit ou gauche de la souris. Si l’utilisateur abandonne une session de capture en temps réel, le contenu du fichier de capture est ignoré. Si l’utilisateur abandonne une session de capture d’image pas à pas, le contenu du fichier de capture jusqu’au point d’abandon de la capture est enregistré.

Vous pouvez récupérer les paramètres de l’abandon d’une session de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’embout de la connexion WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Le paramètre de séquence de touches actuel est stocké dans le membre **vKeyAbort** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) ; les paramètres de la souris actuels sont stockés dans les membres **fAbortLeftMouse** et **fAbortRightMouse** . Vous pouvez définir une nouvelle clé ou une combinaison de touches en spécifiant la combinaison keycode ou keycode (comme dans une combinaison de touches CTRL ou Maj) comme valeur de **vKeyAbort**, ou définir le bouton gauche ou droit de la souris comme touche abandonner en spécifiant le membre **fAbortLeftMouse** ou **fAbortRightMouse** . Après avoir défini ces membres, envoyez la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). La valeur par défaut de **vKeyAbort** est VK \_ Escape. Vous devez appeler la fonction [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) avant de spécifier une touche qui peut abandonner une session de capture. Les valeurs par défaut de **fAbortLeftMouse** et **fAbortRightMouse** sont **true**.

 

 