---
title: Inscription d’un serveur exécutable en cours d’exécution
description: Inscription d’un serveur exécutable en cours d’exécution
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310833"
---
# <a name="registering-a-running-exe-server"></a><span data-ttu-id="20e3c-103">Inscription d’un serveur exécutable en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="20e3c-103">Registering a Running EXE Server</span></span>

<span data-ttu-id="20e3c-104">Lorsqu’un serveur exécutable (EXE) est lancé, il doit appeler [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), qui inscrit le CLSID du serveur dans ce que l’on appelle la table de classe (une table différente de la table d’objets en cours d’exécution).</span><span class="sxs-lookup"><span data-stu-id="20e3c-104">When an executable (EXE) server is launched, it should call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), which registers the CLSID for the server in what is called the class table (a different table than the running object table).</span></span> <span data-ttu-id="20e3c-105">Lorsqu’un serveur est inscrit dans la table de classe, il permet au gestionnaire de contrôle des services (SCM) de déterminer qu’il n’est pas nécessaire de lancer à nouveau la classe, car le serveur est déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="20e3c-105">When a server is registered in the class table, it allows the service control manager (SCM) to determine that it is not necessary to launch the class again, because the server is already running.</span></span> <span data-ttu-id="20e3c-106">Si le serveur n’est pas listé dans la table de classe, le SCM recherche les valeurs appropriées dans le registre et lance le serveur associé au CLSID donné.</span><span class="sxs-lookup"><span data-stu-id="20e3c-106">Only if the server is not listed in the class table will the SCM check the registry for appropriate values and launch the server associated with the given CLSID.</span></span>

<span data-ttu-id="20e3c-107">Vous transmettez [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) au CLSID pour la classe et un pointeur vers son interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="20e3c-107">You pass [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) the CLSID for the class and a pointer to its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="20e3c-108">Les clients qui appellent par la suite [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) avec ce CLSID récupèrent un pointeur vers l’interface demandée, tant que la sécurité ne l’interdit pas.</span><span class="sxs-lookup"><span data-stu-id="20e3c-108">Clients who subsequently call [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with this CLSID will retrieve a pointer to their requested interface, as long as security does not forbid it.</span></span> <span data-ttu-id="20e3c-109">(Consultez [fonctions d’assistance](instance-creation-helper-functions.md) pour la création d’instance pour obtenir une description de plusieurs fonctions de création et d’activation d’une instance.)</span><span class="sxs-lookup"><span data-stu-id="20e3c-109">(See [Instance Creation Helper Functions](instance-creation-helper-functions.md) for a description of several instance creation and activation functions.)</span></span>

<span data-ttu-id="20e3c-110">Le serveur d’un objet de classe doit appeler [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) pour révoquer l’objet de classe (supprimer son inscription) lorsque toutes les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="20e3c-110">The server for a class object should call [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) to revoke the class object (remove its registration) when all of the following are true:</span></span>

-   <span data-ttu-id="20e3c-111">Il n’existe aucune instance existante de la définition de l’objet.</span><span class="sxs-lookup"><span data-stu-id="20e3c-111">There are no existing instances of the object definition.</span></span>
-   <span data-ttu-id="20e3c-112">Il n’y a aucun verrou sur l’objet de classe.</span><span class="sxs-lookup"><span data-stu-id="20e3c-112">There are no locks on the class object.</span></span>
-   <span data-ttu-id="20e3c-113">L’application qui fournit des services à l’objet de classe n’est pas sous le contrôle utilisateur (non visible par l’utilisateur sur l’affichage).</span><span class="sxs-lookup"><span data-stu-id="20e3c-113">The application providing services to the class object is not under user control (not visible to the user on the display).</span></span>

## <a name="related-topics"></a><span data-ttu-id="20e3c-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20e3c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20e3c-115">Installation d’une application en tant que service</span><span class="sxs-lookup"><span data-stu-id="20e3c-115">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="20e3c-116">Inscription d’une classe lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="20e3c-116">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="20e3c-117">Inscription d’objets dans le ROT</span><span class="sxs-lookup"><span data-stu-id="20e3c-117">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="20e3c-118">Inscription automatique</span><span class="sxs-lookup"><span data-stu-id="20e3c-118">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 




