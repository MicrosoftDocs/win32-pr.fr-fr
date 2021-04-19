---
description: Le IMM comprend la vérification de l’identification du thread qui détermine si un thread appelant est le créateur d’un handle de contexte de méthode d’entrée spécifié (type HIMC) ou d’un handle de fenêtre (type HWND).
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Développement d’applications IME-Aware plusieurs threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5730fc72ef41a84e01655116f94fc274f60548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543531"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a><span data-ttu-id="d1432-103">Développement d’applications IME-Aware plusieurs threads</span><span class="sxs-lookup"><span data-stu-id="d1432-103">Developing IME-Aware Multiple-thread Applications</span></span>

<span data-ttu-id="d1432-104">Le IMM comprend la vérification de l’identification du thread qui détermine si un thread appelant est le créateur d’un handle de contexte de méthode d’entrée spécifié (type HIMC) ou d’un handle de fenêtre (type HWND).</span><span class="sxs-lookup"><span data-stu-id="d1432-104">The IMM includes thread identification checking that determines if a calling thread is the creator of a specified input method context handle (HIMC type) or window handle (HWND type).</span></span> <span data-ttu-id="d1432-105">Si le thread n’est pas le créateur du descripteur, la fonction IMM appelée échoue et un appel ultérieur à [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur d' \_ accès non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="d1432-105">If the thread is not the creator of the handle, the called IMM function fails and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_ACCESS.</span></span>

> [!Note]  
> <span data-ttu-id="d1432-106">L’architecture IMM actuelle ne fournit pas de fonction de synchronisation pour l’accès aux handles de IMM.</span><span class="sxs-lookup"><span data-stu-id="d1432-106">The current IMM architecture does not provide a synchronization facility for access to IMM handles.</span></span>

 

<span data-ttu-id="d1432-107">Pour utiliser la vérification de l’identification des threads, vos applications doivent respecter les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1432-107">To use thread identification checking, your applications must adhere to the following guidelines:</span></span>

-   <span data-ttu-id="d1432-108">Un thread ne doit pas accéder au contexte d’entrée créé par un autre thread.</span><span class="sxs-lookup"><span data-stu-id="d1432-108">A thread should not access the input context created by another thread.</span></span>
-   <span data-ttu-id="d1432-109">Un thread ne doit pas associer un contexte d’entrée à une fenêtre créée par un autre thread, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="d1432-109">A thread should not associate an input context with a window created by another thread, and vice versa.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1432-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1432-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1432-111">Utilisation du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="d1432-111">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
