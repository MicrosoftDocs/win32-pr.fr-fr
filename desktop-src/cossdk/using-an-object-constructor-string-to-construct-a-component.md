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
# <a name="using-an-object-constructor-string-to-construct-a-component"></a>Utilisation d’une chaîne de constructeur d’objet pour construire un composant

L’exemple suivant montre comment récupérer et utiliser par programmation une chaîne de constructeur d’objet lors de l’instanciation d’un composant. Il illustre une implémentation de l’interface [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) qui récupère une chaîne de constructeur d’objet. La chaîne peut ensuite être analysée pour définir les valeurs initiales ou influencer le comportement du composant.

## <a name="visual-basic"></a>Visual Basic


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts des chaînes du constructeur d’objet COM+](com--object-constructor-strings-concepts.md)
</dt> <dt>

[Spécification d’une chaîne de constructeur d’objet pour un composant](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



