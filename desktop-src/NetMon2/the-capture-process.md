---
description: Le processus de capture est le même pour chacune des quatre interfaces NPP.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: Processus de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552297"
---
# <a name="the-capture-process"></a>Processus de capture

Le processus de capture est le même pour chacune des quatre interfaces NPP. Dans chaque cas, le processus comprend les éléments suivants :

-   Obtention de l’objet d’interface NPP à utiliser
-   Connexion au réseau
-   Démarrage, puis arrêt de la [ *capture*](c.md)
-   Déconnexion du réseau

> [!Note]  
> Lorsque vous obtenez l’objet d’interface souhaité, veillez à appeler uniquement les méthodes incluses dans cette interface. L’illustration suivante montre que chaque interface fournit des méthodes similaires pour capturer les données réseau. Une erreur est retournée si vous vous connectez au réseau avec une interface, puis essayez d’exécuter une capture à l’aide des méthodes d’une autre interface.

 

Les illustrations suivantes montrent deux façons différentes d’exécuter une capture. La première illustration montre comment exécuter une ou plusieurs captures séquentielles, ce qui vous permet de créer n’importe quel nombre de captures indépendantes.

![capture séquentielle](images/capt1.png)

Comme indiqué ci-dessus, une fois que vous êtes connecté au réseau, vous pouvez démarrer et arrêter une capture autant de fois que vous le souhaitez, en démarrant une nouvelle capture et en générant de nouvelles statistiques chaque fois que vous redémarrez la capture. Par exemple, pour une capture différée à l’aide de l’interface [**IDelaydC**](idelaydc.md) , un nouveau [*fichier de capture*](c.md) est créé chaque fois que vous redémarrez la capture.

Toutefois, sachez également que chaque fois que vous redémarrez le processus de capture, vous devez appeler la méthode de configuration appropriée pour reconfigurer la connexion. Pour l’appel initial de démarrage de la capture, la connexion est configurée par l’appel de la connexion au réseau.

La deuxième illustration montre comment vous pouvez exécuter une capture unique en suspendant et redémarrant.

![capture unique en suspendant et redémarrant](images/capt2.png)

Dans ce cas, vous pouvez suspendre et redémarrer une capture autant de fois que vous le souhaitez. Avec cette approche, vous pouvez exécuter une capture dont les données (et les statistiques associées) sont enregistrées sous la forme d’une capture unique. Par exemple, pour effectuer une capture différée à l’aide de l’interface [**IDelaydC**](idelaydc.md) , toutes les informations réseau capturées sont enregistrées dans un [*fichier de capture*](c.md)unique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CreateNPPInterface**](createnppinterface.md)
</dt> <dt>

[**IDelaydC :: configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC :: Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC ::D éconnecter**](idelaydc-disconnect.md)
</dt> <dt>

[**IDelaydC ::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC :: Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC :: Start**](idelaydc-start.md)
</dt> <dt>

[**IDelaydC :: Stop**](idelaydc-stop.md)
</dt> <dt>

[**IESP :: configure**](iesp-configure.md)
</dt> <dt>

[**IESP :: Connect**](iesp-connect.md)
</dt> <dt>

[**IESP ::D éconnecter**](iesp-disconnect.md)
</dt> <dt>

[**IESP ::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP :: Resume**](iesp-resume.md)
</dt> <dt>

[**IESP :: Start**](iesp-start.md)
</dt> <dt>

[**IESP :: Stop**](iesp-stop.md)
</dt> <dt>

[**IRTC :: configure**](irtc-configure.md)
</dt> <dt>

[**IRTC :: Connect**](irtc-connect.md)
</dt> <dt>

[**IRTC ::D éconnecter**](irtc-disconnect.md)
</dt> <dt>

[**IRTC ::P ause**](irtc-pause.md)
</dt> <dt>

[**IRTC :: Resume**](irtc-resume.md)
</dt> <dt>

[**IRTC :: Start**](irtc-start.md)
</dt> <dt>

[**IRTC :: Stop**](irtc-stop.md)
</dt> <dt>

[**IStats :: configure**](istats-configure.md)
</dt> <dt>

[**IStats :: Connect**](istats-connect.md)
</dt> <dt>

[**IStats ::D éconnecter**](istats-disconnect.md)
</dt> <dt>

[**IStats ::P ause**](istats-pause.md)
</dt> <dt>

[**IStats :: Resume**](istats-resume.md)
</dt> <dt>

[**IStats :: Start**](istats-start.md)
</dt> <dt>

[**IStats :: Stop**](istats-stop.md)
</dt> </dl>

 

 



