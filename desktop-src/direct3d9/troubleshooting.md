---
description: Cette rubrique répertorie les catégories courantes de problèmes que vous pouvez rencontrer lors de l’écriture d’applications Direct3D et comment les empêcher.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Résolution des problèmes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6726e761dd8c15e2da18e6c370472a73e82cef0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513115"
---
# <a name="troubleshooting-direct3d-9"></a><span data-ttu-id="4d6c6-103">Résolution des problèmes (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4d6c6-103">Troubleshooting (Direct3D 9)</span></span>

<span data-ttu-id="4d6c6-104">Cette rubrique répertorie les catégories courantes de problèmes que vous pouvez rencontrer lors de l’écriture d’applications Direct3D et comment les empêcher.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-104">This topic lists common categories of problems that you might encounter when writing Direct3D applications, and how to prevent them.</span></span>

## <a name="device-creation"></a><span data-ttu-id="4d6c6-105">Création de l’appareil</span><span class="sxs-lookup"><span data-stu-id="4d6c6-105">Device Creation</span></span>

<span data-ttu-id="4d6c6-106">Si votre application échoue lors de la création de l’appareil, recherchez les erreurs courantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-106">If your application fails during device creation, check for the following common errors.</span></span>

-   <span data-ttu-id="4d6c6-107">Veillez à vérifier les fonctionnalités de l’appareil, en particulier les profondeurs de rendu.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-107">Make sure you check the device capabilities, particularly the render depths.</span></span>
-   <span data-ttu-id="4d6c6-108">Examinez le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-108">Examine the error code.</span></span> <span data-ttu-id="4d6c6-109">D3DERR \_ OUTOFVIDEOMEMORY est toujours possible.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-109">D3DERR\_OUTOFVIDEOMEMORY is always possible.</span></span>
-   <span data-ttu-id="4d6c6-110">Utilisez les bibliothèques de liens dynamiques (dll) de débogage DirectX et passez en revue les messages de sortie sous le débogueur.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-110">Use the debug DirectX dynamic-link libraries (DLLs) and review output messages under the debugger.</span></span>

## <a name="using-lit-vertices"></a><span data-ttu-id="4d6c6-111">Utilisation des vertex allumés</span><span class="sxs-lookup"><span data-stu-id="4d6c6-111">Using Lit Vertices</span></span>

<span data-ttu-id="4d6c6-112">Les applications qui utilisent des vertex allumés doivent désactiver le moteur d’éclairage Direct3D en affectant la \_ **valeur false** à l’état de rendu d’éclairage D3DRS.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-112">Applications that use lit vertices should disable the Direct3D lighting engine by setting the D3DRS\_LIGHTING render state to **FALSE**.</span></span> <span data-ttu-id="4d6c6-113">Par défaut, lorsque l’éclairage est activé, le système définit la couleur de tout vertex qui ne contient pas de vecteur normal à 0 (noir), même si le vertex d’entrée contenait une valeur de couleur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-113">By default, when lighting is enabled, the system sets the color for any vertex that doesn't contain a normal vector to 0 (black), even if the input vertex contained a nonzero color value.</span></span> <span data-ttu-id="4d6c6-114">Étant donné que lit-vertex ne contient pas, par nature, un sommet normal, toutes les informations de couleur transmises à Direct3D sont perdues pendant le rendu si le moteur d’éclairage est activé.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-114">Because lit-vertices don't, by their nature, contain a vertex normal, any color information passed to Direct3D is lost during rendering if the lighting engine is enabled.</span></span>

<span data-ttu-id="4d6c6-115">Évidemment, la couleur de vertex est importante pour toute application qui effectue sa propre lumière.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-115">Obviously, vertex color is important to any application that performs its own lighting.</span></span> <span data-ttu-id="4d6c6-116">Pour empêcher le système d’imposer les valeurs par défaut, veillez à définir l' \_ éclairage D3DRS sur **false**.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-116">To prevent the system from imposing the default values, make sure you set D3DRS\_LIGHTING to **FALSE**.</span></span>

<span data-ttu-id="4d6c6-117">Si votre application s’exécute mais que rien n’est visible, recherchez les erreurs courantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-117">If your application runs but nothing is visible, check for the following common errors.</span></span>

