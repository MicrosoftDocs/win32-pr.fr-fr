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
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a>Procédure : Ajouter la prise en charge de paramètre d’exécution à un XAPO

Vous pouvez ajouter la prise en charge des paramètres au moment de l’exécution à un XAPO en implémentant l’interface [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) . La prise en charge des paramètres au moment de l’exécution permet à un XAPO de modifier son comportement en fonction des paramètres qui lui sont passés au moment de l’exécution.

1.  Suivez les étapes décrites dans [procédure : créer un XAPO](how-to--create-an-xapo.md).
2.  Modifiez XAPO pour qu’il dérive de [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) et [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).
3.  Ajoutez des appels aux méthodes [**CXAPOParametersBase :: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) et [**CXAPOParametersBase :: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) à l’implémentation de [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

    > [!Note]  
    > L’ajout de ces méthodes à [IXAPO ::P tionnaire](how-to--build-a-basic-audio-processing-graph.md) permet à [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) de conserver ses copies des paramètres Effects dans un état thread-safe. Appelez [**CXAPOParametersBase :: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) au début de [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process)et [**CXAPOParametersBase :: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) à la fin de **IXAPO ::P tionnaire**.

     

4.  Ajoutez du code à l’implémentation [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) pour modifier son comportement en fonction des valeurs stockées par la méthode [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) .

    > [!Note]  
    > L’ajout de code à la méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) pour utiliser les paramètres spécifiés par [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) permet de modifier le comportement de XAPO tout au long de sa durée de vie.

     

5.  Quand vous créez une instance de l’effet, allouez une mémoire tampon de trois des structures qui représenteront les paramètres de l’effet et transmettez-la au constructeur [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .

    > [!Note]  
    > L’instance [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) utilise en interne cette mémoire tampon pour gérer les paramètres d’effet qui lui sont passés quand vous appelez [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters). Vous devez initialiser tous les blocs de paramètres de processus dans *pParameterBlocks* à la même valeur par défaut avant d’appeler l’une des méthodes [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters :: GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)et **IXAPOParameters :: SetParameters** . En général, cette initialisation est gérée dans [**IXAPO :: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) ou dans [**IXAPO :: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).

     

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets audio](audio-effects.md)
</dt> <dt>

[Présentation de XAPO](xapo-overview.md)
</dt> </dl>

 

 
