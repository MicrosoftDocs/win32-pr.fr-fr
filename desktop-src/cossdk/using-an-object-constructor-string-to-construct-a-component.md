---
description: Utilisation d’une chaîne de constructeur d’objet pour construire un composant
ms.assetid: 57d66988-2a65-4309-957a-36a5972233b5
title: Utilisation d’une chaîne de constructeur d’objet pour construire un composant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cbbb1c156fd7ee675b6c21c8ae097494da59ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483409"
---
# <a name="using-an-object-constructor-string-to-construct-a-component"></a><span data-ttu-id="22e11-103">Utilisation d’une chaîne de constructeur d’objet pour construire un composant</span><span class="sxs-lookup"><span data-stu-id="22e11-103">Using an Object Constructor String to Construct a Component</span></span>

<span data-ttu-id="22e11-104">L’exemple suivant montre comment récupérer et utiliser par programmation une chaîne de constructeur d’objet lors de l’instanciation d’un composant.</span><span class="sxs-lookup"><span data-stu-id="22e11-104">The following example illustrates how to programmatically retrieve and use an object constructor string when a component is instantiated.</span></span> <span data-ttu-id="22e11-105">Il illustre une implémentation de l’interface [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) qui récupère une chaîne de constructeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="22e11-105">It shows an implementation of the [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) interface that retrieves an object constructor string.</span></span> <span data-ttu-id="22e11-106">La chaîne peut ensuite être analysée pour définir les valeurs initiales ou influencer le comportement du composant.</span><span class="sxs-lookup"><span data-stu-id="22e11-106">The string can then be parsed to set initial values or influence the behavior of the component.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="22e11-107">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="22e11-107">Visual Basic</span></span>


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="22e11-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22e11-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22e11-109">Concepts des chaînes du constructeur d’objet COM+</span><span class="sxs-lookup"><span data-stu-id="22e11-109">COM+ Object Constructor Strings Concepts</span></span>](com--object-constructor-strings-concepts.md)
</dt> <dt>

[<span data-ttu-id="22e11-110">Spécification d’une chaîne de constructeur d’objet pour un composant</span><span class="sxs-lookup"><span data-stu-id="22e11-110">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



