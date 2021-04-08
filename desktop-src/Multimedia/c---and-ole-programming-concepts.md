---
title: Concepts de programmation C++ et OLE
description: Concepts de programmation C++ et OLE
ms.assetid: 2c6c3f29-aa5d-4e55-8c4d-16c5fb223fb9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c47ef5ff2d89930b5d4138f12e3ebc15385a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840829"
---
# <a name="c-and-ole-programming-concepts"></a><span data-ttu-id="a9068-103">Concepts de programmation C++ et OLE</span><span class="sxs-lookup"><span data-stu-id="a9068-103">C++ and OLE Programming Concepts</span></span>

<span data-ttu-id="a9068-104">Les gestionnaires de fichiers et de flux inclus avec Windows utilisent une conception orientée objet pour promouvoir une interface standard et partager des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="a9068-104">The file and stream handlers included with Windows use an object-oriented design to promote a standard interface and to share functionality.</span></span> <span data-ttu-id="a9068-105">Ces gestionnaires sont écrits en C++ et utilisent le modèle objet du composant OLE.</span><span class="sxs-lookup"><span data-stu-id="a9068-105">These handlers are written in C++ and use the OLE Component Object Model.</span></span>

<span data-ttu-id="a9068-106">Vous pouvez développer des gestionnaires personnalisés à l’aide des systèmes de développement C ou C++. Toutefois, l’utilisation de C++ est vivement recommandée, car elle offre une approche plus simple et plus simple pour implémenter un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="a9068-106">You can develop custom handlers using the C or C++ development systems; however, using C++ is strongly recommended, because it provides an easier and more straightforward approach to implement a handler.</span></span> <span data-ttu-id="a9068-107">À l’aide de C++, vous pouvez définir explicitement des données en tant qu’objets, et vous pouvez associer les fonctions qui manipulent les données aux fonctions membres d’un objet.</span><span class="sxs-lookup"><span data-stu-id="a9068-107">Using C++, you can explicitly define data as objects, and you can associate the functions that manipulate the data with the member functions of an object.</span></span>

<span data-ttu-id="a9068-108">Cette section identifie et résume brièvement les concepts importants de C++ et le modèle objet composant OLE qui s’appliquent à la conception et à l’implémentation de gestionnaires de fichiers et de flux.</span><span class="sxs-lookup"><span data-stu-id="a9068-108">This section identifies and briefly summarizes the important concepts of C++ and the OLE Component Object Model that apply to designing and implementing file and stream handlers.</span></span> <span data-ttu-id="a9068-109">Il existe de nombreux ouvrages écrits à propos de la programmation C++, que vous pouvez référencer pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a9068-109">There are many books written about C++ programming that you can reference for more information.</span></span> <span data-ttu-id="a9068-110">Pour plus d’informations sur OLE, consultez le *Guide de référence du programmeur OLE*.</span><span class="sxs-lookup"><span data-stu-id="a9068-110">For more information on OLE, please see the *OLE Programmer's Reference*.</span></span>

 

 




