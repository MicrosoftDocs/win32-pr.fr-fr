---
title: Prise en main avec le kit de développement logiciel (SDK) Lecteur Windows Media
description: Prise en main avec le kit de développement logiciel (SDK) Lecteur Windows Media
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Lecteur Windows Media Périphériques mobiles, plug-ins
- Lecteur Windows Media Périphériques mobiles, plug-ins d’interface utilisateur
- Lecteur Windows Media Plug-ins mobiles
- plug-ins, interface utilisateur
- plug-ins, Lecteur Windows Media Mobile
- plug-ins d’interface utilisateur, Lecteur Windows Media Mobile
- plug-ins d’interface utilisateur, Lecteur Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7c18157511364b4846b79b8f9a4e617ba7fe87a9f37535d5eaf112546dba28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934569"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a>Prise en main avec le kit de développement logiciel (SDK) Lecteur Windows Media

pour créer votre plug-in, vous devez d’abord installer Microsoft embedded Visual C++ 4,0 et Visual Studio 2003. vous devez également installer le kit de développement logiciel (sdk) Pocket PC 2003 ou le kit de développement logiciel (sdk) Smartphone 2003, qui sont des téléchargements distincts. pour compiler et exécuter le projet, un Pocket PC ou un appareil Smartphone exécutant le système d’exploitation Windows Mobile 2003 Second Edition doit être synchronisé avec l’ordinateur de développement à l’aide de Microsoft ActiveSync® 3.7.1 ou version ultérieure.

étant donné que les plug-ins d’iu sur Windows appareils mobiles utilisent le même modèle de plug-in que les versions de bureau, vous pouvez utiliser l’assistant de plug-in Lecteur Windows Media comme point de départ lors de la création d’un plug-in d’iu d’arrière-plan qui fonctionne avec Lecteur Windows Media 10 Mobile.

Pour créer un code de plug-in d’interface utilisateur, procédez comme suit :

1.  ouvrez Visual Studio 2003 et démarrez un nouveau projet dans Visual C++.
2.  dans le volet **modèles** , sélectionnez **Lecteur Windows Media assistant de Plug-** in.
3.  Nommez votre projet NetworkPlugin, puis cliquez sur **OK**.
4.  Sélectionnez **plug-in d’interface utilisateur** , puis cliquez sur **suivant**.
5.  Sélectionnez **arrière-plan** , puis cliquez sur **suivant**.
6.  Cliquez sur **Suivant** pour terminer l'Assistant. si vous envisagez de surveiller les événements avec votre plug-in, vous devez activer la case à cocher **écouter les événements** avant de terminer l’assistant et vous devez lire la documentation de l’interface **IWMPEvents** pour savoir quels événements sont pris en charge sur Lecteur Windows Media 10 Mobile.

maintenant que vous avez créé votre code de plug-in d’interface utilisateur, vous devez créer un projet de DLL Windows CE vide dans embedded Visual C++ 4,0. Copiez ensuite vos fichiers sources générés par l’Assistant dans ce nouveau projet afin qu’ils se compilent avec le compilateur ARM4.

Pour créer un projet vide

1.  démarrez un nouveau projet dans le Visual C++ incorporé, puis sélectionnez **WCE Dynamic-Link bibliothèque** dans le volet **projets** .
2.  Nommez votre projet et cliquez sur **OK**.
3.  assurez-vous qu' **un projet Windows CE DLL vide** est sélectionné, puis cliquez sur **terminer**.
4.  cliquez sur l’élément de menu **Project** .
5.  sélectionnez **ajouter au Project**, puis cliquez sur **fichiers**.
6.  Sélectionnez les fichiers C++ que vous avez créés à l’aide de l’Assistant de plug-in, puis cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**création d’un Plug-in d’Interface utilisateur pour Lecteur Windows Media 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[**Interface IWMPEvents**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




