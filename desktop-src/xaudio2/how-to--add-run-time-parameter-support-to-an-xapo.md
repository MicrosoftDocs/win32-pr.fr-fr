---
description: Vous pouvez ajouter la prise en charge des paramètres au moment de l’exécution à un XAPO en implémentant l’interface IXAPOParameters. La prise en charge des paramètres au moment de l’exécution permet à un XAPO de modifier son comportement en fonction des paramètres qui lui sont passés au moment de l’exécution.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 'Procédure : Ajouter la prise en charge de paramètre d’exécution à un XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582f51b3dfbdc6d31422494906d5f945f77ccb03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485177"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a><span data-ttu-id="f24df-104">Procédure : Ajouter la prise en charge de paramètre d’exécution à un XAPO</span><span class="sxs-lookup"><span data-stu-id="f24df-104">How to: Add Run-time Parameter Support to an XAPO</span></span>

<span data-ttu-id="f24df-105">Vous pouvez ajouter la prise en charge des paramètres au moment de l’exécution à un XAPO en implémentant l’interface [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) .</span><span class="sxs-lookup"><span data-stu-id="f24df-105">You can add run-time parameter support to an XAPO by implementing the [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interface.</span></span> <span data-ttu-id="f24df-106">La prise en charge des paramètres au moment de l’exécution permet à un XAPO de modifier son comportement en fonction des paramètres qui lui sont passés au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f24df-106">Run-time parameter support allows an XAPO to change its behavior based on the parameters passed to it at run time.</span></span>

1.  <span data-ttu-id="f24df-107">Suivez les étapes décrites dans [procédure : créer un XAPO](how-to--create-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="f24df-107">Follow the steps in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>
2.  <span data-ttu-id="f24df-108">Modifiez XAPO pour qu’il dérive de [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) et [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span><span class="sxs-lookup"><span data-stu-id="f24df-108">Change the XAPO to derive from [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) and [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span></span>
3.  <span data-ttu-id="f24df-109">Ajoutez des appels aux méthodes [**CXAPOParametersBase :: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) et [**CXAPOParametersBase :: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) à l’implémentation de [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span><span class="sxs-lookup"><span data-stu-id="f24df-109">Add calls to the methods [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) to the implementation of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

    > [!Note]  
    > <span data-ttu-id="f24df-110">L’ajout de ces méthodes à [IXAPO ::P tionnaire](how-to--build-a-basic-audio-processing-graph.md) permet à [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) de conserver ses copies des paramètres Effects dans un état thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f24df-110">Adding these methods to [IXAPO::Process](how-to--build-a-basic-audio-processing-graph.md) allows [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) to keep its copies of the effect parameters in a thread-safe state.</span></span> <span data-ttu-id="f24df-111">Appelez [**CXAPOParametersBase :: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) au début de [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process)et [**CXAPOParametersBase :: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) à la fin de **IXAPO ::P tionnaire**.</span><span class="sxs-lookup"><span data-stu-id="f24df-111">Call [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) at the beginning of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) at the end of **IXAPO::Process**.</span></span>

     

4.  <span data-ttu-id="f24df-112">Ajoutez du code à l’implémentation [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) pour modifier son comportement en fonction des valeurs stockées par la méthode [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) .</span><span class="sxs-lookup"><span data-stu-id="f24df-112">Add more code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation to change its behavior according to values stored by the [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="f24df-113">L’ajout de code à la méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) pour utiliser les paramètres spécifiés par [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) permet de modifier le comportement de XAPO tout au long de sa durée de vie.</span><span class="sxs-lookup"><span data-stu-id="f24df-113">Adding code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method to use the parameters specified by [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) allows the XAPO's behavior to be changed throughout its life.</span></span>

     

5.  <span data-ttu-id="f24df-114">Quand vous créez une instance de l’effet, allouez une mémoire tampon de trois des structures qui représenteront les paramètres de l’effet et transmettez-la au constructeur [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .</span><span class="sxs-lookup"><span data-stu-id="f24df-114">When you create an instance of the effect, allocate a buffer of three of the structures that will represent the effect's parameters, and pass it to the [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) constructor.</span></span>

    > [!Note]  
    > <span data-ttu-id="f24df-115">L’instance [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) utilise en interne cette mémoire tampon pour gérer les paramètres d’effet qui lui sont passés quand vous appelez [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters).</span><span class="sxs-lookup"><span data-stu-id="f24df-115">The [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) instance internally uses this buffer to manage effect parameters passed to it when you call [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters).</span></span> <span data-ttu-id="f24df-116">Vous devez initialiser tous les blocs de paramètres de processus dans *pParameterBlocks* à la même valeur par défaut avant d’appeler l’une des méthodes [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters :: GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)et **IXAPOParameters :: SetParameters** .</span><span class="sxs-lookup"><span data-stu-id="f24df-116">You must initialize all the process parameter blocks in *pParameterBlocks* to the same default value before you call any of the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters::GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters), and **IXAPOParameters::SetParameters** methods.</span></span> <span data-ttu-id="f24df-117">En général, cette initialisation est gérée dans [**IXAPO :: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) ou dans [**IXAPO :: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span><span class="sxs-lookup"><span data-stu-id="f24df-117">Usually this initialization is handled in [**IXAPO::Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) or in [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="f24df-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f24df-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f24df-119">Effets audio</span><span class="sxs-lookup"><span data-stu-id="f24df-119">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="f24df-120">Présentation de XAPO</span><span class="sxs-lookup"><span data-stu-id="f24df-120">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
