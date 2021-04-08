---
title: Prise en main avec le kit de développement logiciel (SDK) Windows Media Player
description: Prise en main avec le kit de développement logiciel (SDK) Windows Media Player
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player Mobile, plug-ins
- Windows Media Player Mobile, plug-ins d’interface utilisateur
- Plug-ins Windows Media Player Mobile
- plug-ins, interface utilisateur
- plug-ins, Windows Media Player Mobile
- plug-ins d’interface utilisateur, Windows Media Player Mobile
- Plug-ins d’interface utilisateur, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739301"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a>Prise en main avec le kit de développement logiciel (SDK) Windows Media Player

Pour créer votre plug-in, vous devez d’abord installer Microsoft eMbedded Visual C++ 4,0 et Visual Studio 2003. Vous devez également installer le kit de développement logiciel (SDK) Pocket PC 2003 ou le kit de développement logiciel (SDK) Smartphone 2003, qui sont des téléchargements distincts. Pour compiler et exécuter le projet, un Pocket PC ou un appareil smartphone exécutant le système d’exploitation Windows Mobile 2003 deuxième édition doit être synchronisé avec l’ordinateur de développement à l’aide de Microsoft ActiveSync® 3.7.1 ou version ultérieure.

Étant donné que les plug-ins d’IU sur les périphériques Windows Mobile utilisent le même modèle de plug-in que les versions de bureau, vous pouvez utiliser l’Assistant de plug-in du lecteur Windows Media comme point de départ lors de la création d’un plug-in d’interface utilisateur d’arrière-plan qui fonctionne avec le lecteur Windows Media 10 mobile.

Pour créer un code de plug-in d’interface utilisateur, procédez comme suit :

1.  Ouvrez Visual Studio 2003 et démarrez un nouveau projet dans Visual C++.
2.  Sélectionnez l' **Assistant de plug-in du lecteur Windows Media** dans le volet **modèles** .
3.  Nommez votre projet NetworkPlugin, puis cliquez sur **OK**.
4.  Sélectionnez **plug-in d’interface utilisateur** , puis cliquez sur **suivant**.
5.  Sélectionnez **arrière-plan** , puis cliquez sur **suivant**.
6.  Cliquez sur **Suivant** pour terminer l'Assistant. Si vous envisagez de surveiller les événements avec votre plug-in, vous devez activer la case à cocher **écouter les événements** avant de terminer l’Assistant et vous devez lire la documentation de l’interface **IWMPEvents** pour connaître les événements pris en charge sur le lecteur Windows Media 10 mobile.

Maintenant que vous avez créé votre code de plug-in d’interface utilisateur, vous devez créer un projet de DLL Windows CE vide dans Embedded Visual C++ 4,0. Copiez ensuite vos fichiers sources générés par l’Assistant dans ce nouveau projet afin qu’ils se compilent avec le compilateur ARM4.

Pour créer un projet vide

1.  Démarrez un nouveau projet dans le Visual C++ incorporé, puis sélectionnez **bibliothèque de Dynamic-Link WCE** dans le volet **projets** .
2.  Nommez votre projet et cliquez sur **OK**.
3.  Assurez-vous qu' **un projet Windows ce dll vide** est sélectionné, puis cliquez sur **Terminer**.
4.  Cliquez sur l’élément de menu **projet** .
5.  Sélectionnez **Ajouter au projet**, puis cliquez sur **fichiers**.
6.  Sélectionnez les fichiers C++ que vous avez créés à l’aide de l’Assistant de plug-in, puis cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’un plug-in d’interface utilisateur pour Windows Media Player 10 mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[**Interface IWMPEvents**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