-   <span data-ttu-id="4d6c6-118">Assurez-vous que vos triangles ne sont pas dégénérées.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-118">Ensure that your triangles are not degenerate.</span></span>
-   <span data-ttu-id="4d6c6-119">Assurez-vous que vos triangles ne sont pas éliminés.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-119">Ensure that your triangles are not being culled.</span></span>
-   <span data-ttu-id="4d6c6-120">Assurez-vous que vos transformations sont cohérentes en interne.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-120">Make sure that your transformations are internally consistent.</span></span>
-   <span data-ttu-id="4d6c6-121">Vérifiez les paramètres de la fenêtre d’affichage pour vous assurer qu’ils permettent d’afficher vos triangles.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-121">Check the viewport settings to be sure they allow your triangles to be seen.</span></span>

## <a name="debugging"></a><span data-ttu-id="4d6c6-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="4d6c6-122">Debugging</span></span>

<span data-ttu-id="4d6c6-123">Le débogage d’une application Direct3D peut s’avérer difficile.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-123">Debugging a Direct3D application can be challenging.</span></span> <span data-ttu-id="4d6c6-124">Essayez les techniques suivantes, en plus de vérifier toutes les valeurs de retour, un Conseil particulièrement important dans la programmation Direct3D, qui dépend des implémentations matérielles très différentes.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-124">Try the following techniques, in addition to checking all the return values - a particularly important piece of advice in Direct3D programming, which is dependent on very different hardware implementations.</span></span>

-   <span data-ttu-id="4d6c6-125">Basculez vers les dll de débogage.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-125">Switch to debug DLLs.</span></span>
-   <span data-ttu-id="4d6c6-126">Forcez un périphérique logiciel uniquement, en désactivant l’accélération matérielle, même lorsqu’elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-126">Force a software-only device, turning off hardware acceleration even when it is available.</span></span>
-   <span data-ttu-id="4d6c6-127">Forcez les surfaces dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-127">Force surfaces into system memory.</span></span>
-   <span data-ttu-id="4d6c6-128">Créez une option pour qu’elle s’exécute dans une fenêtre, afin que vous puissiez utiliser un débogueur intégré.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-128">Create an option to run in a window, so that you can use an integrated debugger.</span></span>

<span data-ttu-id="4d6c6-129">Les deuxième et troisième options de cette liste peuvent vous aider à éviter le verrou Win16 qui peut entraîner le blocage de votre débogueur.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-129">The second and third options in this list can help you avoid the Win16 lock which can otherwise cause your debugger to hang.</span></span>

<span data-ttu-id="4d6c6-130">Essayez également d’ajouter les entrées suivantes à Win.ini.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-130">Also, try adding the following entries to Win.ini.</span></span>


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a><span data-ttu-id="4d6c6-131">Initialisation de Borland Floating-Point</span><span class="sxs-lookup"><span data-stu-id="4d6c6-131">Borland Floating-Point Initialization</span></span>

<span data-ttu-id="4d6c6-132">Les compilateurs de Borland signalent des exceptions de virgule flottante d’une manière incompatible avec Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-132">Compilers from Borland report floating-point exceptions in a manner that is incompatible with Direct3D.</span></span> <span data-ttu-id="4d6c6-133">Pour résoudre ce problème, incluez un \_ Gestionnaire d’exceptions matherr comme suit :</span><span class="sxs-lookup"><span data-stu-id="4d6c6-133">To solve this problem, include a \_matherr exception handler like the following:</span></span>


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a><span data-ttu-id="4d6c6-134">Validation des paramètres</span><span class="sxs-lookup"><span data-stu-id="4d6c6-134">Parameter Validation</span></span>

<span data-ttu-id="4d6c6-135">Pour des raisons de performances, la version de débogage du runtime en mode immédiat Direct3D effectue plus de validation de paramètres que la version commerciale, qui n’effectue parfois aucune validation.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-135">For performance reasons, the debug version of the Direct3D Immediate Mode run time performs more parameter validation than the retail version, which sometimes performs no validation at all.</span></span> <span data-ttu-id="4d6c6-136">Cela permet aux applications d’effectuer un débogage robuste avec le composant d’exécution de débogage le plus lent avant d’utiliser la version commerciale la plus rapide pour le réglage des performances et la version finale.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-136">This enables applications to perform robust debugging with the slower debug run-time component before using the faster retail version for performance tuning and final release.</span></span>

