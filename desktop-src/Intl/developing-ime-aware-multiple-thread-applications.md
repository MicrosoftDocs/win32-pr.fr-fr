---
description: Le IMM comprend la vérification de l’identification du thread qui détermine si un thread appelant est le créateur d’un handle de contexte de méthode d’entrée spécifié (type HIMC) ou d’un handle de fenêtre (type HWND).
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Développement d’applications IME-Aware plusieurs threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf495922d347119db3b8b517af13c850f2f19dfc558609f93f24953f0a3386a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949594"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a>Développement d’applications IME-Aware plusieurs threads

Le IMM comprend la vérification de l’identification du thread qui détermine si un thread appelant est le créateur d’un handle de contexte de méthode d’entrée spécifié (type HIMC) ou d’un handle de fenêtre (type HWND). Si le thread n’est pas le créateur du descripteur, la fonction IMM appelée échoue et un appel ultérieur à [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur d' \_ accès non valide \_ .

> [!Note]  
> L’architecture IMM actuelle ne fournit pas de fonction de synchronisation pour l’accès aux handles de IMM.

 

Pour utiliser la vérification de l’identification des threads, vos applications doivent respecter les instructions suivantes :

-   Un thread ne doit pas accéder au contexte d’entrée créé par un autre thread.
-   Un thread ne doit pas associer un contexte d’entrée à une fenêtre créée par un autre thread, et vice versa.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du gestionnaire de méthode d’entrée](using-input-method-manager.md)
</dt> </dl>

 

 
