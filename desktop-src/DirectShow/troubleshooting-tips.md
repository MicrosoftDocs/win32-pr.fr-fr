---
description: Conseils de dépannage
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Conseils de dépannage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531994"
---
# <a name="troubleshooting-tips"></a><span data-ttu-id="26c14-103">Conseils de dépannage</span><span class="sxs-lookup"><span data-stu-id="26c14-103">Troubleshooting Tips</span></span>

<span data-ttu-id="26c14-104">Les conseils suivants vous aideront à éviter les blocages ou les blocages dans votre application DirectShow.</span><span class="sxs-lookup"><span data-stu-id="26c14-104">This following tips will help you to avoid deadlocks or crashes in your DirectShow application.</span></span>

<span data-ttu-id="26c14-105">**Objets globaux**</span><span class="sxs-lookup"><span data-stu-id="26c14-105">**Global Objects**</span></span>

<span data-ttu-id="26c14-106">Un objet C++ global ne doit pas créer d’objets DirectShow dans sa méthode de constructeur, ni les libérer dans sa méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="26c14-106">A global C++ object should not create DirectShow objects in its constructor method or release them in its destructor method.</span></span> <span data-ttu-id="26c14-107">Cela peut entraîner le blocage indéfini de l’application, pour la raison suivante :</span><span class="sxs-lookup"><span data-stu-id="26c14-107">Doing so can cause the application to block indefinitely, for the following reason:</span></span>

<span data-ttu-id="26c14-108">Les threads ne peuvent pas se fermer lorsqu’ils se trouvent dans la fonction de point d’entrée d’une DLL.</span><span class="sxs-lookup"><span data-stu-id="26c14-108">Threads cannot exit while inside a DLL's entry-point function.</span></span> <span data-ttu-id="26c14-109">Le noyau 32 contient un verrou de processus global pendant la fonction de point d’entrée, et le verrou empêche le thread de se fermer.</span><span class="sxs-lookup"><span data-stu-id="26c14-109">Kernel 32 holds a global process lock during the entry-point function, and the lock prevents the thread from exiting.</span></span> <span data-ttu-id="26c14-110">Comme certains objets DirectShow possèdent des threads, ils peuvent bloquer s’ils sont libérés dans une fonction de point d’entrée de DLL.</span><span class="sxs-lookup"><span data-stu-id="26c14-110">Because some DirectShow objects own threads, they can block if released from inside a DLL entry-point function.</span></span> <span data-ttu-id="26c14-111">Si une application a un objet C++ global, la DLL runtime C appelle le destructeur de l’objet lorsque la DLL est déchargée.</span><span class="sxs-lookup"><span data-stu-id="26c14-111">If an application has a global C++ object, the C runtime DLL calls the object's destructor when the DLL is unloaded.</span></span> <span data-ttu-id="26c14-112">Si le destructeur libère des objets DirectShow, il peut en résulter un blocage.</span><span class="sxs-lookup"><span data-stu-id="26c14-112">If the destructor releases DirectShow objects, it can block as a result.</span></span>

<span data-ttu-id="26c14-113">Pour des raisons similaires, une DLL ne doit pas créer ou libérer des objets DirectShow dans sa routine de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="26c14-113">For similar reasons, a DLL should not create or release DirectShow objects in its entry point routine.</span></span>

<span data-ttu-id="26c14-114">**Libérer des interfaces**</span><span class="sxs-lookup"><span data-stu-id="26c14-114">**Releasing Interfaces**</span></span>

<span data-ttu-id="26c14-115">Vous devez libérer tous les pointeurs d’interface DirectShow pendant que votre application traite encore des messages avant de quitter la boucle de message.</span><span class="sxs-lookup"><span data-stu-id="26c14-115">You should release all DirectShow interface pointers while your application is still processing messages, before it exits the message loop.</span></span> <span data-ttu-id="26c14-116">Dans le cas contraire, vous pouvez voir plusieurs assertions, car certains objets DirectShow envoient des messages pendant leurs routines de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="26c14-116">Otherwise, you might see various asserts, because some DirectShow objects send messages during their clean-up routines.</span></span>

<span data-ttu-id="26c14-117">(En tant que corollic, si vous utilisez la classe ATL **CWindowImpl** , n’attendez pas que **OnFinalMessage** libère les interfaces.</span><span class="sxs-lookup"><span data-stu-id="26c14-117">(As a corollary, if you are using the ATL **CWindowImpl** class, do not wait until **OnFinalMessage** to free the interfaces.</span></span> <span data-ttu-id="26c14-118">Au lieu de cela, libérez-les lorsque vous gérez le \_ message WM Close.)</span><span class="sxs-lookup"><span data-stu-id="26c14-118">Instead, free them when you handle the WM\_CLOSE message.)</span></span>

<span data-ttu-id="26c14-119">**Nombres de références**</span><span class="sxs-lookup"><span data-stu-id="26c14-119">**Reference Counts**</span></span>

<span data-ttu-id="26c14-120">Lorsque la version de débogage de Quartz.dll est déchargée, elle vérifie si des objets DirectShow ont des décomptes de références qui n’ont pas été libérés.</span><span class="sxs-lookup"><span data-stu-id="26c14-120">When the debug version of Quartz.dll unloads, it checks whether any DirectShow objects have reference counts that were not released.</span></span> <span data-ttu-id="26c14-121">Si c’est le cas, elle lève une assertion :</span><span class="sxs-lookup"><span data-stu-id="26c14-121">If so, it throws an assertion:</span></span>


```C++
g_cFGObjects == 0 
```



<span data-ttu-id="26c14-122">Lorsque cette assertion échoue, cela signifie que votre application a divulgué un nombre de références.</span><span class="sxs-lookup"><span data-stu-id="26c14-122">When this assertion fails, it means your application has leaked a reference count.</span></span> <span data-ttu-id="26c14-123">Examinez votre code et assurez-vous de libérer tous les pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="26c14-123">Review your code and make sure that you release all interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26c14-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26c14-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26c14-125">Débogage dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="26c14-125">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



