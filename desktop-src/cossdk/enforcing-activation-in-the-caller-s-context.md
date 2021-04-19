---
description: Application de l’activation dans le contexte des appelants
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Application de l’activation dans le contexte des appelants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514739"
---
# <a name="enforcing-activation-in-the-callers-context"></a><span data-ttu-id="db793-103">Application de l’activation dans le contexte de l’appelant</span><span class="sxs-lookup"><span data-stu-id="db793-103">Enforcing Activation in the Caller's Context</span></span>

<span data-ttu-id="db793-104">Vous pouvez contrôler si un objet est activé dans son propre contexte.</span><span class="sxs-lookup"><span data-stu-id="db793-104">You can control whether an object gets activated in its own context.</span></span> <span data-ttu-id="db793-105">Lorsque vous utilisez l’outil d’administration Services de composants pour exiger l’activation d’un composant dans le contexte de l’appelant, les opérations suivantes se produisent lorsque COM+ active une instance du composant dans un contexte :</span><span class="sxs-lookup"><span data-stu-id="db793-105">When you use the Component Services administrative tool to require component activation in the caller's context, the following occurs when COM+ activates an instance of the component in a context:</span></span>

-   <span data-ttu-id="db793-106">L’objet est activé dans le contexte du créateur, si possible.</span><span class="sxs-lookup"><span data-stu-id="db793-106">The object is activated in the creator's context if possible.</span></span>
-   <span data-ttu-id="db793-107">L’activation d’objet échoue si elle requiert son propre contexte ; CO \_ E \_ tentative \_ de \_ création d’un \_ \_ contexte client externe \_ est retourné.</span><span class="sxs-lookup"><span data-stu-id="db793-107">Object activation fails if it requires its own context; CO\_E\_ATTEMPT\_TO\_CREATE\_OUTSIDE\_CLIENT\_CONTEXT is returned.</span></span>

<span data-ttu-id="db793-108">Le fait que l’objet nécessite ou non son propre contexte dépend de sa configuration par rapport à l’état actuel des propriétés de contexte de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="db793-108">Whether or not the object requires its own context depends on its configuration relative to the current state of the caller's context properties.</span></span> <span data-ttu-id="db793-109">Pour plus d’informations, consultez [contextes com+](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="db793-109">For more detail, see [COM+ Contexts](com--contexts.md).</span></span>

<span data-ttu-id="db793-110">Vous souhaitez contrôler l’activation à un niveau précis si certains aspects de votre objet ne fonctionneront pas correctement s’ils ont son propre contexte.</span><span class="sxs-lookup"><span data-stu-id="db793-110">You would want to control activation at that fine a level if some aspect of your object would not function properly if it has its own context.</span></span> <span data-ttu-id="db793-111">Par exemple, si le composant ne prend pas en charge le marshaling et qu’il a son propre contexte, tous les appels à ce dernier échouent, car les appels entre les contextes sont interceptés et un marshaling léger effectué.</span><span class="sxs-lookup"><span data-stu-id="db793-111">For example, if the component does not support marshaling and it has its own context, any calls to it will fail because cross-context calls are intercepted and a lightweight marshal performed.</span></span>

<span data-ttu-id="db793-112">**Pour appliquer l’activation dans le contexte de l’appelant**</span><span class="sxs-lookup"><span data-stu-id="db793-112">**To enforce activation in the caller's context**</span></span>

1.  <span data-ttu-id="db793-113">Dans le volet d’informations de l’outil d’administration Services de composants, cliquez avec le bouton droit sur le composant (situé dans le dossier **composants** de n’importe quelle application com+ sélectionnée) pour lequel vous définissez les propriétés d’activation, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="db793-113">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) for which you are setting activation properties and then click **Properties**.</span></span>

2.  <span data-ttu-id="db793-114">Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **activation** .</span><span class="sxs-lookup"><span data-stu-id="db793-114">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="db793-115">Activez la case à cocher **doit être activé dans le contexte des appelants** .</span><span class="sxs-lookup"><span data-stu-id="db793-115">Select the **Must be activated in the callers context** check box.</span></span>

4.  <span data-ttu-id="db793-116">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="db793-116">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db793-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db793-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db793-118">Concepts d’activation juste-à-temps de COM+</span><span class="sxs-lookup"><span data-stu-id="db793-118">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="db793-119">Application de l’activation dans le contexte par défaut</span><span class="sxs-lookup"><span data-stu-id="db793-119">Enforcing Activation in the Default Context</span></span>](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