<span data-ttu-id="4d6c6-137">Bien que plusieurs méthodes Direct3D en mode immédiat imposent des limites aux valeurs qu’elles peuvent accepter, ces limites ne sont souvent vérifiées et appliquées que par la version Debug du mode exécution Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-137">Although several Direct3D Immediate Mode methods impose limits on the values that they can accept, these limits are often only checked and enforced by the debug version of the Direct3D Immediate Mode run time.</span></span> <span data-ttu-id="4d6c6-138">Les applications doivent être conformes à ces limites, ou des résultats imprévisibles et indésirables peuvent se produire lors de l’exécution sur la version commerciale de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-138">Applications must conform to these limits, or unpredictable and undesirable results can occur when running on the retail version of Direct3D.</span></span> <span data-ttu-id="4d6c6-139">Par exemple, la méthode [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accepte un paramètre (PrimitiveCount) qui indique le nombre de primitives que la méthode restituera.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-139">For example, the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method accepts a parameter (PrimitiveCount) that indicates the number of primitives that the method will render.</span></span> <span data-ttu-id="4d6c6-140">La méthode peut uniquement accepter des valeurs comprises entre 0 et D3DMAXNUMPRIMITIVES.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-140">The method can only accept values between 0 and D3DMAXNUMPRIMITIVES.</span></span> <span data-ttu-id="4d6c6-141">Dans la version Debug de Direct3D, si vous transmettez plus de primitives D3DMAXNUMPRIMITIVES, la méthode échoue correctement, en imprimant un message d’erreur dans le journal des erreurs et en renvoyant une valeur d’erreur à votre application.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-141">In the debug version of Direct3D, if you pass more than D3DMAXNUMPRIMITIVES primitives, the method fails gracefully, printing an error message to the error log, and returning an error value to your application.</span></span> <span data-ttu-id="4d6c6-142">À l’inverse, si votre application génère la même erreur lorsqu’elle s’exécute avec la version commerciale du runtime, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-142">Conversely, if your application makes the same error when it is running with the retail version of the run time, behavior is undefined.</span></span> <span data-ttu-id="4d6c6-143">Pour des raisons de performances, la méthode ne valide pas les paramètres, ce qui se traduit par un comportement imprévisible et complet lorsqu’ils ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-143">For performance reasons, the method does not validate the parameters, resulting in unpredictable and completely situational behavior when they are not valid.</span></span> <span data-ttu-id="4d6c6-144">Dans certains cas, l’appel peut fonctionner et, dans d’autres cas, il peut provoquer une erreur de mémoire dans Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-144">In some cases the call might work, and in other cases it might cause a memory fault in Direct3D.</span></span> <span data-ttu-id="4d6c6-145">Si un appel non valide fonctionne de manière cohérente avec une configuration matérielle spécifique et une version de DirectX, il n’existe aucune garantie qu’il continuera à fonctionner sur un autre matériel ou avec des versions ultérieures de DirectX.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-145">If an invalid call consistently works with a particular hardware configuration and DirectX version, there is no guarantee that it will continue to function on other hardware or with later releases of DirectX.</span></span>

<span data-ttu-id="4d6c6-146">Si votre application rencontre des échecs inexpliqués lors de l’exécution avec le fichier d’exécution Direct3D de vente au détail, effectuez des tests sur la version de débogage et recherchez attentivement les cas où votre application transmet des paramètres non valides.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-146">If your application encounters unexplained failures when running with the retail Direct3D run-time file, test against the debug version and look closely for cases where your application passes invalid parameters.</span></span> <span data-ttu-id="4d6c6-147">Utilisez l’applet du panneau de configuration DirectX, basculez vers le runtime de débogage si nécessaire, puis activez l’option « arrêter sur D3DError ».</span><span class="sxs-lookup"><span data-stu-id="4d6c6-147">Use the DirectX control panel applet, switch to the debug runtime if necessary, and check the "Break on D3DError" option.</span></span> <span data-ttu-id="4d6c6-148">Cette option force le runtime à utiliser la méthode Windows DebugBreak afin de forcer l’arrêt de l’application lorsqu’un bogue de l’application est détecté.</span><span class="sxs-lookup"><span data-stu-id="4d6c6-148">This option will force the runtime to use the Windows DebugBreak method in order to force the application to stop when an application bug is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d6c6-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d6c6-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d6c6-150">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="4d6c6-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
