---
title: Connexion d’une fenêtre de capture à un pilote de capture
description: Connexion d’une fenêtre de capture à un pilote de capture
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- Message WM_CAP_DRIVER_CONNECT
- capDriverConnect macro)
- capGetDriverDescription fonction)
- Message WM_CAP_DRIVER_GET_NAME
- capDriverGetName macro)
- Message WM_CAP_DRIVER_GET_VERSION
- capDriverGetVersion macro)
- Message WM_CAP_DRIVER_DISCONNECT
- capDriverDisconnect macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416858"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a>Connexion d’une fenêtre de capture à un pilote de capture

Vous pouvez connecter ou déconnecter dynamiquement une fenêtre de capture à un pilote de capture. Vous pouvez connecter ou associer une fenêtre de capture à un pilote de capture à l’aide du message de [**\_ \_ \_ connexion du pilote WM Cap**](wm-cap-driver-connect.md) (ou de la macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) ). Une fois qu’une fenêtre de capture et le pilote de capture sont connectés, vous pouvez envoyer des messages spécifiques à l’appareil au pilote de capture associé à une fenêtre de capture.

Si plusieurs périphériques de capture sont installés sur un système, vous pouvez connecter une fenêtre de capture à un pilote de périphérique de capture vidéo spécifique en spécifiant un entier pour le paramètre *wParam* du \_ message de connexion du pilote WM Cap \_ \_ . L’entier est un index qui identifie un pilote de capture vidéo listé dans le registre ou dans \[ la \] section drivers du fichier SYSTEM.INI. Utilisez zéro pour la première entrée d’index.

Vous pouvez récupérer le nom et la version d’un pilote de capture installé à l’aide de la fonction [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) . Votre application peut utiliser cette fonction pour énumérer les périphériques de capture et les pilotes installés, afin que l’utilisateur puisse sélectionner un appareil de capture pour se connecter à une fenêtre de capture.

Vous pouvez récupérer le nom du pilote de périphérique de capture connecté à une fenêtre de capture à l’aide du message [**WM \_ Cap \_ Driver \_ obtenir le \_ nom**](wm-cap-driver-get-name.md) (ou la macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) ). Pour récupérer la version d’un pilote de capture installé, utilisez le message [**WM \_ Cap \_ Driver \_ obtenir la \_ version**](wm-cap-driver-get-version.md) (ou la macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) ).

Vous pouvez déconnecter une fenêtre de capture d’un pilote de capture à l’aide du message de [**\_ \_ \_ déconnexion du pilote WM Cap**](wm-cap-driver-disconnect.md) (ou de la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) ).

Quand une fenêtre de capture est détruite, tous les pilotes de périphérique de capture vidéo connectés sont automatiquement déconnectés.

 

 




