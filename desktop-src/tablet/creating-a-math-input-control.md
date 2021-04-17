---
description: Explique comment créer un contrôle d’entrée mathématique.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Création d’un contrôle d’entrée mathématique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554275"
---
# <a name="creating-a-math-input-control"></a><span data-ttu-id="501c1-103">Création d’un contrôle d’entrée mathématique</span><span class="sxs-lookup"><span data-stu-id="501c1-103">Creating a Math Input Control</span></span>

<span data-ttu-id="501c1-104">Pour créer le contrôle d’entrée mathématique, vous devez :</span><span class="sxs-lookup"><span data-stu-id="501c1-104">To create the math input control, you must:</span></span>

-   [<span data-ttu-id="501c1-105">Inclure des en-têtes et des bibliothèques pour le contrôle d’entrée mathématique</span><span class="sxs-lookup"><span data-stu-id="501c1-105">Include Headers and Libraries for the Math Input Control</span></span>](#include-headers-and-libraries-for-the-math-input-control)
-   [<span data-ttu-id="501c1-106">Déclarer le pointeur de contrôle et appeler CoInitialize sur le pointeur de contrôle</span><span class="sxs-lookup"><span data-stu-id="501c1-106">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [<span data-ttu-id="501c1-107">Afficher le contrôle</span><span class="sxs-lookup"><span data-stu-id="501c1-107">Show the Control</span></span>](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a><span data-ttu-id="501c1-108">Inclure des en-têtes et des bibliothèques pour le contrôle d’entrée mathématique</span><span class="sxs-lookup"><span data-stu-id="501c1-108">Include Headers and Libraries for the Math Input Control</span></span>

<span data-ttu-id="501c1-109">Le code suivant doit être placé en haut de votre code où vous utiliserez le contrôle d’entrée mathématique.</span><span class="sxs-lookup"><span data-stu-id="501c1-109">The following code should be placed at the top of your code where you will be using the math input control.</span></span>


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



<span data-ttu-id="501c1-110">Ce code ajoute la prise en charge du contrôle d’entrée mathématique à votre application.</span><span class="sxs-lookup"><span data-stu-id="501c1-110">This code will add support for the math input control to your application.</span></span>

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a><span data-ttu-id="501c1-111">Déclarer le pointeur de contrôle et appeler CoInitialize sur le pointeur de contrôle</span><span class="sxs-lookup"><span data-stu-id="501c1-111">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>

<span data-ttu-id="501c1-112">Une fois que vous avez inclus les en-têtes pour votre contrôle, vous pouvez déclarer le pointeur de contrôle et vous pouvez appeler CoInitialize dessus pour créer un handle pour l’interface de contrôle d’entrée mathématique.</span><span class="sxs-lookup"><span data-stu-id="501c1-112">After you have included the headers for your control, you can declare the control pointer and can call CoInitialize on it to create a handle to the math input control interface.</span></span> <span data-ttu-id="501c1-113">Le code suivant peut être placé dans une classe ou en tant que variable globale dans l’implémentation de votre application :</span><span class="sxs-lookup"><span data-stu-id="501c1-113">The following code can be placed in a class or as a global variable in your application's implementation:</span></span>


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



<span data-ttu-id="501c1-114">Le code suivant montre comment appeler CoInitialize sur le pointeur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="501c1-114">The following code shows how you can call CoInitialize on the control pointer.</span></span>


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



<span data-ttu-id="501c1-115">Après avoir appelé CoInitialize sur le pointeur de contrôle, vous disposez d’une référence au contrôle et vous pouvez accéder aux méthodes du contrôle.</span><span class="sxs-lookup"><span data-stu-id="501c1-115">After calling CoInitialize on the control pointer, you have a reference to the control and can access the control's methods.</span></span> <span data-ttu-id="501c1-116">Par exemple, vous pouvez activer l’ensemble étendu de contrôles comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="501c1-116">For example, you could enable the extended set of controls as shown in the following example.</span></span>


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a><span data-ttu-id="501c1-117">Afficher le contrôle</span><span class="sxs-lookup"><span data-stu-id="501c1-117">Show the Control</span></span>

<span data-ttu-id="501c1-118">Le contrôle ne s’affiche pas automatiquement une fois que vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="501c1-118">The control will not automatically appear after you create it.</span></span> <span data-ttu-id="501c1-119">Pour afficher le contrôle, appelez la méthode [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) sur la référence de contrôle que vous avez créée à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="501c1-119">To show the control, call the [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) method on the control reference that you created in the previous step.</span></span> <span data-ttu-id="501c1-120">Le code suivant montre comment la méthode [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) peut être appelée.</span><span class="sxs-lookup"><span data-stu-id="501c1-120">The following code demonstrates how the [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) method can be called.</span></span>


```
   hr = g_spMIC->Show();
   
```



<span data-ttu-id="501c1-121">Une fois que le contrôle s’affiche, il ressemble à l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="501c1-121">After the control shows, it will look something like the following illustration.</span></span>

![capture d’écran montrant le contrôle d’entrée mathématique](images/mic.png)

<span data-ttu-id="501c1-123">Notez que j’ai activé le jeu de boutons étendus pour que les opérations de **restauration par progression** et les **annulations** soient disponibles.</span><span class="sxs-lookup"><span data-stu-id="501c1-123">Note that I have enabled the extended set of buttons so that **Redo** and **Undo** are available.</span></span>

 

 
