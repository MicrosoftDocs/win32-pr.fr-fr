---
title: Utilisation d’une interface multidocument
description: Utilisation d’une interface multidocument
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- MCIWndRegisterClass fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b75d337c5375b66974161c1c983c1aeec5bed7805457186139771d879132b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941054"
---
# <a name="using-a-multiple-document-interface"></a>Utilisation d’une interface multidocument

Les applications qui utilisent une interface multidocument (MDI) peuvent avoir besoin de spécifier des styles de fenêtre qui ne sont pas disponibles via la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) . Pour ces applications, vous pouvez inscrire et créer une fenêtre MCIWnd à l’aide de la fonction [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) avec la fonction [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) . La fonction **MCIWndRegisterClass** enregistre la \_ \_ classe de fenêtre de la classe de fenêtre MCIWND, puis **CreateWindowEx** crée une instance d’une fenêtre MCIWND.

 

 