---
title: Utilisation d’une interface multidocument
description: Utilisation d’une interface multidocument
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- MCIWndRegisterClass fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebc30d177ee7b0dd8ae0c5d9ca23c5d6ca577c2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368908"
---
# <a name="using-a-multiple-document-interface"></a>Utilisation d’une interface multidocument

Les applications qui utilisent une interface multidocument (MDI) peuvent avoir besoin de spécifier des styles de fenêtre qui ne sont pas disponibles via la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) . Pour ces applications, vous pouvez inscrire et créer une fenêtre MCIWnd à l’aide de la fonction [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) avec la fonction [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) . La fonction **MCIWndRegisterClass** enregistre la \_ \_ classe de fenêtre de la classe de fenêtre MCIWND, puis **CreateWindowEx** crée une instance d’une fenêtre MCIWND.

 

 