---
description: Les gestionnaires d’exceptions vectorisées sont une extension de la gestion structurée des exceptions.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Gestion des exceptions vectorisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861126"
---
# <a name="vectored-exception-handling"></a><span data-ttu-id="5d828-103">Gestion des exceptions vectorisées</span><span class="sxs-lookup"><span data-stu-id="5d828-103">Vectored Exception Handling</span></span>

<span data-ttu-id="5d828-104">Les gestionnaires d’exceptions vectorisées sont une extension de la gestion structurée des exceptions.</span><span class="sxs-lookup"><span data-stu-id="5d828-104">Vectored exception handlers are an extension to structured exception handling.</span></span> <span data-ttu-id="5d828-105">Une application peut enregistrer une fonction pour surveiller ou gérer toutes les exceptions pour l’application.</span><span class="sxs-lookup"><span data-stu-id="5d828-105">An application can register a function to watch or handle all exceptions for the application.</span></span> <span data-ttu-id="5d828-106">Les gestionnaires vectorisés ne sont pas basés sur des trames. par conséquent, vous pouvez ajouter un gestionnaire qui sera appelé, quel que soit l’endroit où vous vous trouvez dans un frame d’appel.</span><span class="sxs-lookup"><span data-stu-id="5d828-106">Vectored handlers are not frame-based, therefore, you can add a handler that will be called regardless of where you are in a call frame.</span></span> <span data-ttu-id="5d828-107">Les gestionnaires vectorisés sont appelés dans l’ordre dans lequel ils ont été ajoutés, après que le débogueur ait effectué une notification de première chance, mais avant que le système ne commence à dérouler la pile.</span><span class="sxs-lookup"><span data-stu-id="5d828-107">Vectored handlers are called in the order that they were added, after the debugger gets a first chance notification, but before the system begins unwinding the stack.</span></span>

<span data-ttu-id="5d828-108">Pour ajouter un gestionnaire de continuation vectorisé, utilisez la fonction [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) .</span><span class="sxs-lookup"><span data-stu-id="5d828-108">To add a vectored continue handler, use the [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) function.</span></span> <span data-ttu-id="5d828-109">Pour supprimer ce gestionnaire, utilisez la fonction [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) .</span><span class="sxs-lookup"><span data-stu-id="5d828-109">To remove this handler, use the [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) function.</span></span>

<span data-ttu-id="5d828-110">Pour ajouter un gestionnaire d’exceptions vectorisées, utilisez la fonction [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) .</span><span class="sxs-lookup"><span data-stu-id="5d828-110">To add a vectored exception handler, use the [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) function.</span></span> <span data-ttu-id="5d828-111">Pour supprimer ce gestionnaire, utilisez la fonction [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) .</span><span class="sxs-lookup"><span data-stu-id="5d828-111">To remove this handler, use the [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) function.</span></span>

 

 
