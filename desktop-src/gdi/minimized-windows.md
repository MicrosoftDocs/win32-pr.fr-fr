---
description: Le système réduit la fenêtre principale d’une application (style chevauchant) à une fenêtre réduite lorsque l’utilisateur clique sur réduire dans le menu fenêtre ou l’application appelle la fonction ShowWindow et spécifie une valeur telle que SW \_ Minimize.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Windows réduite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415930"
---
# <a name="minimized-windows"></a>Windows réduite

Le système réduit la fenêtre principale d’une application (style chevauchant) à une fenêtre réduite lorsque l’utilisateur clique sur réduire dans le menu fenêtre ou l’application appelle la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) et spécifie une valeur telle que SW \_ Minimize. La réduction d’une fenêtre accélère les performances du système en réduisant la quantité de travail qu’une application doit effectuer lors de la mise à jour de sa fenêtre principale.

Pour une application classique, le système dessine une icône, appelée icône de classe, lorsque la fenêtre est réduite, en l’étiquetant avec le nom de la fenêtre. L’icône de classe, une image statique qui représente l’application, est spécifiée par l’application lors de l’inscription de la classe de fenêtre. L’application assigne un handle à l’icône de classe au membre **HICON** de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) avant d’appeler [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa). L’application peut utiliser la fonction [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) pour récupérer le handle d’icône.

 

 
